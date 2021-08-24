---
title: Cifrado para Skype, OneDrive, SharePoint y Exchange
description: 'Resumen: una descripción del cifrado para Skype, OneDrive, SharePoint, Microsoft Teams y Exchange Online.'
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- SPO_Content
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 480e7e03564075707c90e25ad5777631c1e68ed8
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482032"
---
# <a name="encryption-for-skype-for-business-onedrive-for-business-sharepoint-online-microsoft-teams-and-exchange-online"></a>Cifrado para Skype Empresarial, OneDrive para la Empresa, SharePoint Online, Microsoft Teams y Exchange Online

Microsoft 365 es un entorno altamente seguro que ofrece una protección extensa en varias capas: seguridad del centro de datos físico, seguridad de red, seguridad de acceso, seguridad de aplicaciones y seguridad de datos.

## <a name="skype-for-business"></a>Skype Empresarial

Skype Empresarial datos del cliente pueden almacenarse en reposo en forma de archivos o presentaciones que los participantes de la reunión cargan. El servidor de conferencia web cifra los datos de los clientes mediante AES con una clave de 256 bits. Los datos de cliente cifrados se almacenan en un recurso compartido de archivos. Cada fragmento de datos del cliente se cifra con una clave de 256 bits generada aleatoriamente. Cuando se comparte un fragmento de datos de cliente en una conferencia, el servidor de conferencia web indica a los clientes de conferencia que descarguen los datos cifrados del cliente a través de HTTPS. Envía la clave correspondiente a los clientes para que se puedan descifrar los datos del cliente. El servidor de conferencia web también autentica a los clientes de conferencia antes de que permita a los clientes acceder a los datos de los clientes de conferencia. Al unirse a una conferencia web, cada cliente de conferencia establece un cuadro de diálogo SIP con el componente de foco de conferencia que se ejecuta en el servidor front-end a través de TLS primero. El foco de conferencia pasa al cliente de conferencia una cookie de autenticación generada por el servidor de conferencia web. A continuación, el cliente de conferencia se conecta al servidor de conferencia web que presenta la cookie de autenticación que el servidor va a autenticar.

## <a name="sharepoint-online-and-onedrive-for-business"></a>SharePoint en línea y OneDrive para Empresas

Todos los archivos de cliente SharePoint Online están protegidos por claves únicas por archivo que siempre son exclusivas de un único inquilino. El servicio de SharePoint Online crea y administra las claves, o cuando los clientes usan, crean y administran la clave de cliente. Cuando se carga un archivo, SharePoint Online realiza el cifrado en el contexto de la solicitud de carga, antes de enviarse a Azure Storage. Cuando se descarga un archivo, SharePoint Online recupera los datos de cliente cifrados de Azure Storage en función del identificador de documento único y descifra los datos del cliente antes de enviarlos al usuario. Azure Storage no tiene capacidad para descifrar ni siquiera identificar o comprender los datos del cliente. Todo el cifrado y descifrado ocurren en los mismos sistemas que aplican el aislamiento de inquilinos, que se Azure Active Directory y SharePoint online.

Varias cargas de trabajo de Microsoft 365 almacenan datos en SharePoint Online, incluido Microsoft Teams, que almacena todos los archivos en SharePoint Online y OneDrive para la Empresa, que usa SharePoint Online para su almacenamiento. Todos los datos de clientes almacenados en SharePoint Online se cifran (con una o más claves de AES de 256 bits) y se distribuyen en el centro de datos de la siguiente manera. (Cada paso de este proceso de cifrado es fips 140-2 nivel 2 validado. Para obtener información adicional sobre el cumplimiento de FIPS 140-2, vea [FIPS 140-2 Compliance](/previous-versions/sql/sql-server-2008-r2/bb326611(v=sql.105)).)

- Cada archivo se divide en uno o más fragmentos, según el tamaño del archivo. Cada fragmento se cifra con su propia clave AES de 256 bits única.
- Cuando se actualiza un archivo, la actualización se controla de la misma manera: el cambio se divide en uno o más fragmentos y cada fragmento se cifra con una clave única independiente.
- Estos fragmentos (archivos, fragmentos de archivos y deltas de actualización) se almacenan como blobs en Azure Storage que se distribuyen aleatoriamente entre varias cuentas de Azure Storage.
- El conjunto de claves de cifrado de estos fragmentos de datos de cliente se cifra en sí mismo.

    - Las claves usadas para cifrar los blobs se almacenan en la SharePoint de contenido en línea.
    - La base de datos de contenido está protegida por controles de acceso a bases de datos y cifrado en reposo. El cifrado se [realiza Cifrado de datos transparente](/sql/relational-databases/security/encryption/transparent-data-encryption-tde) (TDE) en [Azure SQL Database](/azure/sql-database/sql-database-technical-overview). (Azure SQL Database es un servicio de base de datos relacional de uso general en Microsoft Azure que admite estructuras como datos relacionales, JSON, espaciales y XML). Estos secretos están en el nivel de servicio para SharePoint Online, no en el nivel de inquilino. Estos secretos (a veces denominados claves maestras) se almacenan en un repositorio seguro independiente denominado Almacén de claves. TDE proporciona seguridad en reposo tanto para la base de datos activa como para las copias de seguridad de la base de datos y los registros de transacciones.
    - Cuando los clientes proporcionan la clave opcional, la clave de cliente se almacena en Azure Key Vault y el servicio usa la clave para cifrar una clave de inquilino, que se usa para cifrar una clave de sitio, que luego se usa para cifrar las claves de nivel de archivo. Básicamente, se introduce una nueva jerarquía de claves cuando el cliente proporciona una clave.
- El mapa usado para volver a ensamblar el archivo se almacena en la base de datos de contenido junto con las claves cifradas, por separado de la clave maestra necesaria para descifrarlas.
- Cada cuenta de Azure Storage tiene sus propias credenciales únicas por tipo de acceso (lectura, escritura, enumeración y eliminación). Cada conjunto de credenciales se encuentra en el almacén de claves seguras y se actualiza periódicamente. Como se describió anteriormente, hay tres tipos diferentes de almacenes, cada uno con una función distinta:
    - Los datos del cliente se almacenan como blobs cifrados en Azure Storage. La clave de cada fragmento de datos del cliente se cifra y almacena por separado en la base de datos de contenido. Los datos del cliente en sí no tienen ninguna pista sobre cómo se pueden descifrar.
    - La base de datos de contenido es una base de datos de SQL Server. Contiene el mapa necesario para localizar y volver a ensamblar los blobs de datos del cliente que se mantienen en Azure Storage, así como las claves necesarias para cifrar esos blobs. Sin embargo, el conjunto de claves se cifra en sí mismo (como se explicó anteriormente) y se mantiene en un almacén de claves independiente.
    - El almacén de claves es físicamente independiente de la base de datos de contenido y el almacenamiento de Azure. Contiene las credenciales de cada contenedor de Azure Storage y la clave maestra del conjunto de claves cifradas que se mantienen en la base de datos de contenido.

Cada uno de estos tres componentes de almacenamiento (el almacén de blobs de Azure, la base de datos de contenido y el almacén de claves) es físicamente independiente. La información contenida en cualquiera de los componentes es inutilizable por sí misma. Sin acceso a los tres, es imposible recuperar las claves de los fragmentos, descifrar las claves para que se puedan usar, asociar las claves con sus fragmentos correspondientes, descifrar cada fragmento o reconstruir un documento de sus fragmentos constituyentes.

Los certificados de BitLocker, que protegen los volúmenes de disco físico de las máquinas del centro de datos, se almacenan en un repositorio seguro (el almacén secreto de SharePoint Online) protegido por la clave de granja de servidores.

Las claves TDE que protegen las claves por blob se almacenan en dos ubicaciones:

- El repositorio seguro, que aloja los certificados de BitLocker y está protegido por la clave de la granja de servidores; y
- En un repositorio seguro administrado por Azure SQL Database.

Las credenciales usadas para obtener acceso a los contenedores de Azure Storage también se mantienen en el almacén secreto de SharePoint Online y se delegan en cada granja de servidores SharePoint Online según sea necesario. Estas credenciales son firmas SAS de Azure Storage, con credenciales independientes que se usan para leer o escribir datos, y con directiva aplicada para que expiren automáticamente cada 60 días. Se usan credenciales diferentes para leer o escribir datos (no ambos) y SharePoint granjas de servidores en línea no tienen permisos para enumerar.

> [!NOTE]
> Para Office 365 los clientes gubernamentales de Estados Unidos, los blobs de datos se almacenan en Azure U.S. Government Storage. Además, el acceso SharePoint claves en línea en Office 365 gobierno de estados unidos está limitado a Office 365 personal que se ha realizado una pantalla específica. El personal de operaciones de Azure U.S. Government no tiene acceso al almacén de claves de SharePoint Online que se usa para cifrar blobs de datos.

Para obtener más información acerca del cifrado de datos en SharePoint Online y OneDrive para la Empresa, vea [Data Encryption in OneDrive para la Empresa and SharePoint Online](https://technet.microsoft.com/library/dn905447.aspx).

### <a name="list-items-in-sharepoint-online"></a>Enumerar elementos en SharePoint Online

Los elementos de lista son fragmentos más pequeños de datos de clientes que se crean ad-hoc o que pueden vivir de forma más dinámica dentro de un sitio, como filas en una lista creada por el usuario, publicaciones individuales en un blog de SharePoint Online o entradas dentro de una página wiki de SharePoint Online. Los elementos de lista se almacenan en la base de datos de contenido (Azure SQL Database) y se protegen con TDE.

## <a name="encryption-of-data-in-transit"></a>Cifrado de datos en tránsito

En OneDrive para la Empresa y SharePoint Online, hay dos escenarios en los que los datos entran y salen de los centros de datos.

- **Comunicación del cliente con el servidor:** la comunicación con SharePoint Online y OneDrive para la Empresa a través de Internet usa conexiones TLS.
- **Movimiento de datos entre centros de datos:** el motivo principal para mover datos entre centros de datos es la replicación geográfica para habilitar la recuperación ante desastres. Por ejemplo, los registros de transacciones y diferencias de almacenamiento de blobs de SQL Server recorren esta canalización. Mientras que estos datos ya se transmiten mediante una red privada, tendrán una mayor protección con el mejor cifrado de su clase.

## <a name="exchange-online"></a>Exchange en línea

Exchange Online usa BitLocker para todos los datos del buzón y la configuración de BitLocker se describe en [BitLocker para cifrado](/microsoft-365/compliance/office-365-bitlocker-and-distributed-key-manager-for-encryption). El cifrado de nivel de servicio cifra todos los datos del buzón en el nivel de buzón. 

Además del cifrado de servicio, Microsoft 365 es compatible con la clave de cliente, que se basa en el cifrado de servicio. Clave de cliente es una opción de clave administrada por Microsoft Exchange Online cifrado de servicio que también se encuentra en la guía básica de Microsoft. Este método de cifrado proporciona una mayor protección que BitLocker no proporciona porque proporciona la separación de los administradores del servidor y las claves criptográficas necesarias para el descifrado de datos y porque el cifrado se aplica directamente a los datos (a diferencia de BitLocker, que aplica cifrado en el volumen de disco lógico), los datos de clientes copiados desde un servidor de Exchange permanecen cifrados.

El ámbito del cifrado Exchange Online servicio son los datos del cliente que se almacenan en reposo dentro de Exchange Online. (Skype Empresarial almacena casi todo el contenido generado por el usuario en el buzón de correo Exchange Online del usuario y, por lo tanto, hereda la característica de cifrado de servicio de Exchange Online).


## <a name="microsoft-teams"></a>Microsoft Teams

Teams TLS y MTLS para cifrar mensajes instantáneos. Todo el tráfico de servidor a servidor requiere MTLS, independientemente de si el tráfico se limita a la red interna o si atraviesa el perímetro de red interno.

En esta tabla se resumen los protocolos usados por Teams.

|**Tipo de tráfico**|**Cifrado por**|
|:-----|:-----|
|Servidor a servidor|MTLS|
|Cliente a servidor (por ejemplo. mensajería instantánea y presencia)|TLS|
|Flujos de medios (por ejemplo. uso compartido de audio y vídeo de medios)|TLS|
|Uso compartido de audio y vídeo de medios|SRTP/TLS|
|Señalización|TLS|

#### <a name="media-encryption"></a>Cifrado de medios

El tráfico de medios se cifra mediante RTP seguro (SRTP), que es un protocolo de transporte en tiempo real (RTP) que proporciona al tráfico RTP confidencialidad, autenticación y protección contra los ataques de reproducción. SRTP usa una clave de sesión generada mediante un generador de números aleatorios seguros y se intercambia mediante el canal TLS de señalización. El tráfico de medios de cliente a cliente se negocia a través de una señalización de conexión de cliente a servidor, pero se cifra mediante SRTP al ir de cliente a cliente directamente.

Teams un token basado en credenciales para el acceso seguro a las retransmisiones multimedia a través de TURN. Las retransmisiones multimedia intercambian el token a través de un canal protegido por TLS.

#### <a name="fips"></a>FIPS

Teams algoritmos compatibles con FIPS (Federal Information Processing Standard) para intercambios de claves de cifrado. Para obtener más información sobre la implementación de FIPS, consulte [Federal Information Processing Standard (FIPS) Publication 140-2](/microsoft-365/compliance/offering-fips-140-2).
