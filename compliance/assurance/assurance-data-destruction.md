---
title: Destrucción de datos en Microsoft 365
description: Información general sobre las directivas de Microsoft sobre reciclaje, eliminación o destrucción de Microsoft 365 unidades de disco y servidores del centro de datos.
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 229221d9cba2d7cc92e99086d647071556dae9e3
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482133"
---
# <a name="data-destruction-in-microsoft-365"></a>Destrucción de datos en Microsoft 365

## <a name="physical-data-destruction"></a>Destrucción de datos físicos

Microsoft tiene directivas estándar de tratamiento de datos que abordan el reciclaje y eliminación de unidades de disco y servidores con errores o retiradas. Antes de volver Microsoft 365 uso de las unidades de disco de Microsoft 365, Microsoft realiza un proceso de desinfección física coherente con la Publicación especial del Instituto Nacional de Estándares y Tecnología 800-88 ([Nist SP 800-88 Guidelines for Media Sanitization](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf)). Dado que todas las unidades de disco de Microsoft 365 se cifran mediante el cifrado de nivel de volumen de BitLocker, la eliminación compatible con NIST SP 800-88 no es técnicamente necesaria. No obstante, Microsoft realiza este proceso.

Los discos con errores usados Microsoft 365 centros de datos se destruyen físicamente y se auditan a través del proceso ISO. El tipo de activo determina los medios de eliminación adecuados. Para los discos duros que no se pueden borrar, Microsoft usa un proceso de destrucción para destruir los medios y hacer imposible la recuperación de información. Por ejemplo, los discos se destruyen físicamente, se pulverizan o se incineran. Microsoft conserva todos los registros de la destrucción y realiza un proceso de desinfección similar en servidores reutilizados en Microsoft 365. Estas directrices abarcan la desinfección electrónica y física.

Cada centro de datos usa un proceso de destrucción física en el sitio para eliminar sus discos. Los contenedores seguros para los medios de almacenamiento designados para la eliminación de discos están en cada área del centro de datos. Cada estación de ubicación segura tiene supervisión de vídeo. Una vez que una papelera de eliminación alcanza aproximadamente el 50 % de capacidad, el equipo de Servicios del sitio se pone en contacto con el equipo de seguridad física para coordinar la eliminación. El personal de Servicios de sitio y un administrador Office quitar la papelera de eliminación segura y colocarla en un área de almacenamiento protegida designada. Las directivas y procedimientos que rigen el tratamiento de los dispositivos portadores de datos durante la eliminación se prueban de forma rutinaria, incluidos los procedimientos para garantizar la condición de las máquinas aprobadas para su destrucción.

En el proceso de destrucción de datos, los discos se borran de forma compatible con NIST 800-88 (si es posible) y, a continuación, se colocan en una trituradora industrial y se destruyen físicamente. Microsoft mantiene la responsabilidad de los activos que salen del centro de datos con nist SP 800-88 limpieza y depuración coherentes, destrucción de activos, cifrado, inventario preciso, seguimiento y protección de la cadena de custodia durante el transporte. Este proceso se supervisa a través de un circuito cerrado de televisión y se emite un certificado de destrucción una vez completado.

Microsoft usa unidades de eliminación de datos de [Extreme Protocol Solutions](https://www.enterprisedataerasure.com/) (EPS). El software EPS admite los requisitos de NIST SP 800-88 para limpieza, purga y eliminación segura. Antes de limpiar o destruir, el administrador de activos de Microsoft crea un inventario. Si se usa un proveedor para la destrucción, el proveedor proporciona un certificado de destrucción para cada activo destruido, que es validado por el administrador de activos.

## <a name="virtual-data-destruction"></a>Destrucción de datos virtuales

Microsoft tiene directivas y procedimientos de tratamiento de datos que abordan la destrucción virtual eficaz de datos para protegerse contra la posibilidad de que los datos se compartan de forma inadecuada entre inquilinos de servicio o que se pueda acceder a ellos después de eliminarlos de forma permanente en el servicio. Los datos eliminados del servicio en un inquilino no son accesibles para otro inquilino de servicio, incluso si se reasigna cualquiera de los almacenamientos físicos subyacentes. Este es un resultado de los efectos compuestos de varias tecnologías de virtualización y fragmentación usadas para escalar entornos virtuales, los comportamientos de eliminación activa de las aplicaciones dentro de cada inquilino de servicio (como la eliminación de ceros de [página)](/office365/securitycompliance/office-365-exchange-online-data-deletion#page-zeroing)y los procesos de cifrado de contenido de aplicaciones y medios necesarios.