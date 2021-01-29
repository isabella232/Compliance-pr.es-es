---
title: Resistencia de datos de SharePoint y OneDrive en Microsoft 365
description: En este artículo se proporciona información general sobre la resistencia de datos de SharePoint y OneDrive en Microsoft 365.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: c940b778681805a1e50a9e565117cd67deb52566
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040390"
---
# <a name="sharepoint-and-onedrive-data-resiliency-in-microsoft-365"></a>Resistencia de datos de SharePoint y OneDrive en Microsoft 365

Dentro de Microsoft 365, OneDrive se basa en la plataforma de archivos de SharePoint. En este artículo, solo se usará SharePoint para hacer referencia a ambos productos. El contenido de este artículo es relevante para Microsoft 365 y no se aplica a los servicios al consumidor.

Hay dos activos principales que son el almacenamiento de contenido principal de SharePoint:

- **Metadatos:** los metadatos sobre cada archivo se almacenan en azure SQL base de datos. Azure SQL ofrece una historia completa de continuidad empresarial que SharePoint usa y los detalles se tratan más adelante en este artículo.
- **Almacenamiento de blobs:** el contenido del usuario que se carga en SharePoint se almacena en Azure Storage. SharePoint ha creado un plan de resistencia personalizado sobre Azure Storage para garantizar la duplicación casi en tiempo real del contenido de los usuarios y un sistema realmente activo/activo.

El conjunto completo de controles para garantizar la resistencia de datos se explica en secciones adicionales.

## <a name="blob-storage-resilience"></a>Resistencia de almacenamiento de blobs

SharePoint tiene una solución personalizada para el almacenamiento de datos de clientes en Azure Storage. Cada archivo se escribe simultáneamente en una región de centro de datos principal y secundario. Si se producirá un error en las escrituras en cualquiera de las regiones de Azure, se producirá un error al guardar el archivo. Después de escribir el contenido en Azure Storage, las sumas de comprobación se almacenan por separado con metadatos y se usan para garantizar que la escritura confirmada sea idéntica al archivo original enviado a SharePoint durante todas las lecturas futuras. Esta misma técnica se usa en todos los flujos de trabajo para evitar la propagación de los daños que deberían producirse. Dentro de cada región, Azure Locally Redundant Storage (LRS) proporciona un alto nivel de confiabilidad. Consulte el [artículo de redundancia de Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-redundancy-lrs) para obtener más información.

SharePoint usa Append-Only almacenamiento. Este proceso garantiza que los archivos no se puedan cambiar ni dañar después de un guardado inicial, pero también mediante el control de versiones del producto, se puede recuperar cualquier versión anterior del contenido del archivo.

Los entornos de SharePoint en cualquiera de los centros de datos pueden tener acceso a contenedores de almacenamiento en ambas regiones de Azure. Por motivos de rendimiento, siempre se prefiere el contenedor de almacenamiento en el mismo centro de datos local, pero las solicitudes de lectura que no ven resultados dentro del umbral deseado tendrán el mismo contenido solicitado desde el centro de datos remoto para garantizar que los datos estén siempre disponibles.

## <a name="metadata-resilience"></a>Resistencia de metadatos

Los metadatos de SharePoint también son fundamentales para obtener acceso al contenido del usuario, ya que almacenan la ubicación y las claves de acceso al contenido almacenado en Azure Storage. Estas bases de datos se almacenan en Azure SQL, que tiene un amplio [plan de continuidad empresarial.](https://docs.microsoft.com/azure/sql-database/sql-database-business-continuity)

SharePoint usa el modelo de replicación proporcionado por Azure SQL y ha creado una tecnología de automatización propietaria para determinar que se requiere una conmutación por error e iniciar la operación si es necesario. Por lo tanto, entra en la categoría "Conmutación por error manual de la base de datos" desde una perspectiva SQL Azure. Las métricas más recientes para la recuperación SQL base de datos de Azure están disponibles [aquí.](https://docs.microsoft.com/azure/azure-sql/database/business-continuity-high-availability-disaster-recover-hadr-overview#recover-a-database-to-the-existing-server)

SharePoint usa el sistema de copia de SQL de Azure para habilitar las restauraciones de punto en tiempo (PITR) durante un máximo de 14 días. PITR se trata más adelante [en una sección.](#deletion-backup-and-point-in-time-restore)

## <a name="automated-failover"></a>Conmutación por error automatizada

SharePoint usa una conmutación por error automatizada integrada personalizada para minimizar el impacto en la experiencia del cliente cuando se produce un evento específico de la ubicación. La automatización controlada por supervisión que detecta un error de uno o varios componentes más allá de determinados umbrales hará que la actividad de todos los usuarios salga del entorno problemático y se desenlace a un segundo nivel. Una conmutación por error da como resultado que los metadatos y el almacenamiento de cálculo se atendidas completamente fuera del nuevo centro de datos. Como el almacenamiento de blobs siempre se ejecuta completamente activo/activo, no se requiere ningún cambio para una conmutación por error. El nivel de proceso prefiere el contenedor de blobs más cercano, pero usará las ubicaciones locales y remotas de almacenamiento de blobs en cualquier momento para garantizar la disponibilidad.

SharePoint usa el servicio front-door de Azure para proporcionar enrutamiento interno a la red de Microsoft. Esta configuración permite el redireccionamiento de conmutación por error independiente de DNS y reduce el efecto del almacenamiento en caché del equipo local. La mayoría de las operaciones de conmutación por error son transparentes para los usuarios finales. Si hay una conmutación por error, los clientes no tendrán que realizar cambios para mantener el acceso al servicio.

## <a name="versioning-and-files-restore"></a>Control de versiones y restauración de archivos

Para las bibliotecas de documentos recién creadas, SharePoint tiene un valor predeterminado de 500 versiones en cada archivo y se puede configurar para conservar más versiones si lo desea. La interfaz de usuario no permite establecer un valor inferior a 100 versiones, pero es posible establecer el sistema para almacenar menos versiones mediante API públicas. Por motivos de confiabilidad, no se recomienda cualquier valor inferior a 100 y puede provocar que la actividad del usuario cause una pérdida de datos involuntaria.

Para obtener más información acerca del control de versiones, vea [Control de versiones en SharePoint.](https://docs.microsoft.com/microsoft-365/community/versioning-basics-best-practices)

La restauración de archivos es la capacidad de volver "atrás en el tiempo" en cualquier biblioteca de documentos de SharePoint a cualquier segundo de tiempo en los últimos 30 días. Este proceso se puede usar para recuperarse de ransomware, eliminaciones masivas, daños o cualquier otro evento. Esta característica usa versiones de archivo, por lo que reducir las versiones predeterminadas puede reducir la eficacia de esta restauración.

La característica de restauración de archivos está documentada para [OneDrive](https://support.office.com/article/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15) y [SharePoint.](https://support.office.com/article/Restore-a-document-library-317791c3-8bd0-4dfd-8254-3ca90883d39a)

## <a name="deletion-backup-and-point-in-time-restore"></a>Eliminación, copia de seguridad y restauración de punto en tiempo

El contenido de usuario eliminado de SharePoint pasa por el siguiente flujo de eliminación.

Los elementos eliminados se conservan en las papeleras de reciclaje durante un período de tiempo determinado. Para SharePoint, el tiempo de retención es de 93 días. Comienza cuando se elimina el elemento de su ubicación original. Cuando se elimina el elemento de la papelera de reciclaje del sitio, éste se incluye en la papelera de reciclaje [de la colección de sitios.](https://support.office.com/article/restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b) Permanece allí durante el resto de los 93 días y, a continuación, se elimina permanentemente. Encontrará más información sobre cómo usar la papelera de reciclaje en estos vínculos:

- [Restaurar elementos de la papelera de reciclaje](https://support.office.com/article/Restore-items-in-the-Recycle-Bin-of-a-SharePoint-site-6df466b6-55f2-4898-8d6e-c0dff851a0be)
- [Restaure los elementos eliminados de la papelera de reciclaje de la colección de sitios.](https://support.office.com/article/Restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b)

Este proceso es el flujo de eliminación predeterminado y no tiene en cuenta las directivas o etiquetas de retención. Para obtener más información, vea [Más información sobre la retención para SharePoint y OneDrive.](https://docs.microsoft.com/microsoft-365/compliance/retention-policies-sharepoint)

Una vez completada la canalización de reciclaje de 93 días, la eliminación se realiza de forma independiente para metadatos y almacenamiento de blobs. Los metadatos se quitarán inmediatamente de la base de datos, lo que hace que el contenido sea ilegible a menos que los metadatos se restauren a partir de la copia de seguridad. SharePoint mantiene copias de seguridad de metadatos durante 14 días. Estas copias de seguridad se toman localmente casi en tiempo real [](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups) y, a continuación, se insertan en el almacenamiento en contenedores redundantes de Azure Storage, según la documentación en el momento de esta publicación, una programación de 5 a 10 minutos.

Al eliminar el contenido de Blob Storage, SharePoint usa la característica de eliminación de software de Azure Blob Storage para protegerse contra la eliminación accidental o malintencionada. Con esta característica, tenemos un total de 14 días para restaurar el contenido antes de que se elimine de forma permanente.

>[!Note]
>Aunque las aplicaciones microsoft enviarán contenido a la papelera de reciclaje para el proceso estándar, SharePoint proporciona API que permiten omitir la papelera de reciclaje y forzar una eliminación inmediata. Revise las aplicaciones para asegurarse de que esto solo se realiza cuando sea necesario por motivos de cumplimiento.

## <a name="integrity-checks"></a>Comprobaciones de integridad

SharePoint usa varios métodos para garantizar la integridad de blobs y metadatos en todas las etapas del ciclo de vida de los datos:

- **Hash de archivo almacenado en metadatos:** el hash de todo el archivo se almacena con metadatos de archivo para garantizar que la integridad de los datos del nivel del documento se mantiene durante todas las operaciones.
- **Hash de blob almacenado en metadatos:** cada elemento blob almacena un hash del contenido cifrado para protegerse contra daños en el almacenamiento de Azure subyacente.
- **Trabajo de** integridad de datos: cada 14 días, cada sitio se examina para buscar integridad mediante la lista de elementos de la base de datos y la coincidencia con los blobs enumerados en Azure Storage. El trabajo notifica los blobs que faltan en las referencias a blobs y puede recuperar esos blobs a través de la característica de eliminación de forma flexible de [Azure Storage](https://docs.microsoft.com/azure/storage/blobs/soft-delete-blob-overview) si es necesario.
