---
title: Información general sobre la supervisión de seguridad
description: Más información sobre la supervisión de seguridad en Microsoft 365
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
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 8a538ee055d10b002ea7efcc7d39ce20658df12b
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787359"
---
# <a name="security-monitoring-overview"></a>Información general sobre la supervisión de seguridad

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>¿Cuál es la estrategia de Microsoft para supervisar la seguridad?

Microsoft 365 participa en la supervisión de seguridad continua de sus sistemas para detectar y responder a las amenazas a los Servicios de Microsoft 365. Nuestros principios clave para la supervisión y alertas de seguridad son:

- Solidez: señales y lógica para detectar una variedad de comportamientos de ataque
- Precisión: alertas significativas para evitar distracciones del ruido
- Velocidad: capacidad de capturar atacantes lo suficientemente rápido como para detenerlos

La automatización, la escala y las soluciones basadas en la nube son los pilares clave de nuestra estrategia de supervisión y respuesta. Para que los ataques se detengan y se detengan de forma eficaz a escala de algunos de los servicios principales de Microsoft 365, nuestros sistemas de supervisión necesitan generar automáticamente alertas altamente precisas casi en tiempo real. Del mismo modo, cuando se detecta un problema, necesitamos la capacidad de mitigar el riesgo a escala, no podemos depender de nuestro equipo para corregir manualmente los problemas máquina por máquina. Para mitigar los riesgos a escala, usamos herramientas basadas en la nube para aplicar automáticamente contramedidas y proporcionar a los ingenieros herramientas para aplicar mitigaciones aprobadas rápidamente en todo el entorno.

## <a name="how-does-microsoft-365-perform-security-monitoring"></a>¿Cómo realiza Microsoft 365 la supervisión de seguridad?

Microsoft 365 usa el registro centralizado para recopilar y analizar eventos de registro de actividades que puedan indicar un incidente de seguridad. Las herramientas de registro centralizado agregan registros de todos los componentes del sistema, incluidos los registros de eventos, los registros de aplicaciones, los registros de control de acceso y los sistemas de detección de intrusiones basados en red. Además del registro del servidor y los datos de nivel de aplicación, la infraestructura principal de nuestro servicio está equipado con agentes de seguridad personalizados que generan telemetría detallada y proporcionan detección de intrusiones basadas en host. Usamos esta telemetría para la supervisión y análisis forense.

Los datos de registro y telemetría que recopilamos permiten alertas de seguridad 24/7. Nuestro sistema de alertas analiza los datos de registro a medida que se cargan, lo que produce alertas casi en tiempo real. Esto incluye alertas basadas en reglas y alertas más sofisticadas basadas en modelos de aprendizaje automático. Nuestra lógica de supervisión va más allá de escenarios de ataque genéricos e incorpora un profundo conocimiento de la arquitectura y las operaciones del servicio. Usamos los datos de supervisión de seguridad para mejorar continuamente nuestros modelos para detectar nuevos tipos de ataques y mejorar la precisión de nuestra supervisión de seguridad.

## <a name="how-does-microsoft-365-respond-to-security-monitoring-alerts"></a>¿Cómo responde Microsoft 365 a las alertas de supervisión de seguridad?

Cuando necesitamos realizar una acción en respuesta a una alerta o investigar aún más las pruebas forenses en todo el servicio, nuestras herramientas basadas en la nube nos permiten responder rápidamente en todo el entorno. Estas herramientas incluyen agentes totalmente automatizados e inteligentes que responden a amenazas detectadas con contramedidas de seguridad. En muchos casos, estos agentes implementan contramedidas automáticas para mitigar las detecciones de seguridad a escala sin intervención humana. Cuando esto no es posible, el sistema de supervisión de seguridad alerta automáticamente a los ingenieros de llamada adecuados, que están equipados con un conjunto de herramientas que les permiten actuar en tiempo real para mitigar las amenazas detectadas a escala. Los posibles incidentes escalados al equipo de respuesta de seguridad de Microsoft 365 se resuelven mediante el proceso de respuesta a incidentes de seguridad.

## <a name="how-does-microsoft-365-monitor-system-availability"></a>¿Cómo supervisa Microsoft 365 la disponibilidad del sistema?

Microsoft 365 supervisa activamente sus sistemas en busca de indicadores de sobrea utilización de recursos y uso anómalo. La supervisión de recursos se complementa con redundancias de servicios para ayudar a evitar un tiempo de inactividad inesperado y proporcionar a los clientes un acceso confiable a los productos y servicios. Los problemas de estado del servicio se comunican rápidamente a los clientes a través del Panel de estado del servicio (SHD).

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las certificaciones y normativas externas. Consulte la tabla siguiente para validar los controles relacionados con la supervisión de seguridad.

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------|:--------|:------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: Administración de cuentas <br> AC-17: Acceso remoto <br> AU-7: Reducción de auditoría y generación de informes <br> SI-4: Supervisión del sistema de información <br> SI-7: integridad de software, firmware e información <br> | 24 de septiembre de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Supervisión de disponibilidad y planeación de capacidad | 22 de febrero de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Supervisión de disponibilidad y planeación de capacidad <br> A.16.1: Administración de incidentes y mejoras de seguridad de la información | 22 de febrero de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Supervisión de cambios <br> CA-26: Informes de incidentes de seguridad <br> CA-29: Ingenieros de llamadas <br> CA-48: Registro de centro de datos | 24 de diciembre de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Supervisión de cambios <br> CA-26: Informes de incidentes de seguridad <br> CA-29: Ingenieros de llamadas <br> CA-30: Supervisión de disponibilidad <br> CA-48: Registro de centro de datos | 24 de diciembre de 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: Informes de incidentes <br> CUEC-10: Contratos de servicio | 24 de diciembre de 2020 |

## <a name="resources"></a>Recursos

- [En segundo plano: proteger la infraestructura que powering el servicio de Microsoft 365](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
