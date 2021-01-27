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
localization_priority: Normal
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
ms.openlocfilehash: 9d38131a6ec8f3213c288d76dc3b176ceaa3aace
ms.sourcegitcommit: b06fa9f1b230fd5e470817486ea51f460f28b691
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/27/2021
ms.locfileid: "50012896"
---
# <a name="attack-simulation-in-microsoft-365"></a>Simulación de ataques en Microsoft 365

Microsoft supervisa y comprueba de forma explícita si hay puntos débiles y vulnerabilidades en los límites del espacio empresarial, incluida la supervisión de intrusiones, intentos de infracción de permisos y falta de recursos. También usamos varios sistemas internos para supervisar continuamente el uso inadecuado de recursos, que, si se detecta, desencadena la limitación integrada.

Microsoft 365 tiene sistemas de supervisión internos que supervisan continuamente cualquier error e impulsan la recuperación automatizada cuando se detecta un error. Los sistemas de Microsoft 365 analizan las desviaciones en el comportamiento del servicio e inician procesos de recuperación automática integrados en el sistema. Microsoft 365 también usa la supervisión externa en la que la supervisión se realiza desde varias ubicaciones, tanto desde servicios de terceros de confianza (para la verificación de SLA independiente) como desde nuestros propios centros de datos para generar alertas. Para diagnósticos, tenemos un registro, auditoría y seguimiento amplios. El seguimiento y la supervisión pormenorizados nos ayudan a aislar problemas y a realizar un análisis de causa raíz rápido y eficaz.

Aunque Microsoft 365 ha automatizado las acciones de recuperación siempre que sea posible, los ingenieros de Llamadas de Microsoft están disponibles las 24 horas del día para investigar todas las escalaciones de seguridad de gravedad 1, y las revisiones posteriores a cada incidente del servicio contribuyen al aprendizaje y mejora continuos. Este equipo incluye ingenieros de soporte técnico, desarrolladores de productos, administradores de programas, jefes de producto y directivos. Nuestros profesionales de llamadas proporcionan copias de seguridad a tiempo y, a menudo, pueden automatizar las acciones de recuperación para que la próxima vez que se produzca un evento, se pueda recuperar automáticamente.

Microsoft realiza una revisión exhaustiva después del incidente cada vez que se produce un incidente de seguridad de Microsoft 365 independientemente de la magnitud del impacto. Una revisión posterior al incidente consiste en un análisis de lo que sucedió, cómo respondimos y cómo evitamos incidentes similares en el futuro. En a favor de la transparencia y la responsabilidad, compartimos la revisión posterior al incidente para cualquier incidente de servicio importante con los clientes afectados. Para obtener información específica, consulte Administración de incidentes de seguridad [de Office 365.](https://aka.ms/Office365SIM)

## <a name="assume-breach-methodology"></a>Asumir la metodología de infracciones

Basándose en un análisis detallado de las tendencias de seguridad, Microsoft promueve y destaca la necesidad de otras inversiones en tecnologías y procesos de seguridad reactivos que se centran en la detección y respuesta a las amenazas emergentes, en lugar de únicamente en la prevención de dichas amenazas. Debido a los cambios en el panorama de amenazas y al análisis detallado, Microsoft refinó su estrategia de seguridad más allá de simplemente evitar infracciones de seguridad a una mejor equipado para tratar las infracciones cuando se producen; una estrategia que tenga en cuenta los eventos de seguridad principales no en cuestión de si, sino de cuándo.

Aunque las [](https://www.microsoft.com/TrustCenter/Security/default.aspx) prácticas de infracción de seguridad de Microsoft se han realizado durante muchos años, muchos clientes no son conscientes del trabajo que se está haciendo en segundo plano para endurecer la nube de Microsoft. Supongamos que Breach es una idea que guía las inversiones en seguridad, las decisiones de diseño y las prácticas de seguridad operativas. Supongamos que la infracción limita la confianza que se coloca en las aplicaciones, servicios, identidades y redes, tratándolos todos(internos y externos) como inseguros y ya comprometidos. Aunque la estrategia De asumir infracciones no fue producto de una infracción real de ninguna empresa de Microsoft o servicios en la nube, se ha reconocido que muchas organizaciones, en todo el sector, se estaban vulnerando a pesar de todos los intentos de evitarla. Aunque la prevención de infracciones es una parte fundamental de las operaciones de cualquier organización, estas prácticas deben probarse y aumentarse continuamente para abordar eficazmente los adversarios modernos y las amenazas persistentes avanzadas. Para que cualquier organización se prepare para una infracción, primero debe crear y mantener procedimientos de respuesta de seguridad sólidos, repetibles y probados exhaustivamente.

Aunque los procesos de seguridad de Prevención de infracciones, como el modelado de amenazas, las revisiones de código y las pruebas de seguridad son muy útiles como parte del ciclo de vida de desarrollo de [seguridad,](https://www.microsoft.com/securityengineering/sdl/)La infracción supone numerosas ventajas que ayudan a tener en cuenta la seguridad general mediante el ejercicio y la medición de capacidades reactivas en caso de una infracción.

En Microsoft, nos hemos establecido para lograr esto a través de ejercicios de juegos bélicos continuos y pruebas de penetración en sitios en directo de nuestros planes de respuesta de seguridad con el objetivo de mejorar nuestra capacidad de detección y respuesta. Microsoft simula regularmente infracciones del mundo real, lleva a cabo una supervisión de seguridad continua y realiza prácticas de administración de incidentes de seguridad para validar y mejorar la seguridad de Microsoft 365, Azure y otros servicios en la nube de Microsoft.

Microsoft ejecuta su estrategia de seguridad de asumación de infracciones mediante dos grupos principales:

- Equipos rojos (atacantes)
- Equipos azules (defenders)

Tanto el personal de Microsoft Azure como el de Microsoft 365 separan los equipos rojos a tiempo completo y los equipos azules.

Denominado "Equipo[rojo",](https://go.microsoft.com/fwlink/?linkid=518599)el enfoque consiste en probar sistemas y operaciones de Azure y Microsoft 365 con las mismas tácticas, técnicas y procedimientos que los adversarios reales, frente a la infraestructura de producción en directo, sin el conocimiento previo de los equipos de ingeniería u operaciones. Esto prueba las capacidades de respuesta y detección de seguridad de Microsoft y ayuda a identificar vulnerabilidades de producción, errores de configuración, suposiciones no válidas y otros problemas de seguridad de forma controlada. Cada infracción de equipo rojo va seguida de una divulgación completa entre ambos equipos para identificar las diferencias, abordar los resultados y mejorar la respuesta a las infracciones.

**NOTA:** no se ha dirigido deliberadamente ningún dato de cliente durante las pruebas de penetración de red teaming o live site. Las pruebas están en contra de la infraestructura y plataformas de Microsoft 365 y Azure, así como de los propios inquilinos, aplicaciones y datos de Microsoft. Los inquilinos, las aplicaciones y el contenido de los clientes hospedados en Microsoft 365 o Azure nunca están destinados.

## <a name="red-teams"></a>Equipos rojos

El equipo rojo es un grupo de personal de tiempo completo de Microsoft que se centra en vulnerar la infraestructura, la plataforma y las propias aplicaciones y inquilinos de Microsoft. Son el adversario dedicado (un grupo de hackers éticos) que realiza ataques dirigidos y persistentes contra Servicios en línea (infraestructura, plataformas y aplicaciones de Microsoft, pero no las aplicaciones o el contenido de los clientes finales).

El rol del equipo rojo es atacar y penetrar entornos con los mismos pasos que un adversario:

![Fases de infracción](../media/office-365-isolation-breach-stages.png)

Entre otras funciones, los equipos rojos intentan específicamente vulnerar los límites de aislamiento del espacio empresarial para encontrar errores o diferencias en nuestro diseño de aislamiento.

## <a name="blue-teams"></a>Equipos azules

El equipo azul está compuesto por un conjunto dedicado de respondedores de seguridad o miembros de las organizaciones de respuesta a incidentes de seguridad, ingeniería y operaciones. Independientemente de su forma de hacer, son independientes y funcionan por separado del equipo rojo. El equipo azul sigue los procesos de seguridad establecidos y usa las herramientas y tecnologías más recientes para detectar y responder a ataques y penetración. Al igual que los ataques reales, el equipo azul no sabe cuándo ni cómo se producirán los ataques del equipo rojo ni qué métodos se pueden usar. Su trabajo, ya sea un ataque de equipo rojo o un ataque real, es detectar y responder a todos los incidentes de seguridad. Por este motivo, el equipo azul está de llamada continuamente y debe reaccionar ante las infracciones del equipo rojo de la misma manera que lo haría con cualquier otra infracción.

Cuando un adversario, como un equipo rojo, ha infringido un entorno, el equipo azul debe:

- Recopilar evidencias dejadas por el adversario
- Detectar las pruebas como una indicación de peligro
- Avisar al equipo o equipos de ingeniería y operación adecuados
- Triage the alerts to determine whether they warrant further investigation
- Recopilar contexto del entorno para el ámbito de la infracción
- Crear un plan de corrección para contener o desalojar al adversario
- Ejecutar el plan de corrección y recuperarse de una infracción

Estos pasos forman la respuesta a incidentes de seguridad que se ejecuta en paralelo con la del adversario, como se muestra a continuación:

![Fases de respuesta a infracciones](../media/office-365-isolation-breach-response-stages.png)

Las infracciones del equipo rojo permiten ejercer la capacidad del equipo azul para detectar y responder a ataques reales de un extremo a otro. Lo más importante es que permite una respuesta a incidentes de seguridad práctica antes de una infracción original. Además, debido a las infracciones del equipo rojo, el equipo azul mejora su conciencia de situación, lo que puede ser útil cuando se trata de infracciones futuras (ya sea del equipo rojo u otro adversario). A lo largo del proceso de detección y respuesta, el equipo azul genera inteligencia procesable y obtiene visibilidad de las condiciones reales de los entornos que están intentando defender. Esto suele realizarse mediante análisis de datos y análisis forenses, realizados por el equipo azul, al responder a ataques de equipo rojo y estableciendo indicadores de amenazas, como indicadores de peligro. Al igual que el modo en que el equipo rojo identifica las diferencias en la historia de seguridad, los equipos azules identifican las diferencias en su capacidad de detectar y responder. Además, dado que los equipos rojos modelan ataques reales, el equipo azul puede evaluarse con precisión sobre su capacidad o incapacidad para enfrentarse a adversarios determinados y persistentes. Por último, las infracciones del equipo rojo miden la preparación y el impacto de nuestra respuesta a las infracciones.
