---
title: Simulación de ataques en Microsoft 365
description: En este artículo, obtenga información sobre cómo Microsoft supervisa y prueba continuamente los límites del espacio empresarial para Microsoft 365.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 940e5a4aa0a1327da6d964d9babf0ae3fb897598
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481862"
---
# <a name="attack-simulation-in-microsoft-365"></a>Simulación de ataques en Microsoft 365

Microsoft supervisa y comprueba de forma explícita las debilidades y vulnerabilidades en los límites del espacio empresarial, incluida la supervisión de intrusiones, intentos de infracción de permisos y falta de recursos. También usamos varios sistemas internos para supervisar continuamente el uso inadecuado de recursos, que, si se detecta, desencadena la limitación integrada.

Microsoft 365 sistemas de supervisión internos que supervisan continuamente cualquier error e impulsan la recuperación automatizada cuando se detecta un error. Microsoft 365 analizan las desviaciones en el comportamiento del servicio e inician procesos de recuperación automática integrados en el sistema. Microsoft 365 también usa la supervisión externa en la que se realiza la supervisión desde varias ubicaciones, tanto de servicios de terceros de confianza (para la verificación de SLA independiente) como de nuestros propios centros de datos para generar alertas. Para diagnósticos, tenemos un registro, auditoría y seguimiento amplios. El seguimiento y la supervisión pormenorizados nos ayudan a aislar problemas y a realizar un análisis de causa raíz rápido y eficaz.

Aunque Microsoft 365 tiene acciones de recuperación automatizadas siempre que sea posible, los ingenieros de Microsoft de guardia están disponibles las 24 horas del día para investigar todas las escalas de seguridad de gravedad 1 y las revisiones post mortem de cada incidente de servicio contribuyen al aprendizaje y mejora continuos. Este equipo incluye ingenieros de soporte técnico, desarrolladores de productos, jefes de programa, jefes de producto y altos directivos. Nuestros profesionales de llamadas proporcionan copias de seguridad a tiempo y a menudo pueden automatizar las acciones de recuperación, de modo que la próxima vez que se produzca un evento, se pueda sanar automáticamente.

Microsoft realiza una revisión exhaustiva después del incidente cada vez que se produce Microsoft 365 incidente de seguridad independientemente de la magnitud del impacto. Una revisión posterior al incidente consiste en un análisis de lo que sucedió, cómo respondimos y cómo evitamos incidentes similares en el futuro. En a interés de transparencia y responsabilidad, compartimos revisiones posteriores a los incidentes para cualquier incidente de servicio importante con los clientes afectados. Para obtener detalles específicos, consulte [Administración de incidentes de seguridad de Microsoft](assurance-security-incident-management.md).

## <a name="assume-breach-methodology"></a>Asumir la metodología de infracción

Basándose en un análisis detallado de las tendencias de seguridad, Microsoft aboga y destaca la necesidad de otras inversiones en tecnologías y procesos de seguridad reactivos que se centran en la detección y respuesta a amenazas emergentes, en lugar de la única prevención de dichas amenazas. Debido a los cambios en el panorama de amenazas y el análisis en profundidad, Microsoft refinó su estrategia de seguridad más allá de evitar las infracciones de seguridad a una mejor equipada para hacer frente a las infracciones cuando se producen; una estrategia que tenga en cuenta los principales eventos de seguridad no como una cuestión de si, sino de cuándo.

Aunque microsoft [](https://www.microsoft.com/TrustCenter/Security/default.aspx) asume que las prácticas de infracción se han realizado durante muchos años, muchos clientes no son conscientes del trabajo que se está haciendo en segundo plano para endurecer la nube de Microsoft. Supongamos que la infracción es una mentalidad que guía las inversiones en seguridad, las decisiones de diseño y las prácticas de seguridad operativa. Suponga que la infracción limita la confianza depositada en aplicaciones, servicios, identidades y redes tratándolos a todos,internos y externos, como inseguros y ya en peligro. Aunque la estrategia de vulneración no se sufragó por una infracción real de ninguna empresa de Microsoft o los servicios en la nube, se reconoció que muchas organizaciones, en todo el sector, se estaban vulnerando a pesar de todos los intentos de impedirlo. Aunque la prevención de infracciones es una parte crítica de las operaciones de cualquier organización, estas prácticas deben probarse y aumentarse continuamente para abordar eficazmente a los adversarios modernos y las amenazas persistentes avanzadas. Para que cualquier organización se prepare para una infracción, primero debe crear y mantener procedimientos de respuesta de seguridad robustos, repetibles y probados exhaustivamente.

Aunque los procesos de seguridad de prevención de infracciones, como el modelado de amenazas, las revisiones de código y las pruebas de seguridad son muy útiles como parte del ciclo de vida de desarrollo de [seguridad,](https://www.microsoft.com/securityengineering/sdl/)supongamos que la infracción proporciona numerosas ventajas que ayudan a tener en cuenta la seguridad general mediante el ejercicio y la medición de capacidades reactivas en caso de una infracción.

En Microsoft, nos hemos establecido para lograrlo mediante ejercicios de juegos de guerra en curso y pruebas de penetración de sitios en directo de nuestros planes de respuesta de seguridad con el objetivo de mejorar nuestra capacidad de detección y respuesta. Microsoft simula regularmente infracciones en el mundo real, realiza supervisión de seguridad continua y realiza prácticas de administración de incidentes de seguridad para validar y mejorar la seguridad de Microsoft 365, Azure y otros servicios en la nube de Microsoft.

Microsoft ejecuta su estrategia de seguridad de vulneración con dos grupos principales:

- Red Teams (atacantes)
- Azul Teams (defensores)

Tanto Microsoft Azure como Microsoft 365 personal separan red a tiempo completo Teams y azul Teams.

Denominado "Red[Teaming",](https://go.microsoft.com/fwlink/?linkid=518599)el enfoque consiste en probar sistemas y operaciones de Azure y Microsoft 365 con las mismas tácticas, técnicas y procedimientos que los verdaderos adversarios, en la infraestructura de producción en directo, sin el conocimiento previo de los equipos de ingeniería u operaciones. Esto prueba las capacidades de detección y respuesta de seguridad de Microsoft y ayuda a identificar vulnerabilidades de producción, errores de configuración, suposiciones no válidas y otros problemas de seguridad de forma controlada. Cada infracción del equipo rojo va seguida de una divulgación completa entre ambos equipos para identificar las diferencias, solucionar los hallazgos y mejorar la respuesta a las infracciones.

**NOTA:** No hay datos de cliente dirigidos deliberadamente durante las pruebas de penetración de sitios en directo o red teaming. Las pruebas están en Microsoft 365 infraestructura y plataformas de Azure, así como en los propios inquilinos, aplicaciones y datos de Microsoft. Los inquilinos de clientes, las aplicaciones y el contenido hospedado en Microsoft 365 o Azure nunca están dirigidos.

## <a name="red-teams"></a>Rojo Teams

El equipo rojo es un grupo de personal a tiempo completo dentro de Microsoft que se centra en vulnerar la infraestructura, la plataforma y las propias aplicaciones y inquilinos de Microsoft. Son el adversario dedicado (un grupo de hackers éticos) que realiza ataques dirigidos y persistentes contra Servicios en línea (infraestructura, plataformas y aplicaciones de Microsoft, pero no aplicaciones o contenido de los clientes finales).

El rol del equipo rojo es atacar y penetrar entornos con los mismos pasos que un adversario:

![Fases de vulneración](../media/office-365-isolation-breach-stages.png)

Entre otras funciones, los equipos rojos intentan específicamente vulnerar los límites de aislamiento de inquilinos para encontrar errores o vacíos en nuestro diseño de aislamiento.

Para ayudar a escalar los esfuerzos de simulación de ataques, el equipo rojo ha creado una herramienta de emulación de ataque automatizada que se ejecuta de forma segura en entornos Microsoft 365 de forma periódica. La herramienta tiene una amplia variedad de ataques predefinidos que se expanden y mejoran constantemente para ayudar a reflejar el panorama de amenazas en evolución. Además de ampliar la cobertura de las pruebas del equipo rojo, ayuda al equipo azul a validar y mejorar su lógica de supervisión de seguridad. La emulación de ataque regular y continua proporciona al equipo azul una secuencia coherente y diversa de señales que se comparan y validan con las respuestas esperadas. Esto ayuda a mejorar la lógica de Microsoft 365 de seguridad y las capacidades de respuesta.

## <a name="blue-teams"></a>Azul Teams

El equipo azul está compuesto por un conjunto dedicado de respondedores de seguridad o miembros de todas las organizaciones de respuesta a incidentes de seguridad, ingeniería y operaciones. Independientemente de su forma de hacer, son independientes y funcionan por separado del equipo rojo. El equipo azul sigue los procesos de seguridad establecidos y usa las herramientas y tecnologías más recientes para detectar y responder a los ataques y la penetración. Al igual que los ataques reales, el equipo azul no sabe cuándo ni cómo se producirán los ataques del equipo rojo ni qué métodos se pueden usar. Su trabajo, ya sea un ataque de equipo rojo o un ataque real, es detectar y responder a todos los incidentes de seguridad. Por este motivo, el equipo azul está de llamada continuamente y debe reaccionar a las infracciones del equipo rojo de la misma manera que lo harían con cualquier otra infracción.

Cuando un adversario, como un equipo rojo, ha vulnerado un entorno, el equipo azul debe:

- Recopilar evidencias dejadas por el adversario
- Detectar la evidencia como una indicación de compromiso
- Avisar a los equipos de ingeniería y operación adecuados
- Triage the alerts to determine whether they warrant further investigation
- Recopilar contexto del entorno para el ámbito de la infracción
- Crear un plan de corrección para contener o desalojar al adversario
- Ejecutar el plan de corrección y recuperarse de la infracción

Estos pasos forman la respuesta a incidentes de seguridad que se ejecuta paralela a la del adversario, como se muestra a continuación:

![Fases de respuesta a infracciones](../media/office-365-isolation-breach-response-stages.png)

Las infracciones del equipo rojo permiten ejercer la capacidad del equipo azul para detectar y responder a los ataques reales de un extremo a otro. Lo más importante es que permite una respuesta a incidentes de seguridad práctica antes de una infracción original. Además, debido a las infracciones del equipo rojo, el equipo azul mejora su conciencia situacional, que puede ser valiosa cuando se trata de infracciones futuras (ya sea del equipo rojo u otro adversario). A lo largo del proceso de detección y respuesta, el equipo azul produce inteligencia procesable y obtiene visibilidad de las condiciones reales de los entornos que están intentando defender. Con frecuencia, esto se logra a través del análisis de datos y los análisis forenses, realizados por el equipo azul, al responder a los ataques del equipo rojo y al establecer indicadores de amenazas, como indicadores de peligro. Al igual que el equipo rojo identifica las diferencias en el artículo de seguridad, los equipos azules identifican las diferencias en su capacidad para detectar y responder. Además, dado que los equipos rojos modelan ataques reales, el equipo azul puede evaluarse con precisión en función de su capacidad o incapacidad para hacer frente a los adversarios determinados y persistentes. Por último, las infracciones del equipo rojo miden la preparación y el impacto de nuestra respuesta de infracción.
