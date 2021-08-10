---
title: Resiliencia y continuidad
description: Obtenga información sobre la resistencia y la continuidad en Microsoft 365
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
ms.openlocfilehash: 9fb013647bc558856f7005c2d5e1ccdb656db9b9b04ceb5882df35a599e7ebff
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292168"
---
# <a name="resiliency-and-continuity-overview"></a>Información general sobre la resiliencia y la continuidad

## <a name="how-does-microsoft-ensure-business-continuity-if-a-disaster-or-other-threat-to-service-availability-occurs"></a>¿Cómo garantiza Microsoft la continuidad empresarial si se produce un desastre u otra amenaza para la disponibilidad del servicio?

El equipo Enterprise administración de continuidad empresarial (EBCM) de Microsoft supervisa la administración de continuidad empresarial y las actividades de recuperación ante desastres en servicios Microsoft y ofertas en la nube. Los representantes de las unidades de negocio de Microsoft se coordinan con el equipo ebcm para desarrollar planes de continuidad empresarial y validar el cumplimiento de los requisitos de continuidad empresarial.

El ciclo de vida de administración de continuidad empresarial (BCM) es el núcleo de nuestra metodología BCM. Este proceso de tres fases está diseñado para ser adaptable para que pueda implementarse mediante una amplia variedad de modelos de negocio en Microsoft. Comienza con una fase **de** evaluación para identificar los procesos y objetivos críticos que deben incluirse en el programa de continuidad empresarial. La fase de evaluación también requiere un análisis de impacto empresarial (BIA). La **fase de** planeación se centra en desarrollar e implementar estrategias de recuperación y resistencia y documentarlas en planes oficiales de continuidad empresarial. Por último, **la validación de capacidad** prueba los planes de continuidad empresarial y sus implementaciones para comprobar la eficacia e identificar posibles mejoras.

Las estrategias de continuidad empresarial de los servicios en línea de Microsoft usan redundancia de hardware, red y centros de datos. La replicación de datos entre centros de datos proporciona alta disponibilidad y confiabilidad durante un incidente catastrófico. También aumenta la resistencia a incidentes mundanos, como errores aislados de hardware o daños en los datos.

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>¿Cómo prueba Microsoft la continuidad empresarial y los planes de recuperación ante desastres?

La directiva Enterprise Administración de continuidad empresarial (EBCM) de Microsoft estipula que todos los planes de continuidad empresarial y recuperación ante desastres de Microsoft deben probarse, actualizarse y revisarse anualmente. Los servicios en línea de Microsoft prueban sus planes de continuidad empresarial al menos anualmente según las directivas de EBCM. Después de crear y revisar los informes de acción para validar, pruebe los resultados e informe a las actualizaciones del plan en respuesta a los problemas detectados durante las pruebas.

Para validar las estrategias de resistencia y recuperación frente a una amplia gama de posibles incidentes, el programa EBCM define varias categorías de escenarios de prueba que afectan a las personas, las ubicaciones y la tecnología. El nivel de validación requerido para cada servicio se basa en la importancia del servicio, y los servicios más críticos reciben una validación más rigurosa. Cada equipo de servicio en línea de Microsoft prueba su plan de continuidad empresarial de acuerdo con las directrices de EBCM para medir la eficacia del plan y la preparación del equipo de servicio para ejecutar el plan.

Según las directrices de EBCM, las revisiones anuales de los planes de continuidad empresarial y la validación de capacidades deben tener lugar dentro de los 12 meses siguientes a la última revisión. La validación de capacidad debe incluir la revisión de la documentación de soporte técnico, como BIA, para garantizar que sigue siendo precisa. Microsoft pone a disposición de nuestros clientes los resultados de validación de funcionalidades para algunos servicios en línea de Microsoft a través de informes trimestrales.

## <a name="how-do-microsoft-online-services-ensure-system-capacity-meets-demand"></a>¿Cómo garantizan los servicios en línea de Microsoft que la capacidad del sistema satisface la demanda?

La planeación de capacidad ayuda a los equipos de servicio a asignar los recursos necesarios para admitir la disponibilidad del servicio en línea de Microsoft. El planeamiento normal de la capacidad es necesario como parte del programa EBCM de Microsoft. Los equipos de servicio revisan los datos de capacidad durante las revisiones trimestrales y durante situaciones de emergencia que merecen más revisión de capacidad.

Cada equipo de servicio mantiene los datos sin procesar para la planeación de capacidad e incluye métricas como el procesamiento del sistema, la memoria y la capacidad de hardware. Las revisiones programadas usan un modelo de la capacidad actual del sistema y lo prueban según las necesidades proyectadas en situaciones de emergencia. Si el modelo indica deficiencias en la capacidad, los cambios propuestos en la capacidad del sistema se envían a la dirección del equipo de servicio para su revisión. Los ingenieros del equipo de servicio incorporan los cambios aprobados en un nuevo modelo antes de la implementación.

## <a name="how-do-microsoft-online-services-maintain-service-availability-during-routine-system-failures"></a>¿Cómo mantienen los servicios en línea de Microsoft la disponibilidad del servicio durante los errores rutinarios del sistema?

Los servicios en línea de Microsoft logran la resistencia del servicio a través de la arquitectura redundante, la replicación de datos y la comprobación automatizada de integridad. La arquitectura redundante implica la implementación de varias instancias de un servicio en hardware separados geográfica y físicamente, lo que proporciona mayor tolerancia a errores para los servicios en línea de Microsoft. La replicación de datos garantiza que siempre haya varias copias de datos de clientes en diferentes zonas de error, lo que permite que los datos críticos del cliente se recuperen si el cliente está dañado, perdido o incluso eliminado accidentalmente. La comprobación de integridad automatizada aumenta la disponibilidad de los datos restaurando automáticamente los datos afectados por muchos tipos de daños físicos o lógicos.

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y certificaciones externas. Consulte la siguiente tabla para la validación de controles relacionados con la resistencia y la continuidad.

### <a name="azure-and-dynamics-365"></a>Azure y Dynamics 365

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1: Continuidad de la seguridad de la información <br> A.17.2: Redundancias | 2 de diciembre de 2020 |
| [ISO 22301](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=6d388547-fc88-46e3-8de2-6bc2edc08b06&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=ee4b611b-bb4d-4056-b189-00da36e88949&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | Todos los controles | 13 de mayo de 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | BC-1: Planes de continuidad empresarial <br> BC-3: Procedimientos de continuidad empresarial y recuperación ante desastres <br> BC-4: pruebas bcdr <br> BC-7: Planes de continuidad del negocio del centro de datos <br> BC-8: Pruebas de continuidad empresarial del centro de datos <br> BC-9: Evaluación de resistencia de centros de datos <br> DS-5: Copia de seguridad de componentes de servicio clave <br> DS-6: redundancia de componentes críticos <br> DS-7: Replicación automática de datos de clientes <br> DS-8: Programación de copia de seguridad <br> DS-9: Procedimientos de restauración de copia de seguridad <br> DS-11: Copias de seguridad fuera del sitio <br> DS-14: Restauración automática de servicios al cliente | 31 de marzo de 2021 |

### <a name="office-365"></a>Office 365

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | CP-2: Plan de contingencia <br> CP-3: Curso de contingencia <br> CP-4: Pruebas del plan de contingencia <br> CP-6: sitio de almacenamiento alternativo <br> CP-7: Sitio de procesamiento alternativo <br> CP-9: Copia de seguridad del sistema de información <br> CP-10: Recuperación y reconstitución del sistema de información | 24 de septiembre de 2020 |
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1: Continuidad de la seguridad de la información <br> A.17.2: Redundancias | 20 de abril de 2021 |
| [ISO 22301](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | Todos los controles | 18 de marzo de 2019 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49: Directivas de copia de seguridad <br> CA-50: Continuidad empresarial <br> CA-51: replicación de datos | 24 de diciembre de 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-09: restauración de correo electrónico exo | 24 de diciembre de 2020 |

## <a name="resources"></a>Recursos

- [Documento técnico del programa de administración de continuidad empresarial de Microsoft Enterprise](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f)
- [Informe de validación de EBCM y plan de recuperación ante desastres de Microsoft Cloud: FY21 Q4](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=83dc940a-2078-4e14-8b7d-07128e5b453d&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>Declinación de responsabilidades legales

- [Declinación de responsabilidades de continuidad empresarial de Enterprise](assurance-ebcm-legal-disclaimer.md)