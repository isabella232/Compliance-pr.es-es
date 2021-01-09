---
title: Resiliencia y continuidad
description: Obtenga información sobre resistencia y continuidad en Microsoft 365
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
ms.openlocfilehash: 405c7b40a9dec01e2729b6c344dfd67502dab728
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787399"
---
# <a name="resiliency-and-continuity-overview"></a>Información general sobre la resiliencia y la continuidad

## <a name="how-does-microsoft-ensure-business-continuity-in-the-case-of-a-disaster-or-other-threat-to-service-availability"></a>¿Cómo garantiza Microsoft la continuidad empresarial en caso de desastre u otra amenaza para la disponibilidad del servicio?

El equipo de Administración de continuidad empresarial de Microsoft (EBCM) supervisa la administración de la continuidad empresarial y las actividades de recuperación ante desastres en los servicios y las ofertas en la nube de Microsoft. Los representantes de las unidades de negocio de Microsoft, como Microsoft 365, se coordinan con el equipo ebcm para desarrollar planes de continuidad empresarial y validar el cumplimiento de los requisitos de continuidad empresarial.

En el centro de nuestra metodología de Administración de continuidad empresarial (BCM) se encuentra el ciclo de vida del BCM. Este proceso de tres fases está diseñado para ser adaptable para que pueda implementarse mediante una amplia variedad de modelos de negocio en Microsoft. Comienza con una fase **de** evaluación para identificar los procesos y objetivos críticos que deben incluirse en el programa de continuidad empresarial. La fase de evaluación también requiere un análisis de impacto empresarial (BIA). La **fase de** planeación se centra en desarrollar e implementar estrategias de resistencia y recuperación, así como documentarlas en planes oficiales de continuidad empresarial. Por último, **la Validación de** capacidad prueba los planes de continuidad empresarial y sus implementaciones para comprobar la eficacia e identificar posibles mejoras.

La estrategia de continuidad empresarial de Microsoft 365 aprovecha la redundancia de hardware, red y centro de datos. La replicación de datos entre centros de datos proporciona alta disponibilidad y confiabilidad en caso de un incidente catastrófico. También aumenta la resistencia a incidentes mundanos, como errores de hardware aislados o daños en los datos.

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>¿Cómo prueba Microsoft la continuidad empresarial y los planes de recuperación ante desastres?

La directiva de Administración de continuidad empresarial de Microsoft (EBCM) estipula que todos los planes de continuidad empresarial y recuperación ante desastres de Microsoft deben probarse, actualizarse y revisarse anualmente. Los servicios de Microsoft 365 prueban sus planes de continuidad empresarial al menos una vez al año según las directivas EBCM. Después de crear y revisar los informes de acción para validar, pruebe los resultados e informe de las actualizaciones del plan en respuesta a los problemas detectados durante las pruebas.

Para validar estrategias de resistencia y recuperación frente a una amplia variedad de posibles incidentes, el programa EBCM define varias categorías de escenarios de prueba que afectan a personas, ubicaciones y tecnología. El nivel de validación necesario para cada servicio se basa en la importancia del servicio, y los servicios más críticos reciben una validación más rigurosa. Cada equipo de servicio de Microsoft 365 prueba su plan de continuidad empresarial de acuerdo con las directrices de EBCM para medir la eficacia del plan y la preparación del equipo de servicio para ejecutar el plan.

Según las directrices de EBCM, las revisiones anuales de los planes de continuidad empresarial y la validación de capacidades deben tener lugar en un plazo de 12 meses a partir de la última revisión. La validación de capacidades debe incluir la revisión de la documentación de apoyo, como BIA, para garantizar que sea precisa. Microsoft pone a disposición de nuestros clientes los resultados de validación de capacidad para seleccionar los servicios de Microsoft 365 a través de informes trimestrales.

## <a name="how-does-microsoft-365-ensure-system-capacity-meets-demand"></a>¿Cómo garantiza Microsoft 365 que la capacidad del sistema satisface la demanda?

La planeación de capacidad ayuda a los equipos de servicio a asignar los recursos necesarios para admitir la disponibilidad del servicio de Microsoft 365. Se requiere una planeación de capacidad regular como parte del programa EBCM de Microsoft. Los equipos de servicio revisan los datos de capacidad durante las revisiones trimestrales, así como durante situaciones de emergencia que justifican la revisión de capacidad adicional.

Cada equipo de servicio mantiene los datos sin procesar para la planeación de la capacidad e incluye métricas como el procesamiento del sistema, la memoria y la capacidad de hardware. Las revisiones programadas usan un modelo de capacidad actual del sistema y lo prueban con las necesidades previstas en situaciones de emergencia. Si el modelo indica diferencias en la capacidad, los cambios propuestos en la capacidad del sistema se envían a la dirección del equipo de servicio para su revisión. Los cambios aprobados se incorporan a un nuevo modelo antes de su implementación por parte de los ingenieros del equipo de servicio.

## <a name="how-does-microsoft-365-maintain-service-availability-during-routine-system-failures"></a>¿Cómo mantiene Microsoft 365 la disponibilidad del servicio durante los errores rutinarios del sistema?

Microsoft 365 logra resistencia de servicios a través de arquitectura redundante, replicación de datos y comprobación de integridad automatizada. La arquitectura redundante implica la implementación de varias instancias de un servicio en hardware separado geográfica y físicamente, lo que proporciona una mayor tolerancia a errores para los servicios de Microsoft 365. La replicación de datos garantiza que siempre hay varias copias de datos de clientes en diferentes zonas de error, lo que permite que los datos críticos de los clientes se recuperen si están dañados, perdidos o incluso eliminados accidentalmente por el cliente. La comprobación de integridad automatizada aumenta la disponibilidad de los datos mediante la restauración automática de los datos afectados por muchos tipos de daños físicos o lógicos.

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las certificaciones y normativas externas. Consulte la tabla siguiente para validar los controles relacionados con la resistencia y la continuidad.

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CP-2: Plan de contingencia <br> CP-3: Formación de contingencia <br> CP-4: Pruebas del plan de contingencia <br> CP-6: sitio de almacenamiento alternativo <br> CP-7: Sitio de procesamiento alternativo <br> CP-9: Copia de seguridad del sistema de información <br> CP-10: Recuperación y reconstitución del sistema de información | 24 de septiembre de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1: Continuidad de la seguridad de la información <br> A.17.2: Redundancias | 22 de febrero de 2020 |
| [ISO 22301 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | Todos los controles | 18 de marzo de 2019 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49: Directivas de copia de seguridad <br> CA-50: Continuidad empresarial <br> CA-51: Replicación de datos | 24 de diciembre de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49: Directivas de copia de seguridad <br> CA-50: Continuidad empresarial <br> CA-51: Replicación de datos | 24 de diciembre de 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-09: Restauración de correo electrónico EXO | 24 de diciembre de 2020 |

## <a name="resources"></a>Recursos

- [Documento técnico del Programa de administración de continuidad empresarial de Microsoft Enterprise](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f) 
- [Informe de validación del plan de recuperación ante desastres y EBCM de Microsoft Cloud: 21 trimestre y segundo trimestre](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=b4181ab3-b03d-4a62-b396-4bfd1c98ddb0&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>Declinación de responsabilidades legales

- [Declinación de responsabilidades de continuidad empresarial de Enterprise](assurance-ebcm-legal-disclaimer.md)