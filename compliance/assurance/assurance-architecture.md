---
title: Introducción a la arquitectura
description: Obtenga información sobre la arquitectura de Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 7ceceb59d0afcbc72fac9758f3de500082b8b365
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/30/2020
ms.locfileid: "49509792"
---
# <a name="architecture-overview"></a>Introducción a la arquitectura

## <a name="what-is-microsoft-365"></a>¿Qué es Microsoft 365?

Microsoft 365 es la versión basada en la suscripción de Office, Windows 10, Enterprise Mobility + Security y el cumplimiento de la suscripción. Los clientes de Microsoft 365 obtienen clientes como Outlook y Windows, y también se benefician de los servicios que hospeda Microsoft en su nombre, como Exchange Online, Microsoft Teams y SharePoint Online. Todos los componentes del servicio se actualizan con regularidad como parte del modelo de suscripción, de modo que nuestros clientes tengan un producto de "perenne". Microsoft administra la infraestructura del servicio en nombre de los clientes, lo que significa que Microsoft es responsable de proteger la infraestructura que almacena los datos de los clientes.

En términos de escala, actualmente usamos cerca de un millón de máquinas para potenciar los servicios 365 de Microsoft. La infraestructura que enciende estos servicios varía en función del hardware específico del servicio y de los entornos virtualizados de Azure, Windows y Linux, y de las plataformas multiinquilino y dedicadas. Microsoft 365 es un negocio global y nuestra infraestructura se distribuye en centros de datos de todo el mundo, lo que permite a nuestros clientes cumplir con los requisitos de la residencia de datos y de la soberanía.

En Resumen, el servicio es complejo, se ejecuta a una escala increíble y requiere miles de ingenieros de Microsoft para su creación y mantenimiento. Es nuestra principal prioridad para mantener la seguridad de toda la infraestructura.

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>¿Cómo garantiza Microsoft 365 el aislamiento entre los inquilinos de cliente?

Los servicios en la nube de Microsoft se basan en la hipótesis de que todos los inquilinos son potencialmente hostiles para todos los demás inquilinos. Para aislar los inquilinos correctamente entre sí, Microsoft implementa una variedad de tecnologías de aislamiento y controles. Estos controles están diseñados para protegerse contra la filtración de información o el acceso no autorizado a los datos de los clientes entre los inquilinos y para evitar que las acciones de un inquilino afecten negativamente al servicio para otro espacio empresarial.

El contenido del cliente se aísla lógicamente en los inquilinos de Microsoft 365 mediante Azure Active Directory (Azure AD). La autenticación de usuarios en Microsoft 365 comprueba no solo la identidad del usuario, sino también la identidad del inquilino de la que forma parte la cuenta de usuario, lo que impide que los usuarios obtengan acceso a datos fuera del entorno del espacio empresarial. Para complementar el aislamiento lógico de Azure AD, el contenido del cliente siempre se cifra en reposo y en tránsito. Los servicios individuales también pueden proporcionar otros niveles de aislamiento de inquilino, como el aislamiento de SharePoint Online de los datos de inquilinos en bases de datos cifradas independientes.

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>¿Cómo se aplican los servicios resistentes de ingeniería de Microsoft 365 que evitan puntos de error únicos?

Microsoft diseña y crea servicios en la nube para maximizar la confiabilidad y minimizar los efectos negativos en los clientes frente a errores y desafíos de las operaciones normales. Esta estrategia comienza con el diseño de la red que conecta nuestros centros de recursos distribuidos geográficamente. La arquitectura de red de Microsoft incluye interconexiones directas y varias rutas de red. Los servicios de Microsoft 365 aprovechan esta redundancia para enrutar automáticamente el tráfico en torno a los errores para mejorar la calidad del servicio.

En el nivel de servicio, la estrategia de resistencia de Microsoft 365 prioriza la resistencia del software. Siempre que sea posible, nuestros servicios se implementan en configuraciones activas/activas con la supervisión automatizada del estado del servicio, lo que permite que el servicio detecte y recupere de muchos errores y fallos comunes sin intervención humana. Además de las configuraciones activo/activo, los servicios de Microsoft 365 aumentan la tolerancia a errores al garantizar que el servicio se implementa en zonas de errores independientes, lo que evita que un error en una zona afecte a la disponibilidad de otras zonas.

La resistencia de los datos complementa la resistencia del servicio al proteger la integridad y la disponibilidad de los datos en los servicios de 365 de Microsoft. Nuestros servicios usan redundancia de almacenamiento local y redundancia geográfica para replicar copias de los datos de clientes en diferentes zonas defectuosas. Si los datos están dañados o se pierden en una zona de errores, se puede tener acceso a ellos en otra zona de errores sin que se pierda la disponibilidad. La comprobación de integridad automatizada restaura automáticamente los datos que se ven afectados por muchos tipos de daños físicos o lógicos. Microsoft 365 también proporciona a los clientes herramientas para restaurar los datos eliminados accidentalmente o modificados por el cliente en Exchange Online y SharePoint Online.

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>¿Cómo realiza el seguimiento de dependencias de Microsoft 365 y se evitan las conexiones de sistema externo no autorizadas?

Los equipos de servicio de Microsoft 365 identifican componentes críticos del sistema y sus dependencias como parte de la administración de la continuidad empresarial. Además, Microsoft 365 documenta y realiza un seguimiento de todas las conexiones de sistema externo para asegurarse de que solo se permiten conexiones autorizadas en las configuraciones del firewall de red. La arquitectura de seguridad de la información de Microsoft 365 describe los sistemas, dependencias y conexiones externas de Microsoft 365. La arquitectura de seguridad de la información y los diagramas de flujo de datos correspondientes se revisan y actualizan anualmente como mínimo, así como cuando se realizan cambios significativos en el sistema.

La arquitectura de Microsoft 365 se valida con regularidad y de forma automática usando herramientas basadas en la nube para comprobar la alineación con nuestros principios de seguridad y para probar continuamente las características de aislamiento y resistencia. La validación de arquitectura funciona para identificar automáticamente instancias en las que el estado actual del servicio ha desplazado del estado deseado, marcando cualquier desviación para revisión y mitigación. El objetivo de la validación de la arquitectura es garantizar que las funciones de seguridad de nuestra infraestructura de servicio continúan funcionando como se esperaba.

## <a name="related-external-regulations--certifications"></a>Certificaciones & de las reglamentaciones externas relacionadas

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y las certificaciones externas. Consulte la tabla siguiente para validar los controles relacionados con la arquitectura de Microsoft 365.

| **Auditorías externas** | **Section** | **Fecha del informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-4: aplicación del flujo de información <br> CP-9: copia de seguridad del sistema de información <br> PL-8: arquitectura de seguridad de la información <br> SC-7: protección de límites <br> SC-22: arquitectura y aprovisionamiento | 24 de septiembre de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 6: organización de la seguridad de la información <br> A. 13.1: administración de seguridad de red <br> A. 17.2: redundancias | 22 de febrero de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 6: organización de la seguridad de la información <br> A. 13.1: administración de seguridad de red | 22 de febrero de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-37: aislamiento de inquilino <br> CA-49: directivas de copia de seguridad <br> CA-51: replicación de datos | 30 de septiembre de 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-05: diagramas de flujo de datos <br> CA-37: aislamiento de inquilino <br> CA-49: directivas de copia de seguridad <br> CA-51: replicación de datos | 30 de septiembre de 2019 |