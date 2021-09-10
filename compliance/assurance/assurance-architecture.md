---
title: Introducción a la arquitectura
description: Obtenga información sobre la arquitectura en Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 97fe615296f03c8f72dbf23d886501988686b53a
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947226"
---
# <a name="architecture-overview"></a>Introducción a la arquitectura

## <a name="what-are-microsoft-online-services"></a>¿Qué son los servicios en línea de Microsoft?

Los servicios en línea de Microsoft hacen referencia a los servicios basados en la nube ofrecidos por Microsoft, que incluyen Azure, Dynamics 365 y Microsoft 365.  Cada servicio ofrece soluciones únicas a las necesidades comunes de productividad y operación empresarial, que sirven a clientes de todo el mundo, desde pequeñas empresas hasta grandes empresas y gobiernos. Los centros de datos distribuidos globalmente conectados por la infraestructura de red administrada independientemente de Microsoft actúan como la columna troncal para admitir servicios en línea, lo que proporciona la capacidad de mantener la disponibilidad en casi todas las situaciones y escalar a una demanda mundial masiva.

Todos los servicios en línea de Microsoft tienen el mismo objetivo de proteger la infraestructura de servicio que administran y los datos de sus clientes, pero cada servicio en línea está operado por una unidad de negocio independiente. En muchos casos, los controles de seguridad se implementan de la misma manera en todos los servicios, pero en algunos casos, toman un enfoque diferente para cumplir sus promesas de cliente y sus obligaciones de cumplimiento.

## <a name="what-is-azure"></a>¿Qué es Azure?

Microsoft Azure es una plataforma informática en la nube para crear, implementar y administrar aplicaciones a través de una red global de centros de datos administrados de Microsoft y de terceros. Admite modelos de servicio en la nube de Plataforma como servicio (PaaS) e Infraestructura como servicio (IaaS) y permite soluciones híbridas que integran los servicios en la nube con los recursos locales de los clientes. Microsoft Azure muchos clientes, partners y organizaciones gubernamentales que abarcan una amplia variedad de productos y servicios, geografías e industrias. Microsoft Azure está diseñado para cumplir con sus requisitos de seguridad, confidencialidad y cumplimiento.

## <a name="what-is-dynamics-365"></a>¿Qué es Dynamics 365?

Dynamics 365 es un conjunto de aplicaciones empresariales en línea que integra las capacidades de administración de relaciones con el cliente (CRM) y sus extensiones con las capacidades de planeación de recursos (ERP) de Enterprise recursos. Estas aplicaciones empresariales de extremo a extremo ayudan a los clientes a convertir las relaciones en ingresos, a ganar clientes y a acelerar el crecimiento empresarial. Dynamics 365 es un conjunto de aplicaciones de software como servicio (SaaS) integrado en la infraestructura de Azure y está disponible para clientes de todo el mundo a través de sus centros de datos distribuidos globalmente.

## <a name="what-is-microsoft-365"></a>¿Qué es Microsoft 365?

Microsoft 365 es la versión basada en suscripción basada en la nube de Office, Windows 10, Enterprise Mobility + Security y Cumplimiento. Microsoft 365 clientes obtienen clientes como Outlook y Windows, y también se benefician de los servicios que Hospeda Microsoft en su nombre, como Exchange Online, Microsoft Teams y SharePoint Online. Todos los componentes del servicio se actualizan periódicamente como parte del modelo de suscripción, de modo que nuestros clientes tengan un producto 'evergreen'. Microsoft administra la infraestructura de servicio en nombre de los clientes, lo que significa que Microsoft es responsable de proteger la infraestructura que almacena los datos de los clientes.

En términos de escala, Microsoft usa actualmente cerca de un millón de máquinas para Microsoft 365 servicios. La infraestructura que proporciona estos servicios varía ampliamente entre el hardware específico del servicio y los entornos virtualizados en Azure, Windows y Linux, y plataformas dedicadas y multiinquilino. Microsoft 365 es un negocio global y nuestra infraestructura se distribuye en centros de datos de todo el mundo, lo que permite a nuestros clientes cumplir los requisitos de soberanía y residencia de datos.

## <a name="how-do-microsoft-online-services-ensure-isolation-between-customer-tenants"></a>¿Cómo garantizan los servicios en línea de Microsoft el aislamiento entre inquilinos de clientes?

Los servicios en la nube de Microsoft se basa en la suposición de que todos los inquilinos son potencialmente hostiles para todos los demás inquilinos. Para aislar correctamente los inquilinos entre sí, Microsoft implementa varias tecnologías y controles de aislamiento. Estos controles están diseñados para proteger contra la filtración de información o el acceso no autorizado a los datos de clientes en todos los inquilinos y para evitar que las acciones de un inquilino afecten negativamente al servicio de otro inquilino.

El contenido del cliente se aísla lógicamente en los inquilinos mediante Azure Active Directory (Azure AD). La autenticación de usuario en los servicios en línea de Microsoft comprueba no solo la identidad de usuario, sino también la identidad de inquilino de la que forma parte la cuenta de usuario, lo que impide que los usuarios tengan acceso a datos fuera de su entorno de inquilino. Para complementar el aislamiento lógico de Azure AD, el contenido del cliente siempre se cifra en reposo y en tránsito. Los servicios individuales también pueden proporcionar capas adicionales de aislamiento de inquilino, como el aislamiento SharePoint en línea de los datos del inquilino en bases de datos cifradas independientes.

## <a name="how-do-microsoft-online-services-engineer-resilient-services-that-avoid-single-points-of-failure"></a>¿Cómo los servicios en línea de Microsoft diseñan servicios resistentes que evitan puntos de error únicos?

Microsoft diseña y crea servicios en la nube para maximizar la confiabilidad y minimizar los efectos negativos en los clientes ante errores y desafíos a las operaciones normales. Esta estrategia comienza con el diseño de la red que conecta nuestros centros de datos distribuidos geográficamente. La arquitectura de red de Microsoft incluye interconexiones directas y varias rutas de red. Los servicios en línea de Microsoft usan esta redundancia para enrutar automáticamente el tráfico alrededor de errores para mejorar la calidad del servicio.

Siempre que sea posible, los servicios en línea de Microsoft se implementan en configuraciones activas o activas con supervisión automatizada del estado del servicio, lo que permite al servicio detectar y recuperarse de muchos errores y errores comunes sin intervención humana. Además de las configuraciones activas o activas, los servicios en línea de Microsoft aumentan la tolerancia a errores al garantizar que el servicio se implementa en zonas de error independientes, lo que impide que un error en una zona afecte a la disponibilidad de otras zonas.

La resistencia de datos complementa la resistencia del servicio protegiendo la integridad y disponibilidad de los datos en los servicios en línea de Microsoft. Nuestros servicios usan redundancia de almacenamiento local y redundancia geográfica para replicar copias de datos de clientes en diferentes zonas de errores. Si los datos están dañados o perdidos en una zona de error, se puede acceder a ellos en otra zona de error sin pérdida de disponibilidad. La comprobación de integridad automatizada restaura automáticamente los datos afectados por muchos tipos de daños físicos o lógicos. Microsoft también proporciona a los clientes herramientas para restaurar datos eliminados o modificados accidentalmente por el cliente en servicios como Exchange Online y SharePoint Online.

## <a name="how-do-microsoft-online-services-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>¿Cómo hacen los servicios en línea de Microsoft para realizar un seguimiento de las dependencias y evitar las conexiones de sistema externo no autorizadas?

Los equipos de servicios en línea de Microsoft identifican componentes críticos del sistema y sus dependencias como parte de la Administración de continuidad empresarial. Además, Microsoft documenta y realiza un seguimiento de todas las conexiones del sistema externo para garantizar que solo se permiten conexiones autorizadas en configuraciones de firewall de red. Los sistemas de servicios en línea de Microsoft, las dependencias y las conexiones externas se documentan en la arquitectura de seguridad de la información de los servicios en línea de Microsoft. Tanto la arquitectura de seguridad de la información como los diagramas de flujo de datos correspondientes se revisan y actualizan anualmente como mínimo, así como siempre que se realicen cambios significativos en el sistema.

La arquitectura de los servicios en línea de Microsoft se valida periódica y automáticamente con herramientas basadas en la nube para comprobar la alineación con nuestros principios de seguridad y para probar continuamente las características de aislamiento y resistencia. La validación de arquitectura funciona para identificar automáticamente las instancias en las que el estado actual del servicio se ha desviado del estado deseado, marcando cualquier desviación para revisión y mitigación. El objetivo de la validación de arquitectura es garantizar que las capacidades de seguridad de nuestra infraestructura de servicio sigan funcionando como se esperaba.

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y certificaciones externas. Consulte la siguiente tabla para la validación de controles relacionados con la arquitectura.

### <a name="azure-and-dynamics-365"></a>Azure y Dynamics 365

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organización de la seguridad de la información <br> A.13.1: Administración de seguridad de red <br> A.17.2: Redundancias | 2 de diciembre de 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organización de la seguridad de la información <br> A.13.1: Administración de seguridad de red <br> A.17.2: Redundancias | 2 de diciembre de 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | BC-1: Planes de continuidad empresarial <br> BC-3: procedimientos BCDR <br> BC-4: pruebas bcdr <br> BC-5: Evaluaciones de riesgos de continuidad empresarial <br> BC-6: Continuidad empresarial de terceros <br> BC-7: Procedimientos de continuidad empresarial del centro de datos <br> BC-8: Pruebas de continuidad empresarial del centro de datos <br> BC-9: Evaluación de resistencia de centros de datos <br>  DS-6: redundancia de componentes críticos <br> DS-7: Replicación de datos de clientes <br> DS-14: Restauración de servicios al cliente <br> DS-16: Segregación de datos del cliente | 31 de marzo de 2021 |

### <a name="office-365"></a>Office 365

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AC-4: Aplicación del flujo de información <br> CP-9: Copia de seguridad del sistema de información <br> PL-8: Arquitectura de seguridad de la información <br> SC-7: Protección de límites <br> SC-22: Arquitectura y aprovisionamiento | 24 de septiembre de 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organización de la seguridad de la información <br> A.13.1: Administración de seguridad de red <br> A.17.2: Redundancias | 20 de abril de 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37: aislamiento de inquilinos <br> CA-49: Directivas de copia de seguridad <br> CA-51: replicación de datos | 24 de diciembre de 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05: Diagramas de flujo de datos <br> CA-37: aislamiento de inquilinos <br> CA-49: Directivas de copia de seguridad <br> CA-51: replicación de datos | 24 de diciembre de 2020 |