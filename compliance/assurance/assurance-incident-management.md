---
title: Información general sobre la administración de incidencias
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
hideEdit: true
ms.openlocfilehash: a699f3fbaeded6922ec6c82aa732ed52474f936b2d6a8391650474064334249c
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "54290998"
---
# <a name="incident-management-overview"></a>Información general sobre la administración de incidencias

## <a name="what-is-a-security-incident"></a>¿Qué es un incidente de seguridad?

Microsoft define un incidente de seguridad en su servicios en línea como una vulneración de seguridad confirmada que conduce a la destrucción accidental o ilegal, pérdida, modificación, divulgación no autorizada o acceso a datos de clientes o datos personales mientras Microsoft los procesa. Por ejemplo, el acceso no autorizado a la infraestructura de servicios en línea de Microsoft y la filtración de datos de clientes constituirían un incidente de seguridad, mientras que los eventos de cumplimiento que no afectan a la confidencialidad, integridad o disponibilidad de servicios o datos de clientes no se consideran incidentes de seguridad.

## <a name="how-does-microsoft-respond-to-security-incidents"></a>¿Cómo responde Microsoft a los incidentes de seguridad?

Siempre que haya un incidente de seguridad, Microsoft se esfuerza por responder de forma rápida y eficaz para proteger los servicios Microsoft y los datos de los clientes. Microsoft emplea una estrategia de respuesta a incidentes diseñada para investigar, contener y eliminar amenazas de seguridad de forma rápida y eficaz.

Los servicios en la nube de Microsoft se supervisan continuamente en busca de signos de peligro. Además de la supervisión y alertas de seguridad automatizadas, todos los empleados reciben formación anual para reconocer e informar de posibles incidentes de seguridad. Cualquier actividad sospechosa detectada por empleados, clientes o herramientas de supervisión de seguridad se escala a equipos de respuesta de seguridad específicos del servicio para su investigación. Todos los equipos de operaciones de servicio, incluidos los equipos de respuesta de seguridad específicos del servicio, mantienen una rotación de llamada profunda para garantizar que los recursos estén disponibles para la respuesta a incidentes 24x7x365. Nuestras rotaciones de llamada permiten a Microsoft montar una respuesta eficaz a incidentes en cualquier momento o escala, incluidos los eventos extendidos o simultáneos.

Cuando se detecta y aumenta la actividad sospechosa, los equipos de respuesta de seguridad específicos del servicio inician un proceso de análisis, contención, eliminación **y recuperación.** Estos equipos coordinan el análisis del posible incidente para determinar su ámbito, incluido cualquier impacto para los clientes o los datos de los clientes. Basándose en este análisis, los equipos de respuesta de seguridad específicos del servicio trabajan con equipos de servicio afectados para desarrollar un plan para contener la amenaza y minimizar el impacto del incidente, eliminar la amenaza del entorno y recuperarse completamente en un estado seguro conocido. Los equipos de servicio relevantes implementan el plan con el apoyo de los equipos de respuesta de seguridad específicos del servicio para asegurarse de que la amenaza se elimina correctamente y los servicios afectados se someten a una recuperación completa.

Una vez resuelto un incidente, los equipos de servicio implementan las lecciones aprendidas del incidente para prevenir, detectar y responder mejor a incidentes similares en el futuro. Seleccione los incidentes de seguridad, especialmente los que afectan al cliente o resultan en una vulneración de datos, se someten a un incidente completo después de la mortem. El análisis posterior está diseñado para identificar los errores técnicos, los errores de procedimientos, los errores manuales y otros errores de proceso que podrían haber contribuido al incidente o que se identificaron durante el proceso de respuesta a incidentes. Las mejoras identificadas durante la post mortem se implementan con la coordinación de los equipos de respuesta de seguridad específicos del servicio para ayudar a evitar incidentes futuros y mejorar las capacidades de detección y respuesta.

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>¿Cómo y cuándo se notifica a los clientes de incidentes de seguridad o privacidad?

Siempre que Microsoft tenga conocimiento de una vulneración de la seguridad que implique pérdida, divulgación o modificación no autorizada de datos de clientes, Microsoft notifica a los clientes afectados en un plazo de 72 horas, tal como se describe en el Anexo de protección de datos (DPA) de los Términos de servicios en línea (OST). El compromiso de escala de tiempo de notificación comienza cuando se produce la declaración oficial de incidentes de seguridad. Tras declarar un incidente de seguridad, el proceso de notificación se produce lo más rápido posible, sin retrasos innecesarios.

Las notificaciones incluyen una descripción de la naturaleza de la infracción, el impacto aproximado del usuario y los pasos de mitigación (si procede). Si la investigación de Microsoft no se completa en el momento de la notificación inicial, la notificación también indicará los siguientes pasos y escalas de tiempo para la comunicación posterior.

Si un cliente tiene conocimiento de un incidente que podría tener un impacto en Microsoft, incluido, entre otros, una infracción de datos, el cliente es responsable de notificar inmediatamente a Microsoft del incidente tal como se define en el DPA.

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y certificaciones externas. Consulte la siguiente tabla para la validación de controles relacionados con la administración de incidentes.

### <a name="azure-and-dynamics-365"></a>Azure y Dynamics 365

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: Administración de incidentes y mejoras de seguridad de la información | 2 de diciembre de 2021 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: Administración de incidentes y mejoras de seguridad de la información | 2 de diciembre de 2021 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: Notificación de una vulneración de datos que implica PII  | 2 de diciembre de 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | IM-1: marco de administración de incidentes <br> IM-2: Mecanismos de detección y alertas <br> IM-3: Ejecución de respuesta a incidentes <br> IM-4: Incidentes post mortems <br> IM-6: Prueba de respuesta a incidentes <br> OA-7: acceso de ingeniero de llamada | 31 de marzo de 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CCM-9: Procedimientos forenses <br> CUEC: Informes de incidentes <br> IM-1: marco de administración de incidentes <br> IM-2: Mecanismos de detección y alertas <br> IM-3: Ejecución de respuesta a incidentes <br> IM-4: Incidentes post mortems <br> IM-6: Prueba de respuesta a incidentes <br> OA-7: acceso de ingeniero de llamada <br> SOC2-6: Sitio web de soporte al cliente <br> SOC2-9: Paneles de servicio | 31 de marzo de 2021 |

### <a name="office-365"></a>Office 365

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | IR-4: Control de incidentes <br> IR-6: Informes de incidentes <br> IR-8: Plan de respuesta a incidentes | 24 de septiembre de 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: Administración de incidentes y mejoras de seguridad de la información | 20 de abril de 2021 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: Notificación de una vulneración de datos que implica PII  | 20 de abril de 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-26: Informes de incidentes de seguridad <br> CA-47: Respuesta a incidentes | 24 de diciembre de 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-12: Acuerdos de nivel de servicio (SLA) <br> CA-13: Guías de respuesta a incidentes <br> CA-15: Notificaciones de estado del servicio  <br>  <br> CA-26: Informes de incidentes de seguridad <br> CA-29: Ingenieros de llamadas <br> CA-47: Respuesta a incidentes | 24 de diciembre de 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: Informar de incidentes  | 24 de diciembre de 2020  |

## <a name="resources"></a>Recursos

- [Términos de Online Services (OST)](https://www.microsoft.com/licensing/product-licensing/products)
- [Addendum de protección de datos (DPA)](https://www.microsoft.com/licensing/product-licensing/products)
- [Guía de implementación de administración de incidentes en la nube de Microsoft para Azure y Office 365](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365: evaluación de vulnerabilidad de terceros de Office 365 - 2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
