---
title: Información general sobre la supervisión de seguridad
description: Obtenga información sobre la supervisión de la seguridad en Microsoft 365
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
ms.openlocfilehash: f3eae0aa5ba79372a7ce0d9a34d4dd35fe83a36b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/30/2020
ms.locfileid: "49509847"
---
# <a name="security-monitoring-overview"></a>Información general sobre la supervisión de seguridad

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>¿Cuál es la estrategia de Microsoft para supervisar la seguridad?

Microsoft 365 participa en la supervisión de seguridad continua de sus sistemas para detectar y responder a las amenazas a los servicios de Microsoft 365. Nuestros principios clave para la supervisión y las alertas de seguridad son los siguientes:

- Solidez: señales y lógica para detectar diversos comportamientos de ataque
- Exactitud: alertas significativas para evitar distracciones por ruido
- Velocidad: capacidad para capturar a los atacantes con rapidez suficiente para detenerlos

La automatización, escala y soluciones basadas en la nube son pilares clave de nuestra estrategia de supervisión y respuesta. Para que podamos captar y detener los ataques de forma eficaz a escala de algunos de los servicios principales de Microsoft 365, nuestros sistemas de supervisión necesitan generar alertas muy precisas casi de forma automática en tiempo real. Del mismo modo, cuando se detecta un problema, es necesario poder mitigar el riesgo a escala, no se puede confiar en nuestro equipo para corregir manualmente los problemas de forma automática. Para mitigar los riesgos a escala, usamos herramientas basadas en la nube para aplicar contramedidas automáticamente y proporcionar a los ingenieros herramientas para aplicar de forma rápida las mitigaciones aprobadas en todo el entorno.

## <a name="how-does-microsoft-365-perform-security-monitoring"></a>¿Cómo realiza Microsoft 365 la supervisión de seguridad?

Microsoft 365 usa el registro centralizado para recopilar y analizar eventos de registro para actividades que puedan indicar un incidente de seguridad. Las herramientas de registro centralizado agregan registros de todos los componentes del sistema, incluidos los registros de eventos, los registros de aplicaciones, los registros de control de acceso y los sistemas de detección de intrusiones basados en red. Además del registro del servidor y los datos del nivel de la aplicación, la infraestructura básica de nuestro servicio está equipada con agentes de seguridad personalizados que generan telemetría detallada y proporcionan detección de intrusiones basada en host. Usamos esta telemetría para supervisión y análisis forense.

Los datos de registro y telemetría que recopilamos permiten alertas de seguridad de 24/7. Nuestro sistema de alertas analiza los datos de registro a medida que se cargan, lo que produce alertas casi en tiempo real. Esto incluye alertas basadas en reglas y alertas más sofisticadas basadas en modelos de aprendizaje de la máquina. Nuestra lógica de supervisión va más allá de los escenarios de ataque genérico e incorpora un conocimiento profundo de la arquitectura y las operaciones de servicio. Usamos datos de supervisión de seguridad para mejorar continuamente nuestros modelos para detectar nuevos tipos de ataques y mejorar la precisión de la supervisión de seguridad.

## <a name="how-does-microsoft-365-respond-to-security-monitoring-alerts"></a>¿Cómo responde Microsoft 365 a las alertas de supervisión de seguridad?

Cuando se necesita realizar una acción en respuesta a una alerta o para investigar con más detalle pruebas forenses en el servicio, nuestras herramientas basadas en la nube nos permiten responder rápidamente en todo el entorno. Estas herramientas incluyen agentes inteligentes completamente automatizados que responden a amenazas detectadas con contramedidas de seguridad. En muchos casos, estos agentes implementan contramedidas automáticas para mitigar las detecciones de seguridad a escala sin intervención humana. Si esto no es posible, el sistema de supervisión de seguridad alerta automáticamente a los ingenieros de llamada adecuados, que cuentan con un conjunto de herramientas que les permiten actuar en tiempo real para mitigar las amenazas detectadas a escala. Los incidentes potenciales que se han transferido al equipo de respuesta de seguridad de 365 de Microsoft se resuelven con el proceso de respuesta a incidentes de seguridad.

## <a name="how-does-microsoft-365-monitor-system-availability"></a>¿Cómo supervisa Microsoft 365 la disponibilidad del sistema?

Microsoft 365 supervisa activamente sus sistemas en busca de indicadores de infrautilización y uso anormal de los recursos. La supervisión de recursos se complementa mediante redundancias de servicio para ayudar a evitar un tiempo de inactividad inesperado y proporcionar a los clientes un acceso confiable a los productos y servicios. Los problemas de estado del servicio se comunican con prontitud a los clientes a través del panel de estado del servicio (publicación).

## <a name="related-external-regulations--certifications"></a>Certificaciones & de las reglamentaciones externas relacionadas

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y las certificaciones externas. Consulte la tabla siguiente para validar los controles relacionados con la supervisión de seguridad.

| **Auditorías externas** | **Section** | **Fecha del informe más reciente** |
|:--------|:--------|:------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: administración de cuentas <br> AC-17: acceso remoto <br> AU-7: reducción de auditoría y generación de informes <br> SI-4: supervisión del sistema de información <br> SI-7: software, firmware e integridad de la información <br> | 24 de septiembre de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.1.3: Planeación de la capacidad y supervisión de la disponibilidad | 22 de febrero de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.1.3: Planeación de la capacidad y supervisión de la disponibilidad <br> A. 16.1: administración de incidentes y mejoras de seguridad de la información | 22 de febrero de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-19: supervisión de cambios <br> CA-26: informes de incidentes de seguridad <br> CA-29: ingenieros de llamada <br> CA-48: registro de centro de conexión | 30 de septiembre de 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-19: supervisión de cambios <br> CA-26: informes de incidentes de seguridad <br> CA-29: ingenieros de llamada <br> CA-30: supervisión de disponibilidad <br> CA-48: registro de centro de conexión | 30 de septiembre de 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-08: informes de incidentes <br> CUEC-10: contratos de servicio | 30 de septiembre de 2019 |

## <a name="resources"></a>Recursos

- [En segundo plano: protección de la infraestructura para alimentar el servicio 365 de Microsoft](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
