---
title: Información general sobre el desarrollo y las operaciones de seguridad
description: Obtenga más información sobre las operaciones y el desarrollo de seguridad en Microsoft 365
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
ms.openlocfilehash: 7c6752b84470eebbdb6ad78c212361156dea957b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508093"
---
# <a name="security-development-and-operations-overview"></a>Información general sobre el desarrollo y las operaciones de seguridad

## <a name="how-does-microsoft-implement-secure-development-practices"></a>¿Cómo implementa Microsoft las prácticas de desarrollo seguro?

El ciclo de vida de desarrollo de seguridad (SDL) de Microsoft es un proceso de garantía de seguridad centrado en el desarrollo y el funcionamiento de software seguro. El SDL proporciona requisitos de seguridad detallados y mensurables para que los desarrolladores e ingenieros de Microsoft reduzcan el número y la gravedad de las vulnerabilidades en nuestros productos y servicios. Todos los equipos de desarrollo de software de Microsoft deben seguir los requisitos de SDL y actualizamos continuamente SDL para reflejar el cambiante panorama de amenazas, las prácticas recomendadas del sector y los estándares normativos para el cumplimiento.

## <a name="how-does-microsofts-sdl-improve-application-security"></a>¿Cómo mejora SDL la seguridad de las aplicaciones de Microsoft?

El proceso de SDL en Microsoft se puede considerar en cinco fases de desarrollo: requisitos, diseño, implementación, comprobación y versión. Comienza por definir los requisitos de software teniendo en cuenta la seguridad. Para ello, se solicitan preguntas relevantes sobre la seguridad sobre lo que debe conseguir la aplicación. ¿La aplicación necesita recopilar datos confidenciales? ¿La aplicación realizará tareas delicadas o importantes? ¿Necesita la aplicación aceptar la entrada de orígenes que no son de confianza?

Una vez que se han identificado los requisitos de seguridad pertinentes, se diseña nuestro software para incorporar las características de seguridad que cumplan estos requisitos. Nuestros desarrolladores implementan SDL y los requisitos de diseño en el código, que comprobamos mediante la revisión manual de código, la herramienta de seguridad automatizada y las pruebas de penetración. Por último, antes de que se pueda liberar el código, las nuevas características y los cambios materiales experimentan una revisión final de seguridad y privacidad para garantizar que se cumplan todos los requisitos.

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>¿Cómo prueba Microsoft el código fuente para las vulnerabilidades comunes?

Para ayudar a nuestros desarrolladores a implementar los requisitos de seguridad durante el desarrollo del código y después de la publicación, Microsoft proporciona un conjunto de herramientas de desarrollo seguro para comprobar de forma automática el código fuente en busca de errores de seguridad y vulnerabilidades. Microsoft define y publica una lista de herramientas aprobadas que los desarrolladores deben usar, como compiladores y entornos de desarrollo, junto con las comprobaciones de seguridad integradas que se ejecutan automáticamente dentro de las canalizaciones de compilación de Microsoft. Nuestros desarrolladores usan las versiones más recientes de las herramientas aprobadas para aprovechar las nuevas características de seguridad.

Antes de que el código pueda protegerse en una bifurcación de versión, SDL requiere una revisión del código manual por un revisor independiente. Los revisores de código comprueban si hay errores de codificación y comprueban que los cambios de código satisfacen SDL y los requisitos de diseño, pasan pruebas funcionales y de seguridad, y funcionan de forma confiable. También revisan la documentación, las configuraciones y las dependencias asociadas para garantizar que los cambios en el código se documentan adecuadamente y no causan efectos secundarios no deseados. Si un revisor encuentra problemas durante la revisión del código, puede pedir al remitente que vuelva a enviar el código con los cambios sugeridos y las pruebas adicionales. Los revisores de código también pueden decidir bloquear completamente la protección del código que no cumple los requisitos. Una vez que el revisor ha considerado satisfactoriamente el código, el revisor proporciona aprobación, que es necesario para que el código pueda pasar a la siguiente fase de implementación.

Además de las herramientas de desarrollo seguras y la revisión manual del código, Microsoft pone a su aplicación los requisitos de SDL mediante herramientas de seguridad automatizadas. Muchas de estas herramientas se integran en la canalización de confirmación y analizan automáticamente el código para detectar errores de seguridad mientras se protegen y, a medida que se compilan nuevas compilaciones. Algunos ejemplos son el análisis de código estático para los errores de seguridad comunes y los analizadores de credenciales que analizan el código de secretos incrustados. Los problemas detectados por las herramientas de seguridad automatizadas deben corregirse antes de que las nuevas compilaciones puedan superar la revisión de seguridad y ser aprobadas para su lanzamiento.

## <a name="how-does-microsoft-manage-open-source-software"></a>¿Cómo administra Microsoft el software de código abierto?

Microsoft ha adoptado una estrategia de alto nivel para administrar la seguridad de código abierto, que aprovecha las herramientas y los flujos de trabajo diseñados para:

- Comprenda qué componentes de código abierto se usan en nuestros productos y servicios.
- Realizar un seguimiento de dónde y cómo se usan dichos componentes.
- Determine si esos componentes tienen alguna vulnerabilidad.
- Responder correctamente cuando se detectan puntos vulnerables que afectan a dichos componentes.

Microsoft Engineering Teams mantiene la responsabilidad de la seguridad de todo el software de código abierto incluido en un producto o servicio. Para lograr esto a escala, Microsoft ha creado capacidades esenciales en los sistemas de ingeniería a través de CG, que automatiza la detección del origen abierto, los flujos de trabajo de requisitos legales y las alertas de componentes vulnerables. Las herramientas de CG automatizadas analizan las versiones de Microsoft para los componentes de código abierto y las obligaciones legales o las vulnerabilidades de seguridad asociadas. Los componentes detectados se registran y se envían a los equipos adecuados para las revisiones de seguridad y de la empresa. Estas revisiones están diseñadas para evaluar las obligaciones legales o las vulnerabilidades de seguridad asociadas con componentes de código abierto y resolverlas antes de aprobar los componentes para la implementación.

## <a name="related-external-regulations--certifications"></a>Certificaciones & de las reglamentaciones externas relacionadas

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y las certificaciones externas. Consulte la tabla siguiente para validar los controles relacionados con el funcionamiento y el desarrollo de seguridad.

| **Auditorías externas** | **Section** | **Fecha del informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SA-3: ciclo de vida de desarrollo del sistema | 24 de septiembre de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.1.2: controles de administración de cambios <br> A. 14.2: seguridad en los procesos de desarrollo y soporte técnico | 22 de febrero de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.1.2: controles de administración de cambios <br> A. 14.2: seguridad en los procesos de desarrollo y soporte técnico | 22 de febrero de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-03: administración de riesgos <br> CA-18: administración de cambios <br> CA-19: supervisión de cambios <br> CA-21: cambiar pruebas <br> CA-38: configuraciones de línea base <br> CA-46: revisión de seguridad | 30 de septiembre de 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-03: administración de riesgos <br> CA-18: administración de cambios <br> CA-19: supervisión de cambios <br> CA-21: cambiar pruebas <br> CA-38: configuraciones de línea base <br> CA-46: revisión de seguridad | 30 de septiembre de 2019 |

## <a name="resources"></a>Recursos

- [Ciclo de vida de desarrollo de seguridad de Microsoft](https://www.microsoft.com/securityengineering/sdl)
