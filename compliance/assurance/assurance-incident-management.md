---
title: Información general sobre la administración de incidencias
description: Más información sobre la administración de incidentes en Microsoft 365
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
ms.openlocfilehash: 24ecad99115705f293f765edb84345dad8ff8c93
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787319"
---
# <a name="incident-management-overview"></a>Información general sobre la administración de incidencias

## <a name="what-is-a-security-incident"></a>¿Qué es un incidente de seguridad?

Microsoft define un incidente de seguridad en sus servicios en línea como una infracción de seguridad confirmada que conduce a la destrucción, pérdida, alteración, divulgación no autorizada o acceso a datos personales o accidentales o ilegales durante el proceso por Parte de Microsoft. Por ejemplo, el acceso no autorizado a la infraestructura de Microsoft 365 y la filtración de datos de clientes constituye un incidente de seguridad, mientras que los eventos de cumplimiento que no afectan a la confidencialidad, integridad o disponibilidad de servicios o datos de clientes no se consideran incidentes de seguridad.

## <a name="how-does-microsoft-respond-to-security-incidents"></a>¿Cómo responde Microsoft a los incidentes de seguridad?

Siempre que haya un incidente de seguridad, Microsoft se esfuerza por responder de forma rápida y eficaz para proteger los servicios de Microsoft y los datos de los clientes. Microsoft emplea una estrategia de respuesta a incidentes diseñada para investigar, contener y eliminar amenazas de seguridad de forma rápida y eficaz.

Los servicios en la nube de Microsoft se supervisan continuamente en busca de signos de peligro. Además de la supervisión y alertas de seguridad automatizadas, todos los empleados reciben formación anual para reconocer y notificar signos de posibles incidentes de seguridad. Cualquier actividad sospechosa detectada por empleados, clientes o herramientas de supervisión de seguridad se escala a los equipos de respuesta de seguridad específicos del servicio para su investigación. Todos los equipos de operaciones de servicio, incluidos los equipos de respuesta de seguridad específicos del servicio, mantienen una rotación de llamada profunda para garantizar que los recursos estén disponibles para la respuesta a incidentes 24 x 7 x 365. Nuestras rotaciones de llamadas permiten a Microsoft montar una respuesta a incidentes eficaz en cualquier momento o escala, incluidos los eventos extendidos o simultáneos.

Cuando se detecta y escala actividad sospechosa, los equipos de respuesta de seguridad específicos del servicio inician un proceso de análisis, contención, reactivación **y recuperación.** Estos equipos coordinan el análisis del posible incidente para determinar su ámbito, incluido cualquier impacto en los clientes o los datos de los clientes. Basándose en este análisis, los equipos de respuesta de seguridad específicos del servicio trabajan con los equipos de servicio afectados para desarrollar un plan que contenga la amenaza y minimice el impacto del incidente, resalte la amenaza del entorno y recupere completamente un estado seguro conocido. Los equipos de servicio relevantes implementan el plan con el soporte de equipos de respuesta de seguridad específicos del servicio para garantizar que la amenaza se elimina correctamente y los servicios afectados se someten a una recuperación completa.

Una vez resuelto un incidente, los equipos de servicio implementan las lecciones aprendidas del incidente para prevenir, detectar y responder mejor a incidentes similares en el futuro. Select security incidents, especially those that are customer-impacting or result in a data breach, undergo a full incident post-mortem. El análisis posterior está diseñado para identificar fallas técnicas, errores de procedimientos, errores manuales y otros defectos del proceso que podrían haber contribuido al incidente o que se identificaron durante el proceso de respuesta a incidentes. Las mejoras identificadas durante el análisis posterior se implementan con la coordinación de los equipos de respuesta de seguridad específicos del servicio para ayudar a evitar incidentes futuros y mejorar las capacidades de detección y respuesta.

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>¿Cómo y cuándo se notifica a los clientes sobre incidentes de seguridad o privacidad?

Siempre que Microsoft tenga conocimiento de una vulneración de seguridad que implique la pérdida, divulgación o modificación no autorizada de los datos de los clientes, Microsoft notifica a los clientes afectados en un plazo de 72 horas como se indica en el Anexo de protección de datos (DPA) de los Términos de Servicios en línea (OST). El compromiso de la escala de tiempo de notificación comienza cuando se produce la declaración oficial de incidentes de seguridad. Tras declarar un incidente de seguridad, el proceso de notificación se produce lo antes posible, sin retrasos debidos.

Las notificaciones incluyen una descripción de la naturaleza de la infracción, el impacto aproximado del usuario y los pasos de mitigación (si procede). Si la investigación de Microsoft no se completa en el momento de la notificación inicial, la notificación también indicará los siguientes pasos y escalas de tiempo para la comunicación posterior.

Si un cliente tiene conocimiento de un incidente que podría tener un impacto en Microsoft, incluida, entre otras, una infracción de datos, el cliente es responsable de notificar rápidamente a Microsoft del incidente tal como se define en el DPA.

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las certificaciones y normativas externas. Consulte la tabla siguiente para validar los controles relacionados con la administración de incidentes.

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | IR-4: Control de incidentes <br> IR-6: Informes de incidentes <br> IR-8: Plan de respuesta a incidentes | 24 de septiembre de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: Administración de incidentes y mejoras de seguridad de la información | 22 de febrero de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: Administración de incidentes y mejoras de seguridad de la información | 22 de febrero de 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Notificación de una infracción de datos que implica PII  | 22 de febrero de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-26: Informes de incidentes de seguridad <br> CA-47: Respuesta a incidentes | 24 de diciembre de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-12: Contratos de nivel de servicio (SLA) <br> CA-13: Guías de respuesta a incidentes <br> CA-15: Notificaciones de estado del servicio  <br>  <br> CA-26: Informes de incidentes de seguridad <br> CA-29: Ingenieros de llamadas <br> CA-47: Respuesta a incidentes | 24 de diciembre de 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: Informes de incidentes  | 24 de diciembre de 2020  |

## <a name="resources"></a>Recursos

- [Términos de Online Services (OST)](https://www.microsoft.com/licensing/product-licensing/products)
- [Anexo de protección de datos (DPA)](https://www.microsoft.com/licensing/product-licensing/products)
- [Guía de implementación de administración de incidentes en la nube de Microsoft para Azure y Office 365](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365: Evaluación de vulnerabilidad de terceros de Office 365 - 2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
