---
title: Resistencia de datos de Exchange Online en Microsoft 365
description: En este artículo, encontrará una explicación de los diversos aspectos de la resistencia de datos en Exchange Online y Microsoft 365.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
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
ms.openlocfilehash: 2cdd37d34612421cc7a9e4687134e2a1e2b1aeec
ms.sourcegitcommit: b06fa9f1b230fd5e470817486ea51f460f28b691
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/27/2021
ms.locfileid: "50012947"
---
# <a name="exchange-online-data-resiliency-in-microsoft-365"></a>Resistencia de datos de Exchange Online en Microsoft 365

>[!IMPORTANT]
>A medida que seguimos invirtiendo en diferentes formas de conservar el contenido del buzón, anunciamos la retirada de las retenciones de In-Place en el Centro de administración de Exchange (EAC) en Exchange Online. A partir del 1 de julio de 2020, no podrá crear nuevas In-Place retenciones. Pero aún podrá administrar las retenciones de In-Place en el EAC o mediante el cmdlet **Set-MailboxSearch** en Exchange Online PowerShell. Sin embargo, a partir del 1 de octubre de 2020, no podrá administrar las In-Place locales. Solo podrá quitarlos en el EAC o con el cmdlet **Remove-MailboxSearch.** El In-Place las retenciones locales en Exchange Server e implementaciones híbridas de Exchange seguirá siendo compatible. Para obtener más información sobre la retirada de In-Place en Exchange Online, consulte Retirada de herramientas de exhibición de [documentos electrónicos heredadas.](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement)

Una conservación local conserva todo el contenido de un buzón de correo, incluidos los elementos eliminados y las versiones originales de los elementos modificados. Todos los elementos del buzón de correo se devuelven en una búsqueda de [Exhibición de documentos electrónicos en contexto](https://docs.microsoft.com/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery). Cuando se coloca una retención In-Place en el buzón de un usuario, el contenido del buzón de archivo correspondiente (si está habilitado) también se coloca en retención y se devuelve en una búsqueda de exhibición de documentos electrónicos.

Hay dos tipos de daños que pueden afectar a una base de datos de Exchange: daños físicos, que normalmente se deben a problemas de hardware (en particular, hardware de almacenamiento) y daños lógicos, que se producen debido a otros factores. Por lo general, hay dos tipos de daños lógicos que pueden producirse en una base de datos de Exchange:

- **Daños lógicos en la** base de datos: la suma de comprobación de la página de base de datos coincide, pero los datos de la página son incorrectos lógicamente. Esto puede ocurrir cuando el motor de base de datos (el motor de almacenamiento extensible (ESE)) intenta escribir una página de base de datos y, aunque el sistema operativo devuelve un mensaje de operación correcta, los datos nunca se escriben en el disco o se escriben en un lugar incorrecto. Esto se conoce como un vaciado *perdido.* ESE incluye numerosas características y protecciones diseñadas para evitar daños físicos en una base de datos y otros escenarios de pérdida de datos. Para evitar que los vaciados perdidos pierdan datos, ESE incluye un mecanismo de detección de vaciado perdido en la base de datos junto con una característica (restauración de página única) para corregirlo.
- **Almacenar daños lógicos:** los datos se agregan, eliminan o manipulan de forma que el usuario no espera. Estos casos son causados por aplicaciones de terceros. Suele ser un daño en el sentido de que el usuario lo ve como daños. El almacén de Exchange considera que la transacción que produce los daños de lógica es una serie de operaciones MAPI válidas. Las [características de](https://docs.microsoft.com/exchange/security-and-compliance/create-or-remove-in-place-holds) retención local de Exchange Online proporcionan protección contra daños lógicos en el almacén (ya que impide que un usuario o una aplicación eliminen permanentemente el contenido). 

Exchange Online realiza varias comprobaciones de coherencia en los archivos de registro replicados durante la inspección de registros y la reproducción de registros. Estas comprobaciones de coherencia impiden que el sistema replique los daños físicos. Por ejemplo, durante la inspección del registro, hay una comprobación de integridad física que comprueba el archivo de registro y valida que la suma de comprobación registrada en el archivo de registro coincide con la suma de comprobación generada en la memoria. Además, se examina el encabezado del archivo de registro para asegurarse de que la firma del archivo de registro registrada en el encabezado de registro coincide con la del archivo de registro. Durante la reproducción de registros, el archivo de registro se somete a un mayor examen. Por ejemplo, el encabezado de base de datos también contiene la firma de registro que se compara con la firma del archivo de registro para asegurarse de que coinciden. 

La protección contra los daños de los datos del buzón en Exchange Online se logra mediante Exchange Native Data Protection, una estrategia de resistencia que aprovecha la replicación en el nivel de aplicación en varios servidores y varios centros de datos, junto con otras características que ayudan a proteger los datos de pérdida debido a daños u otros motivos. Estas características incluyen características nativas administradas por Microsoft o la propia aplicación de Exchange Online, como:

- [Grupos de disponibilidad de datos](https://docs.microsoft.com/exchange/back-up-email)
- Corrección de bit único 
- Análisis de bases de datos en línea 
- Detección de vaciado perdido 
- Restauración de una sola página 
- Servicio de replicación de buzones 
- Comprobaciones de archivos de registro 
- Implementación en el sistema de archivos resistente 

Para obtener más información sobre las características nativas enumeradas anteriormente, seleccione los hipervínculos y vea lo siguiente para obtener información adicional y para obtener detalles sobre los elementos sin hipervínculos. Además de estas características nativas, Exchange Online también incluye características de resistencia de datos que los clientes pueden administrar, como: 
- [Recuperación de un solo elemento (habilitada de forma predeterminada)](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages) 
- [Conservación local y retención por juicio](https://docs.microsoft.com/exchange/security-and-compliance/in-place-and-litigation-holds) 
- [Retención de elementos eliminados y Soft-Deleted buzones de correo eliminados (ambos habilitados de forma predeterminada)](https://docs.microsoft.com/exchange/recipients-in-exchange-online/delete-or-restore-mailboxes) 

## <a name="database-availability-groups"></a>Grupos de disponibilidad de base de datos 
Todas las bases de datos de buzones de Microsoft 365 se hospedan en un grupo de disponibilidad de base de datos [(DAG)](https://docs.microsoft.com/exchange/back-up-email) y se replican en centros de datos separados geográficamente dentro de la misma región. La configuración más común son cuatro copias de bases de datos en cuatro centros de datos; sin embargo, algunas regiones tienen menos centros de datos (las bases de datos se replican en tres centros de datos en India y dos centros de datos en Australia y Japón). Pero, en todos los casos, cada base de datos de buzones de correo tiene cuatro copias que se distribuyen en varios centros de datos, lo que garantiza que los datos del buzón estén protegidos contra errores de software, hardware e incluso centros de datos. 

De estas cuatro copias, tres de ellas están configuradas como de alta disponibilidad. La cuarta copia se configura como [una copia de base de datos lateda.](https://docs.microsoft.com/Exchange/high-availability/manage-ha/activate-lagged-db-copies) La copia de base de datos con latencia no está pensada para la recuperación de buzones individuales o la recuperación de elementos de buzón. Su objetivo es proporcionar un mecanismo de recuperación para el raro evento de daños lógicos catastróficos en todo el sistema. 

Las copias de bases de datos con retraso en Exchange Online se configuran con un tiempo de retraso de reproducción de archivos de registro de siete días. Además, el Administrador de retrasos de reproducción de Exchange está habilitado para proporcionar la reproducción dinámica de archivos de registro para copias con retraso con el objeto de permitir que las copias de bases de datos con retrasos se puedan reparar automáticamente y administrar el crecimiento del archivo de registro. Aunque las copias de base de datos con latencia se usan en Exchange Online, es importante comprender que no son una copia de seguridad de un momento dado garantizada. Las copias de bases de datos con latencia en Exchange Online tienen un umbral de disponibilidad, normalmente en torno al 90 %, debido a períodos en los que el disco que contiene una copia con un tiempo de espera se pierde debido a un error en el disco, la copia latente se convierte en una copia de alta disponibilidad (debido a la reproducción automática), así como los períodos en los que la copia de base de datos latente está recompilando la cola de reproducción de registros. 

## <a name="transport-resilience"></a>Resistencia de transporte 
Exchange Online incluye dos características principales de resistencia de transporte: redundancia de instantáneas y red de seguridad. La redundancia de instantáneas mantiene una copia redundante de un mensaje mientras está en tránsito. La red de seguridad conserva una copia redundante de un mensaje después de entregarlo correctamente. 

Con la redundancia de instantáneas, cada servidor de transporte de Exchange Online realiza una copia de cada mensaje que recibe antes de confirmar que recibe correctamente el mensaje al servidor de envío. Esto hace que todos los mensajes de la canalización de transporte sea redundante mientras están en tránsito. Si Exchange Online determina que el mensaje original se perdió en tránsito, se reenvía una copia redundante del mensaje. 

La red de seguridad es una cola de transporte asociada con el servicio de transporte en un servidor de buzones de correo. Esta cola almacena copias de mensajes correctamente procesados por el servidor. Cuando un error de servidor o base de datos de buzones de correo requiere activar una copia no actualizada de la base de datos de buzones de correo, los mensajes de la cola de red de seguridad se reenvíen automáticamente a la nueva copia activa de la base de datos de buzones de correo. La red de seguridad también es redundante, lo que elimina el transporte como un único punto de error. Usa el concepto de una red de seguridad principal y una red de seguridad de instantáneas donde si la red de seguridad principal no está disponible durante más de 12 horas, las solicitudes de reenvío se convierten en solicitudes de reenvío de instantáneas y los mensajes se vuelven a entregar desde la red de seguridad de instantáneas.

Los reenvíos de mensajes desde la red de seguridad se inician automáticamente mediante el componente de Active Manager del servicio de replicación de Microsoft Exchange que administra dag y copias de bases de datos de buzones de correo. No se requiere ninguna acción manual para reenviar mensajes desde la red de seguridad. 

## <a name="single-bit-correction"></a>Corrección de un solo bit 
ESE incluye un mecanismo para detectar y resolver errores CRC de un solo bit (también conocidos como volteos de un solo bit) que son el resultado de errores de hardware (y, por lo tanto, representan daños físicos). Cuando se producen estos errores, ESE los corrige automáticamente y registra un evento en el registro de eventos. 

## <a name="online-database-scanning"></a>Análisis de bases de datos en línea 
El análisis de bases de datos en línea (también conocido como suma de comprobación de base de *datos)* es el proceso en el que un ESE usa un herramienta de comprobación de coherencia de base de datos para leer cada página y comprobar si hay daños en la página. El propósito principal es detectar daños físicos y vaciados perdidos que pueden no ser detectados por operaciones transaccionales. El análisis de la base de datos también realiza operaciones de bloqueo posteriores al almacenamiento. El espacio se puede perder debido a bloqueos y el análisis de bases de datos en línea busca y recupera espacio perdido. El sistema está diseñado con la expectativa de que cada base de datos se examina completamente una vez cada siete días. 

## <a name="lost-flush-detection"></a>Detección de vaciado perdido 
Un vaciado perdido se produce cuando una operación de escritura de base de datos que el sistema operativo o subsistema de disco devuelto como completado no se escribió realmente en el disco o se escribió en la ubicación incorrecta. Los incidentes de vaciado perdidos pueden causar daños lógicos en la base de datos, por lo que para evitar que los vaciados perdidos se pierdan datos, ESE incluye un mecanismo de detección de vaciado perdido. A medida que las páginas de base de datos se escriben en copias pasivas, se realiza una comprobación de los vaciados perdidos en la copia activa. Si se detecta un vaciado perdido, ESE puede reparar el proceso mediante un proceso de revisión de página. 

## <a name="single-page-restore"></a>Restauración de página única 
La restauración de una sola página, también conocida como revisión de *página,* es un proceso automático en el que las páginas de base de datos dañadas se reemplazan por copias en buen estado de una réplica en buen estado. El proceso de reparación de una página dañada depende de si la copia de base de datos está activa o pasiva. Cuando una copia de base de datos activa encuentra una página dañada, puede copiar una página de una de sus réplicas, siempre que la página que copia esté actualizada. Este proceso se realiza colocando una solicitud de la página en la secuencia de registro, que es la base de la replicación de bases de datos de buzones de correo. Tan pronto como una réplica encuentra la solicitud de página, responde enviando una copia de la página a la copia de base de datos solicitante. La restauración de una sola página también proporciona un mecanismo de comunicación asincrónico para que el activo solicite una página a las réplicas, incluso si las réplicas están actualmente sin conexión. 

En caso de daños en una copia de base de datos pasiva, incluida una copia de base de datos atrasada, dado que estas copias están siempre detrás de su copia activa, siempre es seguro copiar cualquier página de la copia activa a una copia pasiva. Por naturaleza, una copia de base de datos pasiva está altamente disponible, por lo que durante el proceso de revisión de página, la reproducción de registros se suspende, pero la copia de registros continúa. La copia pasiva de base de datos recupera una copia de la página dañada de la copia activa, espera hasta que se copia e inspecciona el archivo de registro que cumple el requisito máximo de generación de registros necesario y, a continuación, revisa la página dañada. Una vez que se ha parcheado la página, se reanuda la reproducción de registros. El proceso es el mismo para la copia de base de datos lateda, excepto en que la base de datos lateda reproduce primero todos los archivos de registro necesarios para lograr un estado de revisión. 

## <a name="mailbox-replication-service"></a>Servicio de replicación de buzones 
Mover buzones es una parte clave de la administración de un servicio de correo electrónico a gran escala. Siempre hay tecnologías actualizadas y actualizaciones de hardware y versiones con las que tratar, por lo que tener un sistema robusto y con limitaciones que permita a nuestros ingenieros realizar este trabajo a la vez que mantiene el buzón de correo transparente para los usuarios (asegurándose de que permanezcan en línea durante todo el proceso) es clave y asegurarse de que el proceso se escala correctamente a medida que los buzones se hacen más grandes y grandes. 

El servicio de replicación de buzones de Exchange (MRS) es responsable de mover buzones entre bases de datos. Durante el movimiento, MRS realiza una comprobación de coherencia en todos los elementos del buzón. Si se encuentra un problema de coherencia, MRS corregirá el problema o omitirá los elementos dañados, lo que elimina los daños del buzón. 

Dado que MRS es un componente de Exchange Online, podemos realizar cambios en su código para solucionar los nuevos tipos de daños que se detectan en el futuro. Por ejemplo, si detectamos un problema de coherencia que MRS no puede corregir, podemos analizar los daños, cambiar el código MRS y corregir la incoherencia (si sabemos cómo hacerlo). 

## <a name="log-file-checks"></a>Comprobaciones de archivos de registro 
Todos los archivos de registro de transacciones generados por una base de datos de Exchange se someten a varias formas de comprobaciones de coherencia. Cuando se crea un archivo de registro, lo primero que se hace es escribir un patrón de bits y, a continuación, se realiza una serie de escrituras de registro. Esta estructura permite a Exchange Online ejecutar una serie de comprobaciones (vaciado perdido, CRC y otras comprobaciones) para validar cada archivo de registro mientras se escribe y de nuevo a medida que se replica. 

## <a name="deployment-on-resilient-file-system"></a>Implementación en el sistema de archivos resistente 
Para ayudar a evitar que se produzcan daños en el nivel del sistema de archivos, Exchange Online se implementa en particiones del Sistema de archivos resistente (ReFS) para proporcionar capacidades de recuperación mejoradas. ReFS es un sistema de archivos de Windows Server 2012 y versiones posteriores que está diseñado para ser más resistente frente a daños en los datos, maximizando así la integridad y la disponibilidad de los datos. En concreto, ReFS aporta mejoras en la forma en que se actualizan los metadatos, lo que ofrece una mejor protección para los datos y reduce los casos de daños en los datos. También usa sumas de comprobación para comprobar la integridad de los datos de archivo y los metadatos, lo que garantiza que los datos dañados se puedan encontrar y reparar fácilmente. 

Exchange Online aprovecha varias ventajas de ReFS: 
- Una mayor resistencia en la integridad de datos significa menos incidentes de daños en los datos. Reducir el número de incidentes de daños significa menos reedecciones innecesarias de la base de datos. 
- Suma de comprobación que se ejecuta en metadatos, lo que permite detecciones de casos de daños de forma más rápida y determinista, lo que nos permite corregir los daños en los datos de los clientes antes de que se produzcan errores grises en los volúmenes de datos.
- Diseñado para funcionar bien con grandes conjuntos de datos (petabytes y más grandes) sin impacto en el rendimiento
- Compatibilidad con otras características usadas por Exchange Online, como el cifrado de BitLocker. 

Exchange Online también se beneficia de otras características de ReFS: 
- **Integridad (secuencias** de integridad): ReFS almacena datos de manera que los protege de muchos de los errores comunes que normalmente pueden causar la pérdida de datos. Búsqueda de Microsoft 365 usa secuencias de integridad para ayudar con la detección temprana de daños en el disco y sumas de comprobación del contenido del archivo. La característica también reduce los incidentes de daños causados por "Rasgar escrituras" (cuando una operación de escritura no se completa debido a cortes en la alimentación, etc.). 
- **Disponibilidad (Recuperación):** ReFS prioriza la disponibilidad de los datos. Históricamente, los sistemas de archivos eran a menudo susceptibles a daños en los datos que requerirían que el sistema se desconectara para su reparación. Aunque rara vez, si se producen daños, ReFS implementa la recuperación, una característica que quita los datos dañados del espacio de nombres en un volumen en directo y garantiza que los datos correctos no se ven afectados negativamente por datos dañados no reparables. Aplicar la característica de recuperación y aislar los daños en los datos en los volúmenes de bases de datos de Exchange Online significa que podemos mantener las bases de datos no afectadas en un volumen dañado en buen estado entre el momento de los daños y la acción de reparación. Esta estructura aumenta la disponibilidad de las bases de datos que normalmente se verían afectadas por estos problemas de daños en el disco. 
