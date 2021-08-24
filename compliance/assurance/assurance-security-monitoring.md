---
title: Información general sobre la supervisión de seguridad
description: Obtenga información sobre la supervisión de seguridad en Microsoft 365
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
ms.openlocfilehash: 8ba736fbd6e72963badc3245e11cbed2292cba94
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481732"
---
# <a name="security-monitoring-overview"></a>Información general sobre la supervisión de seguridad

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>¿Cuál es la estrategia de Microsoft para supervisar la seguridad?

Microsoft se dedica a la supervisión de seguridad continua de sus sistemas para detectar y responder a las amenazas a los servicios en línea de Microsoft. Nuestros principios clave para la supervisión y alertas de seguridad son:

- Robustez: señales y lógica para detectar diversos comportamientos de ataque
- Precisión: alertas significativas para evitar distracciones por ruido
- Velocidad: capacidad para capturar atacantes lo suficientemente rápido como para detenerlos

La automatización, la escala y las soluciones basadas en la nube son pilares clave de nuestra estrategia de supervisión y respuesta. Para evitar de forma eficaz ataques a la escala de algunos de los servicios en línea de Microsoft, nuestros sistemas de supervisión necesitan generar automáticamente alertas de alta precisión en tiempo casi real. Asimismo, cuando se detecta un problema, necesitamos la capacidad de mitigar el riesgo a escala, no podemos confiar en nuestro equipo para solucionar manualmente problemas máquina por máquina. Para mitigar los riesgos a escala, usamos herramientas basadas en la nube para aplicar automáticamente las contramedidas y proporcionar a los ingenieros herramientas para aplicar acciones de mitigación aprobadas rápidamente en todo el entorno.

## <a name="how-do-microsoft-online-services-perform-security-monitoring"></a>¿Cómo realizan los servicios en línea de Microsoft la supervisión de seguridad?

Los servicios en línea de Microsoft usan el registro centralizado para recopilar y analizar eventos de registro para actividades que puedan indicar un incidente de seguridad. Las herramientas de registro centralizadas agregan registros de todos los componentes del sistema, incluidos los registros de eventos, los registros de aplicaciones, los registros de control de acceso y los sistemas de detección de intrusiones basados en red. Además del registro de servidores y los datos de nivel de aplicación, la infraestructura principal está equipada con agentes de seguridad personalizados que generan telemetría detallada y proporcionan detección de intrusiones basadas en host. Usamos esta telemetría para la supervisión y el análisis forense.

Los datos de registro y telemetría que recopilamos permiten alertas de seguridad 24/7. Nuestro sistema de alertas analiza los datos de registro a medida que se cargan, lo que genera alertas casi en tiempo real. Incluye alertas basadas en reglas y alertas más sofisticadas basadas en modelos de aprendizaje automático. Nuestra lógica de supervisión va más allá de los escenarios de ataque genéricos e incorpora un conocimiento profundo de la arquitectura y las operaciones del servicio. Analizamos los datos de supervisión de seguridad para mejorar continuamente nuestros modelos para detectar nuevos tipos de ataques y mejorar la precisión de nuestra supervisión de seguridad.

## <a name="how-do-microsoft-online-services-respond-to-security-monitoring-alerts"></a>¿Cómo responden los servicios en línea de Microsoft a las alertas de supervisión de seguridad?

Cuando los eventos de seguridad que desencadenan alertas requieren una acción de respuesta o una investigación adicional de pruebas forenses en todo el servicio, nuestras herramientas basadas en la nube permiten una respuesta rápida en todo el entorno. Estas herramientas incluyen agentes inteligentes totalmente automatizados que responden a las amenazas detectadas con contramedidas de seguridad. En muchos casos, estos agentes implementan contramedidas automáticas para mitigar las detecciones de seguridad a escala sin intervención humana. Cuando esta respuesta no es posible, el sistema de supervisión de seguridad alerta automáticamente a los ingenieros de llamada adecuados, que están equipados con un conjunto de herramientas que les permiten actuar en tiempo real para mitigar las amenazas detectadas a escala. Las posibles incidencias se escalan al equipo de respuesta de seguridad de Microsoft adecuado y se resuelven mediante el proceso de respuesta a incidentes de seguridad.

## <a name="how-do-microsoft-online-services-monitor-system-availability"></a>¿Cómo supervisan los servicios en línea de Microsoft la disponibilidad del sistema?

Microsoft supervisa activamente sus sistemas en busca de indicadores de sobre utilización de recursos y uso anormal. La supervisión de recursos se complementa con redundancias de servicio para ayudar a evitar un tiempo de inactividad inesperado y proporcionar a los clientes acceso confiable a productos y servicios. Los problemas de estado del servicio en línea de Microsoft se comunican rápidamente a los clientes a través del Panel de mantenimiento del servicio (SHD).

Los servicios en línea de Azure y Dynamics 365 usan varios servicios de infraestructura para supervisar su seguridad y disponibilidad de estado. La implementación de pruebas de transacción sintética (STX) permite a los servicios de Azure y Dynamics comprobar la disponibilidad de sus servicios. El marco STX está diseñado para admitir las pruebas automatizadas de componentes en los servicios en ejecución y se prueba en alertas de error de sitios activos. Además, el servicio Azure Security Monitoring (ASM) ha implementado procedimientos de prueba sintética centralizados para comprobar que las alertas de seguridad funcionan según lo esperado en los servicios nuevos y en ejecución.

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y certificaciones externas. Consulte la siguiente tabla para la validación de controles relacionados con la supervisión de seguridad.

### <a name="azure-and-dynamics-365"></a>Azure y Dynamics 365

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------|:--------|:------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Supervisión de disponibilidad y planeación de capacidad | 2 de diciembre de 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Supervisión de disponibilidad y planeación de capacidad <br> A.16.1: Administración de incidentes y mejoras de seguridad de la información | 2 de diciembre de 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | IM-1: marco de administración de incidentes <br> IM-2: configuración de detección de incidentes <br> IM-3: Procedimientos de administración de incidentes <br> IM-4: Incident post-mortem <br> VM-1: Registro y colección de eventos de seguridad <br> VM-12: supervisión de disponibilidad de servicios de Azure <br> VM-4: investigación de eventos malintencionados <br> VM-6: Supervisión de vulnerabilidades de seguridad | 31 de marzo de 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | IM-1: marco de administración de incidentes <br> IM-2: configuración de detección de incidentes <br> IM-3: Procedimientos de administración de incidentes <br> IM-4: Incident post-mortem <br> PI-2: Revisión del rendimiento del SLA de Azure Portal <br> VM-1: Registro y colección de eventos de seguridad <br> VM-12: supervisión de disponibilidad de servicios de Azure <br> VM-4: investigación de eventos malintencionados <br> VM-6: Supervisión de vulnerabilidades de seguridad | 31 de marzo de 2021 |

### <a name="office-365"></a>Office 365

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------|:--------|:------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AC-2: Administración de cuentas <br> AC-17: Acceso remoto <br> AU-7: Reducción de auditoría y generación de informes <br> SI-4: Supervisión del sistema de información <br> SI-7: Integridad de software, firmware e información <br> | 24 de septiembre de 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Supervisión de disponibilidad y planeación de capacidad | 20 de abril de 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Supervisión de cambios <br> CA-26: Informes de incidentes de seguridad <br> CA-29: Ingenieros de llamadas <br> CA-48: Registro de centros de datos | 24 de diciembre de 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Supervisión de cambios <br> CA-26: Informes de incidentes de seguridad <br> CA-29: Ingenieros de llamadas <br> CA-30: Supervisión de disponibilidad <br> CA-48: Registro de centros de datos | 24 de diciembre de 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: Informar de incidentes <br> CUEC-10: Contratos de servicio | 24 de diciembre de 2020 |

## <a name="resources"></a>Recursos

- [Entre bastidores: protección de la infraestructura que impulsa el servicio Microsoft 365](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
