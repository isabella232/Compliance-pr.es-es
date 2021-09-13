---
title: Introducción al desarrollo y las operaciones de seguridad
description: Obtenga información sobre el desarrollo y las operaciones de seguridad en Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: b74c004e63838900f87c774a8acf84ab8aeb03d4
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160794"
---
# <a name="security-development-and-operations-overview"></a>Introducción al desarrollo y las operaciones de seguridad

## <a name="how-does-microsoft-implement-secure-development-practices"></a>¿Cómo implementa Microsoft prácticas de desarrollo seguro?

El ciclo de vida de desarrollo de seguridad (SDL) de Microsoft es un proceso de garantía de seguridad centrado en el desarrollo y el funcionamiento de software seguro. El SDL proporciona requisitos de seguridad detallados y medibles para que los desarrolladores e ingenieros de Microsoft reduzcan el número y la gravedad de las vulnerabilidades en nuestros productos y servicios. Todos los equipos de desarrollo de software de Microsoft deben cumplir los requisitos de SDL y actualizamos continuamente SDL para reflejar el panorama de amenazas cambiante, los procedimientos recomendados del sector y los estándares normativos para el cumplimiento.

## <a name="how-does-microsofts-sdl-improve-application-security"></a>¿Cómo mejora SDL de Microsoft la seguridad de las aplicaciones?

El proceso de SDL en Microsoft se puede pensar en cinco fases de desarrollo: requisitos, diseño, implementación, verificación y lanzamiento. Comienza definiendo los requisitos de software teniendo en cuenta la seguridad. Para cumplir este objetivo, le hacemos preguntas relevantes para la seguridad sobre lo que la aplicación debe lograr. ¿La aplicación necesita recopilar datos confidenciales? ¿La aplicación realizará tareas confidenciales o importantes? ¿La aplicación debe aceptar entradas de orígenes que no son de confianza?

Una vez identificados los requisitos de seguridad pertinentes, diseñamos nuestro software para incorporar características de seguridad que cumplan estos requisitos. Nuestros desarrolladores implementan el SDL y requisitos de diseño en el código, que se comprueban mediante la revisión manual del código, las herramientas de seguridad automatizadas y las pruebas de penetración. Por último, antes de que se pueda publicar el código, las nuevas características y los cambios materiales se someten a la revisión final de seguridad y privacidad para garantizar que se cumplen todos los requisitos.

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>¿Cómo prueba Microsoft el código fuente para las vulnerabilidades comunes?

Para ayudar a nuestros desarrolladores a implementar los requisitos de seguridad durante el desarrollo de código y después del lanzamiento, Microsoft proporciona un conjunto de herramientas de desarrollo seguras para comprobar automáticamente el código fuente en busca de errores y vulnerabilidades de seguridad. Microsoft define y publica una lista de herramientas aprobadas para que nuestros desarrolladores usen, como compiladores y entornos de desarrollo, junto con las comprobaciones de seguridad integradas ejecutadas automáticamente en las canalizaciones de compilación de Microsoft. Nuestros desarrolladores usan las versiones más recientes de las herramientas aprobadas para aprovechar las nuevas características de seguridad.

Para poder comprobar el código en una rama de lanzamiento, SDL requiere la revisión manual del código por parte de un revisor independiente. Los revisores de código comprueban si hay errores de codificación y comprueban que los cambios de código cumplen los requisitos de diseño y SDL, pasan pruebas funcionales y de seguridad y funcionan de forma confiable. También revisan la documentación, las configuraciones y las dependencias asociadas para asegurarse de que los cambios de código se documentan correctamente y no provocarán efectos secundarios imprescriptibles. Si un revisor encuentra problemas durante la revisión del código, puede pedir al remitente que vuelva a enviar el código con los cambios sugeridos y pruebas adicionales. Los revisores de código también pueden decidir bloquear la inserción en el repositorio por completo para el código que no cumple los requisitos. Una vez que el revisor ha considerado que el código es satisfactorio, el revisor proporciona la aprobación, que es necesaria para que el código pueda continuar con la siguiente fase de implementación.

Además de las herramientas de desarrollo seguras y la revisión manual del código, Microsoft aplica los requisitos de SDL mediante herramientas de seguridad automatizadas. Muchas de estas herramientas están integradas en la canalización de confirmación y analizan automáticamente el código en busca de defectos de seguridad a medida que se comprueba y se compilan nuevas compilaciones. Algunos ejemplos son el análisis de código estático para los defectos de seguridad comunes y los escáneres de credenciales que analizan el código para los secretos incrustados. Los problemas descubiertos por las herramientas de seguridad automatizadas deben solucionarse antes de que las nuevas compilaciones puedan pasar la revisión de seguridad y se aprueben para su lanzamiento.

## <a name="how-does-microsoft-manage-open-source-software"></a>¿Cómo administra Microsoft el software de código abierto?

Microsoft ha adoptado una estrategia de alto nivel para administrar la seguridad de código abierto, que usa herramientas y flujos de trabajo diseñados para:

- Comprender qué componentes de código abierto se usan en nuestros productos y servicios.
- Realizar un seguimiento de dónde y cómo se usan esos componentes.
- Determinar si esos componentes tienen vulnerabilidades.
- Responder correctamente cuando se detecten vulnerabilidades que afecten a esos componentes.

Los equipos de ingeniería de Microsoft mantienen la responsabilidad de la seguridad de todo el software de código abierto incluido en un producto o servicio. Para lograr esta seguridad a escala, Microsoft ha integrado capacidades esenciales en sistemas de ingeniería a través del Gobierno de componentes (CG), que automatiza la detección de código abierto, los flujos de trabajo de requisitos legales y las alertas de componentes vulnerables. Las herramientas de CG automatizadas analizan las compilaciones de Microsoft en busca de componentes de código abierto y vulnerabilidades de seguridad u obligaciones legales asociadas. Los componentes detectados se registran y envían a los equipos adecuados para revisiones empresariales y de seguridad. Estas revisiones están diseñadas para evaluar las obligaciones legales o las vulnerabilidades de seguridad asociadas a los componentes de código abierto y resolverlas antes de aprobar los componentes para la implementación.

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y certificaciones externas. Consulte la siguiente tabla para la validación de controles relacionados con el desarrollo y la operación de seguridad.

### <a name="azure-and-dynamics-365"></a>Azure y Dynamics 365

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Controles de administración de cambios <br> A.14.2: Seguridad en procesos de desarrollo y soporte técnico | 2 de diciembre de 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Controles de administración de cambios <br> A.14.2: Seguridad en procesos de desarrollo y soporte técnico | 2 de diciembre de 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | SDL-1: metodología de ciclo de vida de desarrollo de seguridad (SDL) <br> SDL-2: Requisitos de control de seguridad documentados en las versiones <br> SDL-4: Segregación de entornos de prueba y producción <br> SDL-6: Exámenes de malware en compilaciones de código fuente <br> SDL7: revisión semesual de SDL | 31 de marzo de 2021 |

### <a name="office-365"></a>Office 365

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | SA-3: Ciclo de vida de desarrollo del sistema | 24 de septiembre de 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Controles de administración de cambios <br> A.14.2: Seguridad en procesos de desarrollo y soporte técnico | 20 de abril de 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: Administración de riesgos <br> CA-18: Administración de cambios <br> CA-19: Supervisión de cambios <br> CA-21: Pruebas de cambio <br> CA-38: Configuraciones de línea base <br> CA-46: Revisión de seguridad | 24 de diciembre de 2020 |

## <a name="resources"></a>Recursos

- [Ciclo de vida de desarrollo de seguridad de Microsoft](https://www.microsoft.com/securityengineering/sdl)
