---
title: Resistencia y continuidad
description: Obtenga más información sobre resistencia y continuidad en Microsoft 365
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
ms.openlocfilehash: 6763e363938c422ac419fe9e76f9170912627dd5
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507732"
---
# <a name="resiliency-and-continuity-overview"></a>Información general sobre resistencia y continuidad

## <a name="how-does-microsoft-ensure-business-continuity-in-the-case-of-a-disaster-or-other-threat-to-service-availability"></a>¿Cómo garantiza Microsoft la continuidad del negocio en el caso de un desastre u otra amenaza para la disponibilidad del servicio?

El equipo de administración de continuidad empresarial del negocio (EBCM) de Microsoft supervisa las actividades de recuperación ante desastres y administración de continuidad empresarial en los servicios y las ofertas de la nube de Microsoft. Los representantes de las unidades de negocio de Microsoft, como Microsoft 365, coordinan con el equipo de EBCM para desarrollar planes de continuidad del negocio y validar el cumplimiento de los requisitos de continuidad del negocio.

En el centro de nuestra metodología de administración de continuidad del negocio (BCM) se encuentra el ciclo de vida de BCM. Este proceso de tres fases está diseñado para ser adaptable, de modo que se pueda implementar mediante una amplia variedad de modelos empresariales en Microsoft. Comienza con una fase de **evaluación** para identificar los procesos y objetivos críticos que deben incluirse en el programa de continuidad del negocio. La fase de evaluación también requiere un análisis de impacto en la empresa (BIA). La fase de **planeación** se centra en el desarrollo y la implementación de estrategias de recuperación y resistencia, así como también su documentación en planes de continuidad del negocio oficiales. Por último, la **validación de capacidades** comprueba los planes de continuidad del negocio y sus implementaciones para comprobar la eficacia e identificar posibles mejoras.

La estrategia de continuidad del negocio de Microsoft 365 aprovecha el hardware, la red y la redundancia del centro de trabajo. La replicación de datos entre centros de datos proporciona alta disponibilidad y confiabilidad en caso de un incidente catastrófico. También aumenta la resistencia a incidentes más comunes, como errores de hardware aislados o daños en los datos.

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>¿Cómo prueba Microsoft probar los planes de continuidad del negocio y recuperación ante desastres?

La Directiva de administración de continuidad del negocio empresarial (EBCM) de Microsoft estipula que todos los planes de continuidad del negocio y recuperación ante desastres de Microsoft deben probarse, actualizarse y revisarse anualmente. Los servicios de Microsoft 365 prueban sus planes de continuidad del negocio al menos anualmente por las directivas de EBCM. Una vez que se han creado y revisado los informes de acciones para validar, probar los resultados e informar del plan de actualizaciones en respuesta a los problemas detectados durante las pruebas.

Para validar las estrategias de recuperación y resistencia frente a una amplia gama de posibles incidentes, el programa EBCM define varias categorías de escenarios de prueba que afectan a personas, ubicaciones y tecnología. El nivel de validación necesario para cada servicio se basa en la criticidad del servicio, con servicios más críticos que reciben una validación más rigurosa. Cada equipo de servicio de Microsoft 365 prueba su plan de continuidad empresarial de acuerdo con las directrices de EBCM para medir la eficacia del plan y la preparación del equipo de servicio para ejecutar el plan.

Según las instrucciones de EBCM, las revisiones anuales de los planes de continuidad del negocio y la validación de la capacidad deben tener lugar en un plazo de 12 meses a partir de la última revisión. La validación de la capacidad debe incluir la revisión de la documentación de soporte, como el BIA, para asegurarse de que sigue siendo precisa. Microsoft facilita los resultados de validación de capacidad para los servicios de Microsoft 365, que están disponibles para nuestros clientes a través de informes trimestrales.

## <a name="how-does-microsoft-365-ensure-system-capacity-meets-demand"></a>¿Cómo garantiza Microsoft 365 que la capacidad del sistema cumple la demanda?

La planeación de la capacidad ayuda a los equipos de servicios a asignar los recursos necesarios para admitir la disponibilidad del servicio de Microsoft 365. La planeación de capacidad normal es necesaria como parte del programa EBCM de Microsoft. Los equipos de servicios revisan los datos de capacidad durante las revisiones trimestrales, así como en situaciones de emergencia que garantizan una revisión de la capacidad adicional.

Los datos sin procesar de la planeación de capacidad los mantiene cada equipo de servicio e incluyen métricas como el procesamiento del sistema, la memoria y la capacidad de hardware. Las revisiones programadas usan un modelo de la capacidad actual del sistema y la prueban con las necesidades previstas en situaciones de emergencia. Si el modelo indica intervalos de capacidad, los cambios propuestos en la capacidad del sistema se envían al liderazgo de equipo de servicio para revisión. Los cambios aprobados se incorporan a un nuevo modelo antes de ser implementados por los ingenieros de equipo de servicio.

## <a name="how-does-microsoft-365-maintain-service-availability-during-routine-system-failures"></a>¿Cómo mantiene Microsoft 365 la disponibilidad del servicio durante los errores rutinarios del sistema?

Microsoft 365 logra la resistencia de los servicios a través de la arquitectura redundante, la replicación de datos y la comprobación de integridad automatizada. La arquitectura redundante implica la implementación de varias instancias de un servicio en hardware independiente geográficamente y físicamente, lo que proporciona mayor tolerancia a errores para los servicios de Microsoft 365. La replicación de datos garantiza que siempre haya varias copias de los datos de clientes en distintas zonas con errores, lo que permite que los datos críticos del cliente se recuperen si están dañados, se pierdan o incluso los elimine accidentalmente el cliente. La comprobación de integridad automatizada aumenta la disponibilidad de los datos mediante la restauración automática de los datos afectados por muchos tipos de daños físicos o lógicos.

## <a name="related-external-regulations--certifications"></a>Certificaciones & de las reglamentaciones externas relacionadas

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y las certificaciones externas. Consulte la tabla siguiente para validar los controles relacionados con la resistencia y la continuidad.

| **Auditorías externas** | **Section** | **Fecha del informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CP-2: Plan de contingencia <br> CP-3: aprendizaje de contingencias <br> CP-4: pruebas de planes de contingencia <br> CP-6: sitio de almacenamiento alternativo <br> CP-7: sitio de procesamiento alternativo <br> CP-9: copia de seguridad del sistema de información <br> CP-10: recuperación y reconstitución del sistema de información | 24 de septiembre de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 17.1: continuidad de la seguridad de la información <br> A. 17.2: redundancias | 22 de febrero de 2020 |
| [ISO 22301 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | Todos los controles | 18 de marzo de 2019 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-49: directivas de copia de seguridad <br> CA-50: continuidad empresarial <br> CA-51: replicación de datos | 30 de septiembre de 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-49: directivas de copia de seguridad <br> CA-50: continuidad empresarial <br> CA-51: replicación de datos | 30 de septiembre de 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-09: restauración de correo electrónico EXO | 30 de septiembre de 2019 |

## <a name="resources"></a>Recursos

- [Whitepaper del programa de administración de continuidad empresarial de empresa de Microsoft](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f) 
- [EBCM en la nube de Microsoft y informe de validación del plan de recuperación ante desastres: FY20 T4](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=5437a1d9-5883-468b-aee0-8c8a8e4ef56a&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>Renuncia legal

- [Declinación de responsabilidades de continuidad empresarial de Enterprise](assurance-ebcm-legal-disclaimer.md)