---
title: Resistencia de datos de Exchange Online en Microsoft 365
description: En este artículo, encuentre una explicación de los diversos aspectos de la resistencia de datos dentro de Exchange Online y Microsoft 365.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 0e3f050c1f28fa0ca8ac89c8bb8d7151cf9cba10
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947266"
---
# <a name="exchange-online-data-resiliency-in-microsoft-365"></a>Exchange Online resistencia de datos en Microsoft 365

>[!IMPORTANT]
>A medida que seguimos invirtiendo en diferentes formas de conservar el contenido del buzón, anunciamos la retirada de las retenciones de In-Place en el Centro de administración de Exchange (EAC) en Exchange Online. A partir del 1 de julio de 2020, no podrá crear nuevas In-Place retenciones. Pero aún podrá administrar las In-Place en el EAC o mediante el cmdlet **Set-MailboxSearch** en Exchange Online PowerShell. Sin embargo, a partir del 1 de octubre de 2020, no podrá administrar las In-Place retenciones. Solo podrá quitarlos en el EAC o mediante el cmdlet **Remove-MailboxSearch.** El In-Place de espera en Exchange Server y Exchange las implementaciones híbridas seguirán siendo compatibles. Para obtener más información acerca de la retirada de In-Place en Exchange Online, vea [Retirement of legacy eDiscovery tools](/microsoft-365/compliance/legacy-ediscovery-retirement).

Una conservación local conserva todo el contenido de un buzón de correo, incluidos los elementos eliminados y las versiones originales de los elementos modificados. Todos los elementos del buzón de correo se devuelven en una búsqueda de [Exhibición de documentos electrónicos en contexto](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery). Cuando se coloca una retención de In-Place en el buzón de un usuario, el contenido del buzón de archivo correspondiente (si está habilitado) también se coloca en espera y se devuelve en una búsqueda de exhibición de documentos electrónicos.

Hay dos tipos de daños que pueden afectar a una base de datos de Exchange: daños físicos, que suelen deberse a problemas de hardware (en particular, hardware de almacenamiento) y daños lógicos, que se producen debido a otros factores. Por lo general, hay dos tipos de daños lógicos que pueden producirse en una base Exchange datos:

- **Daños lógicos de la** base de datos: la suma de comprobación de la página de base de datos coincide, pero los datos de la página son incorrectos lógicamente. Esto puede ocurrir cuando el motor de base de datos (el Motor extensible de Storage (ESE)) intenta escribir una página de base de datos y, aunque el sistema operativo devuelve un mensaje de éxito, los datos nunca se escriben en el disco o se escriben en el lugar incorrecto. Esto se conoce como vaciado *perdido*. ESE incluye numerosas características y protecciones diseñadas para evitar daños físicos de una base de datos y otros escenarios de pérdida de datos. Para evitar que los vaciados perdidos pierdan datos, ESE incluye un mecanismo de detección de vaciado perdido en la base de datos junto con una característica (restauración de una sola página) para corregirlo.
- **Almacenar daños lógicos:** los datos se agregan, eliminan o manipulan de forma que el usuario no espera. Estos casos son causados por aplicaciones de terceros. Por lo general, se trata de daños en el sentido de que el usuario lo ve como dañado. El almacén de Exchange considera que la transacción que produce los daños de lógica es una serie de operaciones MAPI válidas. Las [características de](/exchange/security-and-compliance/create-or-remove-in-place-holds) retención local en Exchange Online proporciona protección contra daños lógicos del almacén (ya que impide que un usuario o una aplicación eliminen el contenido de forma permanente). 

Exchange Online varias comprobaciones de coherencia en archivos de registro replicados durante la inspección de registros y la reproducción de registros. Estas comprobaciones de coherencia impiden que el sistema replique los daños físicos. Por ejemplo, durante la inspección del registro, hay una comprobación de integridad física que comprueba el archivo de registro y valida que la suma de comprobación registrada en el archivo de registro coincide con la suma de comprobación generada en la memoria. Además, se examina el encabezado del archivo de registro para asegurarse de que la firma del archivo de registro registrada en el encabezado del registro coincide con la del archivo de registro. Durante la reproducción del registro, el archivo de registro se somete a un mayor escrutinio. Por ejemplo, el encabezado de base de datos también contiene la firma de registro que se compara con la firma del archivo de registro para asegurarse de que coinciden. 

La protección contra daños de los datos de buzones de correo en Exchange Online se logra mediante la protección de datos nativa de Exchange, una estrategia de resistencia que aprovecha la replicación a nivel de aplicación en varios servidores y varios centros de datos, junto con otras características que ayudan a proteger los datos de pérdidas debido a daños u otros motivos. Estas características incluyen características nativas administradas por Microsoft o la propia aplicación Exchange Online, como:

- [Grupos de disponibilidad de datos](/exchange/back-up-email)
- Corrección de un solo bit 
- Análisis de bases de datos en línea 
- Detección de vaciado perdido 
- Restauración de una sola página 
- Servicio de replicación de buzones 
- Comprobaciones de archivos de registro 
- Implementación en el sistema de archivos resistente 

Para obtener más información sobre las características nativas enumeradas anteriormente, seleccione los hipervínculos y vea lo siguiente para obtener información adicional y detalles sobre los elementos sin hipervínculos. Además de estas características nativas, Exchange Online también incluye características de resistencia de datos que los clientes pueden administrar, como: 
- [Recuperación de elementos únicos (habilitada de forma predeterminada)](/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages) 
- [Conservación local y retención por juicio](/exchange/security-and-compliance/in-place-and-litigation-holds) 
- [Retención de elementos eliminados y Soft-Deleted buzones de correo (ambos habilitados de forma predeterminada)](/exchange/recipients-in-exchange-online/delete-or-restore-mailboxes) 

## <a name="database-availability-groups"></a>Grupos de disponibilidad de base de datos 
Todas las bases de datos de buzones de Microsoft 365 se hospedan en un grupo de disponibilidad de base de datos [(DAG)](/exchange/back-up-email) y se replican en centros de datos separados geográficamente dentro de la misma región. La configuración más común son cuatro copias de base de datos en cuatro centros de datos; sin embargo, algunas regiones tienen menos centros de datos (las bases de datos se replican en tres centros de datos en india y dos centros de datos en Australia y Japón). Pero en todos los casos, cada base de datos de buzones de correo tiene cuatro copias distribuidas en varios centros de datos, lo que garantiza que los datos del buzón estén protegidos contra errores de software, hardware e incluso centros de datos. 

De estas cuatro copias, tres de ellas están configuradas como altamente disponibles. La cuarta copia se configura como [una copia de base de datos con latencia.](/Exchange/high-availability/manage-ha/activate-lagged-db-copies) La copia de base de datos con latencia no está diseñada para la recuperación individual de buzones de correo o la recuperación de elementos de buzón. Su propósito es proporcionar un mecanismo de recuperación para el raro evento de daños lógicos catastróficos en todo el sistema. 

Las copias de base de datos Exchange Online se configuran con un tiempo de retraso de reproducción de archivos de registro de siete días. Además, el Administrador de retrasos de reproducción de Exchange está habilitado para proporcionar la reproducción dinámica de archivos de registro para copias con retraso para permitir que las copias de bases de datos con retraso se puedan reparar automáticamente y administrar el crecimiento de archivos de registro. Aunque se usan copias de base de datos Exchange Online, es importante comprender que no son una copia de seguridad de un momento dado garantizado. Las copias de base de datos con latencia en Exchange Online tienen un umbral de disponibilidad, normalmente alrededor del 90 %, debido a períodos en los que el disco que contiene una copia con un disco rezagado se pierde debido a un error en el disco, la copia de latencia se convierte en una copia de alta disponibilidad (debido a la reproducción automática), así como los períodos en los que la copia de base de datos de latencia está recompilando la cola de reproducción de registros. 

## <a name="transport-resilience"></a>Resistencia de transporte 
Exchange Online incluye dos características de resistencia de transporte principales: Redundancia de instantáneas y Red de seguridad. La redundancia de instantáneas mantiene una copia redundante de un mensaje mientras está en tránsito. La red de seguridad conserva una copia redundante de un mensaje después de que el mensaje se entregue correctamente. 

Con la redundancia de instantáneas, Exchange Online servidor de transporte realiza una copia de cada mensaje que recibe antes de que reconozca que recibe correctamente el mensaje en el servidor de envío. Esto hace que todos los mensajes de la canalización de transporte sea redundante mientras están en tránsito. Si Exchange Online determina que el mensaje original se perdió en tránsito, se reenvía una copia redundante del mensaje. 

Red de seguridad es una cola de transporte asociada al servicio de transporte en un servidor de buzones. Esta cola almacena copias de mensajes correctamente procesados por el servidor. Cuando una base de datos de buzones o un error de servidor requiere activar una copia desuso de la base de datos de buzones de correo, los mensajes de la cola de red de seguridad se envían automáticamente a la nueva copia activa de la base de datos de buzones de correo. La red de seguridad también es redundante, lo que elimina el transporte como un único punto de error. Usa el concepto de una red de seguridad principal y una red de seguridad de instantáneas en las que si la red de seguridad principal no está disponible durante más de 12 horas, las solicitudes de reenvío se convierten en solicitudes de reenvío de instantáneas y los mensajes se vuelven a enviar desde la red de seguridad de instantáneas.

Las reenmisiones de mensajes desde la red de seguridad se inician automáticamente por el componente de Active Manager del servicio de replicación de Microsoft Exchange que administra dag y copias de bases de datos de buzones de correo. No se requiere ninguna acción manual para reenviar mensajes desde la red de seguridad. 

## <a name="single-bit-correction"></a>Corrección de un solo bit 
ESE incluye un mecanismo para detectar y resolver errores CRC de un solo bit (también conocidos como volteos de un solo bit) que son el resultado de errores de hardware (y por lo tanto representan daños físicos). Cuando se producen estos errores, ESE los corrige automáticamente y registra un evento en el registro de eventos. 

## <a name="online-database-scanning"></a>Análisis de bases de datos en línea 
El examen de bases de datos en línea (también conocido como suma de comprobaciones de base de *datos)* es el proceso en el que un ESE usa un control de coherencia de la base de datos para leer cada página y comprobar si hay daños en la página. El objetivo principal es detectar daños físicos y vaciados perdidos que pueden no detectarse mediante operaciones transaccionales. El examen de bases de datos también realiza operaciones de bloqueo posteriores al almacén. El espacio se puede perder debido a bloqueos y el análisis de bases de datos en línea busca y recupera espacio perdido. El sistema está diseñado con la expectativa de que cada base de datos se examina completamente una vez cada siete días. 

## <a name="lost-flush-detection"></a>Detección de vaciado perdido 
Un vaciado perdido se produce cuando una operación de escritura de base de datos que el subsistema de disco/sistema operativo devuelto como completado no se escribió realmente en el disco o se escribió en la ubicación incorrecta. Los incidentes de vaciado perdidos pueden provocar daños lógicos en la base de datos, por lo que para evitar que los vaciados perdidos den como resultado la pérdida de datos, ESE incluye un mecanismo de detección de vaciado perdido. A medida que las páginas de base de datos se escriben en copias pasivas, se realiza una comprobación de los vaciados perdidos en la copia activa. Si se detecta un vaciado perdido, ESE puede reparar el proceso mediante un proceso de revisión de página. 

## <a name="single-page-restore"></a>Restauración de una sola página 
La restauración de una sola página, también conocida como revisión de *páginas,* es un proceso automático en el que las páginas de base de datos dañadas se reemplazan por copias en buen estado de una réplica en buen estado. El proceso de reparación de una página dañada depende de si la copia de la base de datos es activa o pasiva. Cuando una copia de base de datos activa encuentra una página dañada, puede copiar una página de una de sus réplicas, siempre que la página que copie esté actualizada. Este proceso se realiza colocando una solicitud para la página en la secuencia de registro, que es la base de la replicación de bases de datos de buzones de correo. Tan pronto como una réplica encuentra la solicitud de página, responde enviando una copia de la página a la copia de base de datos solicitante. La restauración de una sola página también proporciona un mecanismo de comunicación asincrónica para que el activo solicite una página a réplicas, incluso si las réplicas están actualmente sin conexión. 

En caso de daños en una copia pasiva de base de datos, incluida una copia de base de datos atrasada, ya que estas copias siempre están detrás de su copia activa, siempre es seguro copiar cualquier página de la copia activa en una copia pasiva. Por naturaleza, una copia pasiva de base de datos está altamente disponible, por lo que durante el proceso de revisión de página, la reproducción de registros se suspende, pero la copia de registros continúa. La copia pasiva de la base de datos recupera una copia de la página dañada de la copia activa, espera hasta que se copia e inspecciona el archivo de registro que cumple el requisito máximo necesario de generación de registros y, a continuación, se revisa la página dañada. Una vez que se ha parcheado la página, se reanuda la reproducción del registro. El proceso es el mismo para la copia de base de datos con latencia, excepto que la base de datos con latencia reproduce primero todos los archivos de registro necesarios para lograr un estado de revisión. 

## <a name="mailbox-replication-service"></a>Servicio de replicación de buzones 
Mover buzones es una parte clave de la administración de un servicio de correo electrónico a gran escala. Siempre hay tecnologías actualizadas y actualizaciones de hardware y versiones con las que tratar, por lo que tener un sistema robusto y con limitaciones que permita a nuestros ingenieros realizar este trabajo mientras mantienen el buzón de correo transparente para los usuarios (asegurándose de que permanezcan en línea durante todo el proceso) es clave y asegurarse de que el proceso se escala correctamente a medida que los buzones se hacen más grandes y grandes. 

El Exchange replicación de buzones de correo (MRS) es responsable de mover buzones entre bases de datos. Durante el movimiento, MRS realiza una comprobación de coherencia en todos los elementos del buzón. Si se encuentra un problema de coherencia, MRS corregirá el problema o omitirá los elementos dañados, eliminando así los daños del buzón. 

Dado que MRS es un componente de Exchange Online, podemos realizar cambios en su código para abordar nuevas formas de corrupción que se detectan en el futuro. Por ejemplo, si detectamos un problema de coherencia que MRS no puede corregir, podemos analizar los daños, cambiar el código MRS y corregir la incoherencia (si entendemos cómo hacerlo). 

## <a name="log-file-checks"></a>Comprobaciones de archivos de registro 
Todos los archivos de registro de transacciones generados Exchange base de datos se someten a varias formas de comprobaciones de coherencia. Cuando se crea un archivo de registro, lo primero que se hace es escribir un patrón de bits y, a continuación, se realiza una serie de escrituras de registro. Esta estructura permite a Exchange Online ejecutar una serie de comprobaciones (vaciado perdido, CRC y otras comprobaciones) para validar cada archivo de registro tal como se escribe y de nuevo a medida que se replica. 

## <a name="deployment-on-resilient-file-system"></a>Implementación en el sistema de archivos resistente 
Para ayudar a evitar que se produzcan daños en el nivel del sistema de archivos, Exchange Online se está implementando en particiones del Sistema de archivos resistentes (ReFS) para proporcionar capacidades de recuperación mejoradas. ReFS es un sistema de archivos en Windows Server 2012 y posteriores que está diseñado para ser más resistente frente a la corrupción de datos, maximizando así la integridad y la disponibilidad de los datos. En concreto, ReFS aporta mejoras en la forma en que se actualizan los metadatos, lo que ofrece una mejor protección para los datos y reduce los casos de corrupción de datos. También usa sumas de comprobación para comprobar la integridad de los datos de archivos y los metadatos, lo que garantiza que los datos dañados se encuentran y reparan fácilmente. 

Exchange Online aprovecha varias ventajas de ReFS: 
- Una mayor resistencia en la integridad de los datos significa menos incidentes de corrupción de datos. Reducir el número de incidentes de corrupción significa menos reediciones innecesarias de la base de datos. 
- Suma de comprobación que se ejecuta en metadatos que habilitan detecciones de casos de daños de forma más rápida y determinista, lo que nos permite corregir los daños en los datos de los clientes antes de que se produzcan errores grises en los volúmenes de datos.
- Diseñado para funcionar bien con conjuntos de datos grandes (petabytes y más grandes) sin impacto en el rendimiento
- Compatibilidad con otras características usadas por Exchange Online, como el cifrado de BitLocker. 

Exchange Online también se beneficia de otras características de ReFS: 
- **Integridad (integridad Secuencias):** ReFS almacena los datos de una manera que lo protege de muchos de los errores comunes que normalmente pueden causar la pérdida de datos. Microsoft 365 La búsqueda usa el Secuencias integridad para ayudar con la detección de daños en el disco temprano y las sumas de comprobación del contenido del archivo. La característica también reduce los incidentes de daños causados por "Escrituras rotas" (cuando una operación de escritura no se completa debido a cortes de energía, etc.). 
- **Disponibilidad (salvamento):** ReFS prioriza la disponibilidad de datos. Históricamente, los sistemas de archivos eran a menudo susceptibles a daños en los datos que requerirían que el sistema se desconectara para su reparación. Aunque es poco frecuente, si se producen daños, ReFS implementa el salvamento, una característica que quita los datos dañados del espacio de nombres en un volumen en directo y garantiza que los datos buenos no se ven afectados negativamente por datos dañados no reparables. La aplicación de la característica de recuperación y el aislamiento de daños de datos en volúmenes de base de datos Exchange Online significa que podemos mantener las bases de datos no afectadas en un volumen dañado en buen estado entre el momento de los daños y las acciones de reparación. Esta estructura aumenta la disponibilidad de bases de datos que normalmente se verían afectadas por estos problemas de daños en el disco. 
