---
title: Información general de administración de incidentes
description: Obtenga información sobre la administración de incidentes en Microsoft 365
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
ms.openlocfilehash: 6b5c77a2a81f8231ad620fbc40205457c6ba1a49
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507852"
---
# <a name="incident-management-overview"></a>Información general de administración de incidentes

## <a name="what-is-a-security-incident"></a>¿Qué es un incidente de seguridad?

Microsoft define un incidente de seguridad en sus servicios en línea como una infracción de seguridad confirmada que provoca la destrucción, pérdida, alteración, revelación no autorizada o acceso a datos de clientes o datos personales que Microsoft está procesando de forma accidental o ilícita. Por ejemplo, el acceso no autorizado a la infraestructura de 365 de Microsoft y la exfiltración de los datos de clientes constituyen un incidente de seguridad, mientras que los eventos de cumplimiento que no afectan a la confidencialidad, la integridad o la disponibilidad de los servicios o los datos de los clientes no se consideran incidentes de seguridad.

## <a name="how-does-microsoft-respond-to-security-incidents"></a>¿Cómo responde Microsoft a los incidentes de seguridad?

Siempre que haya un incidente de seguridad, Microsoft se esfuerza por responder de forma rápida y eficaz para proteger los servicios de Microsoft y los datos de clientes. Microsoft emplea una estrategia de respuesta a incidentes diseñada para investigar, contener y eliminar las amenazas de seguridad de forma rápida y eficaz.

Los servicios en la nube de Microsoft se supervisan continuamente en busca de signos de peligro. Además de las alertas y la supervisión automatizada de la seguridad, todos los empleados reciben formación anual para reconocer e informar sobre los incidentes de seguridad potenciales. Cualquier actividad sospechosa que hayan detectado los empleados, los clientes o las herramientas de supervisión de seguridad se remitirán a los equipos de respuesta de seguridad específicos del servicio para su investigación. Todos los equipos de operaciones de servicio, incluidos los equipos de respuesta de seguridad específicos del servicio, mantienen una rotación de llamada profunda para garantizar que los recursos están disponibles para la respuesta a incidentes 24x7x365. Nuestras rotaciones de llamada permiten a Microsoft montar una respuesta de incidente efectiva en cualquier momento o escala, incluidos eventos generalizados o simultáneos.

Cuando se detectan actividades sospechosas y se escalan, los equipos de respuesta de seguridad específicos del servicio inician un proceso de **análisis, contención, erradicación y recuperación**. Estos equipos coordinan el análisis del posible incidente para determinar su ámbito, lo que incluye cualquier impacto en los clientes o los datos de los clientes. Basándose en este análisis, los equipos de respuesta de seguridad específicos del servicio trabajan con los equipos de servicio afectados para desarrollar un plan para contener la amenaza y minimizar el impacto del incidente, erradicar la amenaza del entorno y recuperar completamente a un estado seguro conocido. Los equipos de servicio relevantes implementan el plan con soporte de los equipos de respuesta de seguridad específicos del servicio para garantizar que la amenaza se elimine correctamente y los servicios afectados sufran una recuperación completa.

Después de resolver un incidente, los equipos de servicio implementan las lecciones aprendidas del incidente para evitar, detectar y responder mejor a incidentes similares en el futuro. Seleccione los incidentes de seguridad, especialmente aquellos que tienen un impacto en el cliente o dan lugar a una infracción de datos, se someten a un análisis completo del incidente. El post-mortem está diseñado para identificar las interrupciones técnicas, los errores de procedimientos, los errores manuales y otros errores de procesos que puedan haber contribuido al incidente o que se identificaron durante el proceso de respuesta ante incidentes. Las mejoras identificadas durante el post-mortem se implementan con la coordinación de los equipos de respuesta de seguridad específicos del servicio para ayudar a evitar futuros incidentes y mejorar las capacidades de detección y respuesta.

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>¿Cómo y cuándo se notifican los incidentes de seguridad o privacidad a los clientes?

Siempre que Microsoft detecta una violación de la seguridad que implica pérdida, revelación o modificación no autorizados de los datos de los clientes, Microsoft notifica a los clientes afectados en un plazo de 72 horas, como se describe en el anexo de protección de datos (DPA) de los términos de servicios en línea (OST). El compromiso escala de tiempo de notificación se inicia cuando se produce la declaración oficial de incidente de seguridad. Al declarar un incidente de seguridad, el proceso de notificación se produce tan rápidamente como sea posible, sin que haya un retraso indebido.

Las notificaciones incluyen una descripción de la naturaleza de la infracción, aproximadamente el impacto de los usuarios y los pasos de mitigación (si procede). Si la investigación de Microsoft no se completa en el momento de la notificación inicial, la notificación también indicará los siguientes pasos y escalas de tiempo para la comunicación subsiguiente.

Si un cliente se da cuenta de un incidente que puede tener un impacto en Microsoft, incluidos pero sin limitarse a una infracción de datos, el cliente es responsable de notificar con prontitud a Microsoft el incidente tal como se define en DPA.

## <a name="related-external-regulations--certifications"></a>Certificaciones & de las reglamentaciones externas relacionadas

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y las certificaciones externas. Consulte la tabla siguiente para validar los controles relacionados con la administración de incidentes.

| **Auditorías externas** | **Section** | **Fecha del informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | IR-4: tratamiento de incidentes <br> IR a 6: informes de incidentes <br> IR-8: Plan de respuesta ante incidentes | 24 de septiembre de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 16.1: administración de incidentes y mejoras de seguridad de la información | 22 de febrero de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 16.1: administración de incidentes y mejoras de seguridad de la información | 22 de febrero de 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 10.1: notificación de una infracción de datos en relación con PII  | 22 de febrero de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-26: informes de incidentes de seguridad <br> CA-47: respuesta de incidente | 30 de septiembre de 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-12: contratos de nivel de servicio (SLA) <br> CA-13: guías de respuesta a incidentes <br> CA-15: notificaciones de estado del servicio  <br>  <br> CA-26: informes de incidentes de seguridad <br> CA-29: ingenieros de llamada <br> CA-47: respuesta de incidente | 30 de septiembre de 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-08: informes de incidentes  | 30 de septiembre de 2019  |

## <a name="resources"></a>Recursos

- [Términos de servicios en línea (OST)](https://www.microsoft.com/licensing/product-licensing/products)
- [Anexo de protección de datos (DPA)](https://www.microsoft.com/licensing/product-licensing/products)
- [Guía de implementación de administración de incidentes de Microsoft Cloud para Azure y Office 365](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365: evaluación de la vulnerabilidad de terceros de Office 365-2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
