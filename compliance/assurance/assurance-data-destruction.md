---
title: Destrucción de datos en Microsoft 365
description: Información general sobre las directivas de Microsoft sobre el reciclaje, la eliminación o la destrucción de unidades de disco y servidores del centro de datos de Microsoft 365.
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
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: d97c5f1be6bf09a772244aac14086171643af89e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120679"
---
# <a name="data-destruction-in-microsoft-365"></a>Destrucción de datos en Microsoft 365

## <a name="physical-data-destruction"></a>Destrucción de datos físicos

Microsoft tiene directivas estándar de control de datos que abordan el reciclaje y la eliminación de unidades de disco y servidores con errores o retiradas. Antes de volver a uso de las unidades de disco de Microsoft 365, Microsoft realiza un proceso de saneo físico coherente con la publicación especial 800-88 del Instituto Nacional de Estándares y Tecnología[(NIST SP 800-88 Guidelines for Media Sanitization](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf)). Dado que todas las unidades de disco de Microsoft 365 se cifran mediante el cifrado de nivel de volumen de BitLocker, la eliminación compatible con NIST SP 800-88 no es técnicamente necesaria. No obstante, Microsoft realiza este proceso.

Los discos con errores usados en centros de datos de Microsoft 365 se destruyen físicamente y se auditan a través del proceso ISO. El tipo de activo determina los medios de eliminación adecuados. Para las unidades de disco duro que no se pueden borrar, Microsoft usa un proceso de destrucción para destruir los medios y hacer imposible la recuperación de información. Por ejemplo, los discos se destruyen físicamente, se destruyen o se desanudan. Microsoft conserva todos los registros de la destrucción y realiza un proceso de desinfección similar en los servidores reutilizados en Microsoft 365. Estas directrices abarcan la desinfección electrónica y física.

Cada centro de datos usa un proceso de destrucción física en el sitio para eliminar sus discos. Los contenedores seguros para los medios de almacenamiento designados para la eliminación de discos están en cada área del centro de datos. Cada estación de bandeja segura tiene vigilancia de supervisión de vídeo. Una vez que un contenedor de eliminación alcanza aproximadamente el 50 % de su capacidad, el equipo de Servicios del sitio se pone en contacto con el equipo de seguridad física para coordinar la eliminación. El personal de servicios del sitio y una oficina de seguridad quitan la papelera de eliminación segura y la colocan en un área de almacenamiento protegida designada. Las directivas y procedimientos que rigen el tratamiento de dispositivos de transporte de datos durante la eliminación se prueban de forma rutinaria, incluidos los procedimientos para garantizar la condición de organismo aprobado para su destrucción.

En el proceso de destrucción de datos, los discos se borran de una manera conforme a NIST 800-88 (si es posible) y, a continuación, se colocan en una ralenilla industrial y físicamente. Microsoft mantiene la responsabilidad de los activos que salen del centro de datos mediante la limpieza y depuración coherentes de NIST SP 800-88, la destrucción de activos, el cifrado, el inventario preciso, el seguimiento y la protección de la cadena de limpieza durante el transporte. Este proceso se supervisa a través de la televisión de circuito cerrado y se emite un certificado de destrucción una vez completado.

Microsoft usa unidades de eliminación de datos de [Soluciones de protocolo extremo](https://www.enterprisedataerasure.com/) (EPS). El software EPS admite los requisitos de NIST SP 800-88 para limpieza, depuración y eliminación de seguridad. Antes de la limpieza o destrucción, el administrador de activos de Microsoft crea un inventario. Si se usa un proveedor para la destrucción, el proveedor proporciona un certificado de destrucción para cada activo que se destruye, validado por el administrador de activos.

## <a name="virtual-data-destruction"></a>Destrucción de datos virtuales

Microsoft tiene directivas y procedimientos de tratamiento de datos que abordan la destrucción virtual eficaz de datos para protegerse contra la posibilidad de que los datos se compartan de forma inadecuada entre inquilinos de servicio o que se pueda acceder a ellos después de una eliminación permanente en el servicio. Los datos eliminados del servicio en un inquilino no son accesibles para otro inquilino de servicio, incluso si se reasigna alguno de los almacenamientos físicos subyacentes. Esto es un resultado de los efectos compuestos de varias tecnologías de virtualización y fragmentación usadas para escalar entornos virtuales, los comportamientos de eliminación activos de las aplicaciones dentro de cada inquilino de servicio (como el [zeroing](/office365/securitycompliance/office-365-exchange-online-data-deletion#page-zeroing)de páginas) y los procesos de cifrado de contenido de aplicaciones y medios necesarios.