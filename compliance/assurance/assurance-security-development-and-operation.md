---
title: Introducción al desarrollo y las operaciones de seguridad
description: Más información sobre el desarrollo y las operaciones de seguridad en Microsoft 365
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
ms.openlocfilehash: 916303ff2a65777785c89c6ccae70bea9a0bfda9
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787309"
---
# <a name="security-development-and-operations-overview"></a>Introducción al desarrollo y las operaciones de seguridad

## <a name="how-does-microsoft-implement-secure-development-practices"></a>¿Cómo implementa Microsoft prácticas de desarrollo seguras?

El ciclo de vida de desarrollo de seguridad (SDL) de Microsoft es un proceso de garantía de seguridad centrado en desarrollar y operar software seguro. La SDL proporciona requisitos de seguridad detallados y medibles para que los desarrolladores e ingenieros de Microsoft reduzcan el número y la gravedad de las vulnerabilidades de nuestros productos y servicios. Todos los equipos de desarrollo de software de Microsoft deben seguir los requisitos de SDL y actualizamos continuamente la SDL para reflejar el cambiante panorama de amenazas, los procedimientos recomendados del sector y los estándares normativos para el cumplimiento.

## <a name="how-does-microsofts-sdl-improve-application-security"></a>¿Cómo mejora la SDL de Microsoft la seguridad de las aplicaciones?

El proceso sdl de Microsoft se puede tener en cuenta en cinco fases de desarrollo: requisitos, diseño, implementación, comprobación y lanzamiento. Comienza definiendo los requisitos de software pensando en la seguridad. Para ello, hacemos preguntas relevantes para la seguridad sobre lo que debe lograr la aplicación. ¿La aplicación necesita recopilar datos confidenciales? ¿La aplicación realizará tareas importantes o confidenciales? ¿La aplicación necesita aceptar entradas de orígenes que no son de confianza?

Una vez identificados los requisitos de seguridad relevantes, diseñamos nuestro software para incorporar características de seguridad que cumplan estos requisitos. Nuestros desarrolladores implementan sdl y requisitos de diseño en el código, que comprobamos mediante la revisión manual del código, las herramientas de seguridad automatizadas y las pruebas de penetración. Por último, antes de que se pueda publicar el código, las nuevas características y los cambios materiales se someten a la revisión final de seguridad y privacidad para garantizar que se cumplen todos los requisitos.

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>¿Cómo prueba Microsoft el código fuente para las vulnerabilidades comunes?

Para ayudar a nuestros desarrolladores en la implementación de requisitos de seguridad durante el desarrollo de código y después del lanzamiento, Microsoft proporciona un conjunto de herramientas de desarrollo seguro para comprobar automáticamente el código fuente en busca de vulnerabilidades y defectos de seguridad. Microsoft define y publica una lista de herramientas aprobadas que nuestros desarrolladores usarán, como compiladores y entornos de desarrollo, junto con las comprobaciones de seguridad integradas que se ejecutan automáticamente en las canalizaciones de compilación de Microsoft. Nuestros desarrolladores usan las últimas versiones de las herramientas aprobadas para aprovechar las nuevas características de seguridad.

Para poder comprobar el código en una rama de versión, la SDL requiere la revisión manual del código por parte de un revisor independiente. Los revisores de código comprueban si hay errores de codificación y comprueban que los cambios de código cumplen los requisitos de sdl y diseño, pasan pruebas funcionales y de seguridad y realizan un funcionamiento confiable. También revisan la documentación, las configuraciones y las dependencias asociadas para asegurarse de que los cambios de código se documentan correctamente y no provocarán efectos secundarios no deseados. Si un revisor encuentra problemas durante la revisión del código, puede pedir al enviado que vuelva a enviar el código con los cambios sugeridos y pruebas adicionales. Los revisores de código también pueden decidir bloquear la comprobación por completo para el código que no cumple los requisitos. Una vez que el revisor considera que el código es satisfactorio, el revisor proporciona la aprobación, que es necesaria para que el código pueda pasar a la siguiente fase de implementación.

Además de las herramientas de desarrollo seguras y la revisión manual de código, Microsoft aplica los requisitos de SDL mediante herramientas de seguridad automatizadas. Muchas de estas herramientas están integradas en la canalización de confirmación y analizan automáticamente el código en busca de errores de seguridad a medida que se comprueba y se compilan nuevas compilaciones. Algunos ejemplos son el análisis de código estático para defectos comunes de seguridad y escáneres de credenciales que analizan el código de secretos incrustados. Los problemas descubiertos por las herramientas de seguridad automatizadas deben solucionarse antes de que las nuevas compilaciones puedan pasar la revisión de seguridad y aprobarse para su lanzamiento.

## <a name="how-does-microsoft-manage-open-source-software"></a>¿Cómo administra Microsoft el software de código abierto?

Microsoft ha adoptado una estrategia de alto nivel para administrar la seguridad de código abierto, que aprovecha herramientas y flujos de trabajo diseñados para:

- Comprenda qué componentes de código abierto se usan en nuestros productos y servicios.
- Realice un seguimiento de dónde y cómo se usan esos componentes.
- Determinar si esos componentes tienen vulnerabilidades.
- Responder correctamente cuando se detectan vulnerabilidades que afectan a esos componentes.

Los equipos de ingeniería de Microsoft mantienen la responsabilidad de la seguridad de todo el software de código abierto incluido en un producto o servicio. Para lograr esto a escala, Microsoft ha integrado capacidades esenciales en sistemas de ingeniería a través de CG, que automatiza la detección de código abierto, los flujos de trabajo de requisitos legales y las alertas de componentes vulnerables. Las herramientas de CG automatizadas analizan las compilaciones de Microsoft en busca de componentes de código abierto y vulnerabilidades de seguridad u obligaciones legales asociadas. Los componentes detectados se registran y envían a los equipos adecuados para las revisiones empresariales y de seguridad. Estas revisiones están diseñadas para evaluar las obligaciones legales o vulnerabilidades de seguridad asociadas con los componentes de código abierto y resolverlas antes de aprobar los componentes para su implementación.

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las certificaciones y normativas externas. Consulte la tabla siguiente para validar los controles relacionados con el desarrollo y el funcionamiento de la seguridad.

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SA-3: Ciclo de vida de desarrollo del sistema | 24 de septiembre de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Controles de administración de cambios <br> A.14.2: Seguridad en procesos de desarrollo y soporte técnico | 22 de febrero de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Controles de administración de cambios <br> A.14.2: Seguridad en procesos de desarrollo y soporte técnico | 22 de febrero de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: Administración de riesgos <br> CA-18: Administración de cambios <br> CA-19: Supervisión de cambios <br> CA-21: Pruebas de cambios <br> CA-38: Configuraciones de línea base <br> CA-46: Revisión de seguridad | 24 de diciembre de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: Administración de riesgos <br> CA-18: Administración de cambios <br> CA-19: Supervisión de cambios <br> CA-21: Pruebas de cambios <br> CA-38: Configuraciones de línea base <br> CA-46: Revisión de seguridad | 24 de diciembre de 2020 |

## <a name="resources"></a>Recursos

- [Ciclo de vida de desarrollo de seguridad de Microsoft](https://www.microsoft.com/securityengineering/sdl)
