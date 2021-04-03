---
title: Eliminación de datos de Microsoft 365 Exchange Online
description: Obtenga información sobre cómo se controlan en Exchange Online las eliminaciones de datos suaves y duros para buzones y elementos dentro de los buzones.
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
hideEdit: true
ms.openlocfilehash: c88e7359931fb964fbc4cb6531c5151072a50df0
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497197"
---
# <a name="exchange-online-data-deletion-in-microsoft-365"></a>Eliminación de datos de Exchange Online en Microsoft 365

Dentro de Exchange Online, hay dos tipos de eliminaciones: eliminaciones suaves y eliminaciones permanentes. Esto se aplica tanto a buzones como a elementos dentro de un buzón.

## <a name="soft-deleted-and-hard-deleted-mailboxes"></a>Buzones eliminados temporalmente y eliminados de forma permanente

Un buzón de usuario eliminado temporalmente es un buzón que se ha eliminado con el Centro de administración de Microsoft 365 o el cmdlet Remove-Mailbox y que todavía ha estado en la papelera de reciclaje de Azure Active Directory durante menos de 30 días. Un buzón puede eliminarse temporalmente de cualquiera de las siguientes maneras:

- La cuenta de usuario asociada del buzón de usuario de Azure Active Directory se elimina temporalmente (el objeto de usuario está fuera del ámbito o en el contenedor de la papelera de reciclaje).
- La cuenta de usuario de Azure Active Directory asociada al buzón de usuario se ha eliminado de forma permanente, pero el buzón de Exchange Online está bajo retención por juicio o retención de exhibición de documentos electrónicos.
- La cuenta de usuario de Azure Active Directory asociada al buzón de usuario se ha purgado en los últimos 30 días; que es la longitud máxima de retención que Exchange Online mantendrá el buzón en un estado eliminado temporalmente antes de que se purgue permanentemente y no se podrá recuperar.

Un buzón de usuario eliminado de forma permanente es un buzón que se ha eliminado de una de las siguientes maneras:

- El buzón de usuario se ha eliminado temporalmente durante más de 30 días y el usuario asociado de Azure Active Directory se ha eliminado de forma permanente. Todo el contenido del buzón, como correos electrónicos, contactos y archivos, se elimina permanentemente.
- La cuenta de usuario asociada al buzón de usuario se ha eliminado de forma permanente de Azure Active Directory. El buzón de usuario se elimina temporalmente en Exchange Online y permanece en un estado eliminado temporalmente durante 30 días. Si en el período de 30 días se sincroniza un nuevo usuario de Azure Active Directory desde la cuenta de destinatario original con el mismo **ExchangeGuid** o **ArchiveGuid,** y esa nueva cuenta tiene licencia para Exchange Online, esto provocará una eliminación permanente del buzón de usuario original. Todo el contenido del buzón, como correos electrónicos, contactos y archivos, se elimina permanentemente.
- Un buzón eliminado temporalmente se elimina **mediante Remove-Mailbox -PermanentlyDelete**.

Los escenarios de eliminación anteriores suponen que el buzón de usuario no está en ninguno de los estados de retención, como retención por juicio o retención de exhibición de documentos electrónicos. Si hay algún tipo de retención en el buzón, no se puede eliminar el buzón. Para todos los tipos de [](https://support.office.com/article/manage-legal-investigations-in-office-365-2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e?ui=en-US&rs=en-US&ad=US) destinatarios del usuario de correo, cualquier configuración de retención se omite y no tiene ningún efecto en eliminaciones duras o eliminaciones suaves.

## <a name="soft-deleted-and-hard-deleted-items"></a>Elementos eliminados temporalmente y eliminados de forma permanente

Cuando un usuario elimina un elemento de buzón (como un mensaje de correo electrónico, un contacto, una cita de calendario o una tarea), el elemento se mueve a la carpeta Elementos recuperables y a una subcarpeta denominada "Eliminaciones". Esto se conoce como eliminación suave. El tiempo que se mantienen los elementos eliminados en la carpeta Eliminaciones depende del período de retención de elementos eliminados configurado para el buzón. Un buzón de Exchange Online mantiene los elementos eliminados durante 14 días de forma predeterminada, pero los administradores de Exchange Online pueden cambiar esta configuración para aumentar el período hasta un máximo de 30 días. (Para obtener instrucciones detalladas para aumentar el período de retención de elementos eliminados para un buzón de Exchange Online, vea Cambiar cuánto tiempo se mantienen los elementos eliminados permanentemente para un buzón de [Exchange Online).](/exchange/recipients-in-exchange-online/manage-user-mailboxes/change-deleted-item-retention) Los usuarios pueden recuperar o purgar elementos eliminados antes de que expire el tiempo de retención de un elemento eliminado. Para ello, usan la característica Recuperar elementos eliminados en Microsoft Outlook o Outlook en la web.

Si un usuario purga un elemento eliminado mediante la característica Recuperar elementos eliminados en Outlook o Outlook en la web, esto se conoce como eliminación permanente. En Exchange Online, la recuperación de elementos únicos está habilitada [](/Exchange/recipients/user-mailboxes/recover-deleted-messages) de forma predeterminada cuando se crea un nuevo buzón de correo, por lo que un administrador aún puede recuperar elementos eliminados de forma permanente antes de que expire el período de retención de elementos eliminados. Además, si un usuario o un proceso modifican un mensaje, también se conservan copias del elemento original cuando se habilita la recuperación de un elemento único.

## <a name="page-zeroing"></a>Ceros de página

*El cero* es un mecanismo de seguridad que escribe ceros o un patrón binario sobre los datos eliminados para que los datos eliminados sea más difícil de recuperar. En Exchange Online, las bases de datos de buzones de correo usan *páginas* como su unidad de almacenamiento e implementan un proceso de sobrescritura denominado *cero de página*. El cero de página está habilitado de forma predeterminada y no pueden deshabilitarla los clientes ni Microsoft. Las operaciones de cero de página se registran en los archivos de registro de transacciones de modo que todas las copias de una base de datos determinada tienen ceros de página de forma similar. La puesta a cero de una página en una copia de base de datos activa hace que la página se cero en las copias pasivas de la base de datos.

El cero de página escribe un patrón binario sobre registros eliminados de forma permanente. El patrón de ceros de página es específico de las operaciones del Motor de almacenamiento extensible (ESE) (el nombre del motor de base de datos interno usado por los servidores de Exchange Online) y es diferente para las operaciones en tiempo de ejecución frente a las operaciones de mantenimiento de bases de datos en segundo plano. (El mantenimiento de bases de datos en segundo plano es un proceso que comprueba y examina continuamente cada base de datos. Su función principal es crear páginas de base de datos de suma de comprobación, pero también controla la limpieza del espacio y la puesta a cero de los registros y páginas que no se han reducido a cero debido a un bloqueo de la Tienda).

La siguiente tabla muestra una lista de las tramas de relleno que corresponden a operaciones de tiempo de ejecución específicas.

| Operación de tiempo de ejecución de ESE   | Trama de relleno |
|--------------------------|--------------|
| Reemplazar                  | R            |
| Eliminación de valor de registro/largo | D            |
| Espacio de página liberado         | H            |

La siguiente tabla muestra una lista de las tramas de relleno que corresponden a operaciones específicas que ocurren durante el mantenimiento de la base de datos de ESE en segundo plano.

| Operación de mantenimiento de base de datos de ESE en segundo plano | Trama de relleno |
|-----------------------------------------------|--------------|
| Eliminación de registro                                 | D            |
| Eliminación de valor largo                             | L            |
| Espacio de página liberado de página parcialmente usada       | Z            |
| Espacio de página liberado de página no utilizada               | U            |

### <a name="page-zeroing-process"></a>Proceso de ceros de página

El proceso de cero de página depende del escenario de eliminación. La siguiente tabla analiza los escenarios de eliminación de bases de datos y cuándo se produce el llenado con ceros de páginas.

| Escenario de eliminación de bases de datos | Proceso de ESE y datos de base de datos de período de tiempo a cero |
|:--------------------------|:------------------------------------------------|
| El elemento expira en función del período de retención de elementos eliminados. | Un subproceso asincrónico escribe un patrón binario sobre los datos eliminados. Esta acción se produce en milisegundos durante la eliminación de registro. Si el proceso de la Tienda se bloquea mientras el trabajo de cero asincrónico aún está pendiente (o la limpieza del almacén de versiones se cancela debido al crecimiento del almacén de versiones), el cero se completa cuando el mantenimiento de la base de datos en segundo plano procesa esa sección de la base de datos. |
| View Scenario: Expiration of items from Outlook/Outlook on the web folder view (for example, Conversation view) | El llenado con ceros de datos se produce cuando el mantenimiento de la base de datos en segundo plano procesa esa sección de la base de datos. |
| Mover buzón/Eliminar escenario de buzón: buzón de origen eliminado (expiración del buzón eliminado) | El llenado con ceros de datos se produce cuando el mantenimiento de la base de datos en segundo plano procesa esa sección de la base de datos. |

### <a name="mailbox-data-types-without-page-zeroing"></a>Tipos de datos de buzones sin ceros de página

Los siguientes tipos de datos de buzón de correo no tienen ninguna disposición para la puesta a cero de página:

- **Registros de transacciones** de base de datos de buzones de correo: cuando los registros de transacciones se eliminan como parte de las operaciones normales, no hay ningún proceso para cero los bloques del sistema de archivos que almacenaban los archivos de registro eliminados. Es probable que el sistema de archivos reutilice rápidamente ese espacio libre para los registros recién creados, pero no hay ninguna garantía de que esto suceda.
- **Archivos de catálogo de índices de** contenido: Exchange Online usa Search Foundation (también conocido como FAST) para la funcionalidad de indización de búsqueda. El catálogo de índices de búsqueda se compone de varias docenas de archivos almacenados en el mismo volumen que el archivo de base de datos de buzones de correo. Cuando se elimina de forma permanente un mensaje de la base de datos del buzón de correo, el contenido asociado al catálogo de búsqueda no se elimina de inmediato. La eliminación de contenido se produce cuando Search Foundation realiza una instantánea (o combinación maestra) de muchos archivos de catálogo pequeños en un único archivo más grande. Una vez finalizada la combinación maestra, se eliminan los archivos de catálogo más pequeños. No hay ningún proceso para cero los bloques que almacenaban los archivos de catálogo eliminados.

## <a name="continuous-replication"></a>Replicación continua

La replicación continua (también conocida como trasvase de registros y reproducción) es una tecnología de Exchange Online que crea y mantiene copias de todas las bases de datos de buzones de correo para proporcionar alta disponibilidad, resistencia de sitios y recuperación ante desastres. La replicación continua usa la Exchange Server de recuperación de bloqueo de base de datos para proporcionar tecnología que realiza la actualización asincrónica de una o más copias de una base de datos de buzones de correo. Cada servidor de buzones registra las actualizaciones de bases de datos realizadas en una base de datos activa (por ejemplo, actividad de correo electrónico de usuario) como registros de registro en un conjunto secuencial de archivos de registro de transacciones de 1 MB. Este conjunto de archivos se conoce como la secuencia de registro. En la replicación continua, la secuencia de registro también se usa para actualizar de forma asincrónica una o más copias de una base de datos. Para ello, transmita los registros a una ubicación que contenga una copia pasiva de la base de datos activa y, a continuación, reprodrázcalos en la copia pasiva de la base de datos. Si todos los registros de la base de datos activa se reproducen en una copia pasiva de la base de datos, las dos bases de datos son equivalentes y es a través de este proceso que cualquier cambio físico realizado en una base de datos activa se replica en todas las copias pasivas de esa base de datos.

Cualquier eliminación de una base de datos de buzones de correo, ya sea un elemento de buzón o un buzón completo, y si una eliminación suave o una eliminación permanente, representa un cambio físico en la base de datos activa. La creación de ceros de página también implica realizar cambios físicos en la base de datos activa. Estos cambios se escriben en los archivos de registro a través de un proceso denominado replicación continua y cuando esos archivos de registro se reproducen en copias pasivas de la base de datos, se realizan los mismos cambios físicos en esas bases de datos pasivas.
