---
title: Introducción a la arquitectura
description: Más información sobre la arquitectura en Microsoft 365
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
ms.openlocfilehash: e1b4e9701e76c1e758f683750c8ebfeda2bc1f1f
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787496"
---
# <a name="architecture-overview"></a>Introducción a la arquitectura

## <a name="what-is-microsoft-365"></a>¿Qué es Microsoft 365?

Microsoft 365 es la versión basada en la nube basada en suscripción de Office, Windows 10, Enterprise Mobility + Security y Cumplimiento. Los clientes de Microsoft 365 obtienen clientes como Outlook y Windows, y también se benefician de los servicios que Microsoft hospeda en su nombre, como Exchange Online, Microsoft Teams y SharePoint Online. Todos los componentes del servicio se actualizan periódicamente como parte del modelo de suscripción, para que nuestros clientes tengan un producto "de hoja de vida". Microsoft administra la infraestructura de servicio en nombre de los clientes, lo que significa que Microsoft es responsable de proteger la infraestructura que almacena los datos de los clientes.

En términos de escala, actualmente usamos cerca de un millón de máquinas para dar energía a los servicios de Microsoft 365. La infraestructura que usa estos servicios varía ampliamente entre hardware específico del servicio y entornos virtualizados en Azure, Windows y Linux, y plataformas multiinquilino y dedicadas. Microsoft 365 es una empresa global y nuestra infraestructura se distribuye en centros de datos de todo el mundo, lo que permite a nuestros clientes cumplir los requisitos de residencia de datos y independencia.

En resumen, el servicio es complejo, se ejecuta a una escala increíble y requiere miles de ingenieros de Microsoft para crear y mantener. Es nuestra prioridad principal mantener toda esta infraestructura segura.

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>¿Cómo garantiza Microsoft 365 el aislamiento entre inquilinos de clientes?

Los servicios en la nube de Microsoft se construyen en la suposición de que todos los inquilinos son potencialmente ajenados a todos los demás inquilinos. Para aislar correctamente los inquilinos entre sí, Microsoft implementa una variedad de tecnologías y controles de aislamiento. Estos controles están diseñados para proteger contra la fuga de información o el acceso no autorizado a los datos de los clientes en todos los inquilinos y para evitar que las acciones de un inquilino afecten negativamente al servicio de otro inquilino.

El contenido del cliente se aísla lógicamente en los inquilinos de Microsoft 365 con Azure Active Directory (Azure AD). La autenticación de usuario en Microsoft 365 comprueba no solo la identidad del usuario, sino también la identidad del inquilino de la que forma parte la cuenta de usuario, lo que impide que los usuarios tengan acceso a datos fuera de su entorno de inquilino. Para complementar el aislamiento lógico de Azure AD, el contenido del cliente siempre se cifra en reposo y en tránsito. Los servicios individuales también pueden proporcionar capas adicionales de aislamiento de inquilinos, como el aislamiento de SharePoint Online de datos de inquilino en bases de datos cifradas independientes.

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>¿Cómo diseña Microsoft 365 servicios resistentes que evitan puntos únicos de error?

Microsoft diseña y crea servicios en la nube para maximizar la confiabilidad y minimizar los efectos negativos en los clientes ante errores y desafíos a las operaciones normales. Esta estrategia comienza con el diseño de la red que conecta nuestros centros de datos distribuidos geográficamente. La arquitectura de red de Microsoft incluye interconexiones directas y varias rutas de red. Los servicios de Microsoft 365 aprovechan esta redundancia para enrutar automáticamente el tráfico en torno a errores para mejorar la calidad del servicio.

En el nivel de servicio, la estrategia de resistencia de Microsoft 365 prioriza la resistencia de software. Siempre que sea posible, nuestros servicios se implementan en configuraciones activas/activas con supervisión automatizada del estado del servicio, lo que permite al servicio detectar y recuperarse de muchos errores y errores comunes sin la intervención humana. Además de las configuraciones activas/activas, los servicios de Microsoft 365 aumentan la tolerancia a errores al garantizar que el servicio se implementa en zonas de error independientes, evitando que un error en una zona afecte a la disponibilidad de otras zonas.

La resistencia de datos complementa la resistencia de servicios al proteger la integridad y disponibilidad de los datos en los servicios de Microsoft 365. Nuestros servicios usan redundancia de almacenamiento local y redundancia geográfica para replicar copias de datos de clientes en diferentes zonas de error. Si los datos están dañados o perdidos en una zona de error, se puede tener acceso a ellos en otra zona de error sin pérdida de disponibilidad. La comprobación de integridad automatizada restaura automáticamente los datos afectados por muchos tipos de daños físicos o lógicos. Microsoft 365 también proporciona a los clientes herramientas para restaurar datos eliminados o modificados accidentalmente por el cliente en Exchange Online y SharePoint Online.

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>¿Cómo realiza Microsoft 365 el seguimiento de las dependencias y evita las conexiones no autorizadas del sistema externo?

Los equipos de servicio de Microsoft 365 identifican componentes críticos del sistema y sus dependencias como parte de la Administración de continuidad empresarial. Además, Microsoft 365 documenta y realiza un seguimiento de todas las conexiones del sistema externo para garantizar que solo se permiten las conexiones autorizadas en las configuraciones de firewall de red. Los sistemas, dependencias y conexiones externas de Microsoft 365 se documentan en la arquitectura de seguridad de la información de Microsoft 365. Tanto la arquitectura de seguridad de la información como los diagramas de flujo de datos correspondientes se revisan y actualizan anualmente como mínimo, así como siempre que se realicen cambios significativos en el sistema.

La arquitectura de Microsoft 365 se valida periódica y automáticamente mediante herramientas basadas en la nube para comprobar la alineación con nuestros principios de seguridad y para probar continuamente las características de aislamiento y resistencia. La validación de arquitectura funciona para identificar automáticamente las instancias en las que el estado actual del servicio se ha desviado del estado deseado, marcando las desviaciones para revisión y mitigación. El objetivo de la validación de arquitectura es garantizar que las capacidades de seguridad de nuestra infraestructura de servicio sigan funcionando según lo esperado.

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las certificaciones y normativas externas. Consulte la tabla siguiente para validar los controles relacionados con la arquitectura de Microsoft 365.

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-4: Aplicación del flujo de información <br> CP-9: Copia de seguridad del sistema de información <br> PL-8: Arquitectura de seguridad de la información <br> SC-7: Protección de límites <br> SC-22: Arquitectura y aprovisionamiento | 24 de septiembre de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organización de la seguridad de la información <br> A.13.1: Administración de seguridad de red <br> A.17.2: Redundancias | 22 de febrero de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organización de la seguridad de la información <br> A.13.1: Administración de seguridad de red | 22 de febrero de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37: Aislamiento de inquilinos <br> CA-49: Directivas de copia de seguridad <br> CA-51: Replicación de datos | 24 de diciembre de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05: Diagramas de flujo de datos <br> CA-37: Aislamiento de inquilinos <br> CA-49: Directivas de copia de seguridad <br> CA-51: Replicación de datos | 24 de diciembre de 2020 |