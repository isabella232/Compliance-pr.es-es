---
title: 'Administración de incidentes de seguridad de Microsoft 365: Preparación'
description: En este artículo se proporciona información general sobre el proceso de preparación de la administración de incidentes de seguridad en Microsoft 365.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: b14a9fa236cd71cff7dd02baf04a30c249bc4346
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040343"
---
# <a name="microsoft-365-security-incident-management-preparation"></a>Administración de incidentes de seguridad de Microsoft 365: Preparación

## <a name="training-and-background-checks"></a>Formación y comprobaciones de antecedentes

Cada empleado que trabaja en Microsoft 365 tiene formación sobre incidentes de seguridad y procedimientos de respuesta adecuados para su rol. Cada empleado de Microsoft 365 recibe formación al unirse y aprendizaje de actualización anual cada año a partir de entonces. El aprendizaje está diseñado para proporcionar al empleado una comprensión básica del enfoque de Microsoft en materia de seguridad para que, una vez completado el aprendizaje, todos los empleados comprendan lo siguiente:

- Definición de un incidente de seguridad
- Responsabilidad de todos los empleados de informar sobre incidentes de seguridad
- Cómo escalar un posible incidente de seguridad al equipo de respuesta de seguridad de Microsoft 365
- Cómo responde el equipo de respuesta ante incidentes de seguridad de Microsoft 365 a incidentes de seguridad
- Preocupaciones especiales relacionadas con la privacidad, especialmente la privacidad de los clientes
- Dónde encontrar información adicional sobre seguridad y privacidad, y contactos de escalación
- Cualquier otra área de seguridad relevante (según sea necesario)

Los empleados adecuados reciben formación de actualización sobre seguridad anualmente. La formación de actualización anual se centra en:

- Cualquier cambio realizado en los procedimientos operativos estándar del año anterior
- La responsabilidad de todos los usuarios de informar sobre incidentes de seguridad y cómo hacerlo
- Dónde encontrar información adicional sobre seguridad y privacidad, y contactos de escalación
- Cualquier otra área de seguridad que pueda ser relevante cada año

Cada empleado que trabaja en Microsoft 365 también pasa por una revisión de antecedentes adecuada y exhaustiva que incluye la educación, el empleo, el historial delictivo y otra información específica del candidato según las regulaciones de los Estados Unidos, como la Ley de portabilidad y responsabilidad de seguros de salud (HIPAA), el Reglamento internacional de tráfico de armas (ITAR), el Programa federal de administración de riesgos y autorización (FedRAMP) y otros.

Las comprobaciones de antecedentes son obligatorias para todos los empleados que trabajan en ingeniería de Microsoft 365. Algunos entornos y roles de operador de Microsoft 365 también pueden requerir huellas digitales completa, requisitos de nacionalidad, requisitos de autorización del gobierno y otros controles más estrictos. Además, algunos equipos de servicio y roles pueden pasar por formación de seguridad especializada según sea necesario. Por último, los propios miembros del equipo de seguridad obtienen formación especializada y participación en conferencias relacionadas directamente con la seguridad. Esta formación varía según la necesidad del equipo y del empleado, pero incluye aspectos como conferencias del sector, conferencias internas de Seguridad de Microsoft y cursos de formación externos a través de proveedores de formación de seguridad conocidos en el sector. También disponemos de artículos dedicados de formación en seguridad publicados a lo largo del año para la comunidad de seguridad de Microsoft y especializados en Microsoft 365 periódicamente.

## <a name="penetration-testing--assessment"></a>Pruebas de penetración & evaluación

Microsoft trabaja con diversos organismos del sector y expertos en seguridad para comprender las nuevas amenazas y las tendencias en evolución. Microsoft evalúa continuamente sus propios sistemas de vulnerabilidades y contrae con diversos expertos independientes externos que hacen lo mismo.

Las pruebas realizadas para el endurecimiento del servicio en Microsoft 365 se pueden agrupar en cuatro categorías generales:

1. **Pruebas de seguridad automatizadas:** El personal interno y externo analiza periódicamente el entorno de Microsoft 365 en función de las prácticas de la SDL de Microsoft, los 10 riesgos principales de Open Web Application Security Project (OWASP) y las amenazas emergentes notificadas por distintos organismos del sector.
2. **Evaluaciones de vulnerabilidad:** Las interacciones formales con evaluadores independientes y de terceros validan periódicamente si los controles lógicos clave funcionan de forma eficaz para cumplir las obligaciones de servicio de los distintos organismos reguladores. Las evaluaciones las lleva a cabo el personal certificado por el Consejo de evaluadores de seguridad éticos registrados (CREST) y se basan en los 10 riesgos principales de OWASP y otras amenazas aplicables al servicio. Se realiza un seguimiento de todas las amenazas encontradas hasta el cierre.
3. **Pruebas continuas de vulnerabilidad del sistema:** Microsoft realiza pruebas periódicas en las que los equipos intentan vulnerar el sistema mediante amenazas emergentes, amenazas mezcladas o amenazas persistentes avanzadas, mientras que otros equipos intentan bloquear dichos intentos de infracción.
4. **Microsoft Online Services programa de** corrección de errores: este programa opera una directiva que permite evaluaciones limitadas de vulnerabilidades originadas por el cliente en Microsoft 365. Para obtener más información, [vea Microsoft Online Services términos de error.](https://www.microsoft.com/msrc/bounty-terms)

El equipo de ingeniería de Microsoft 365 publica periódicamente diversos documentos de cumplimiento. Varios de esos documentos están disponibles en virtud de un acuerdo de confidencialidad desde el Portal de confianza del servicio en la nube de [Microsoft](https://aka.ms/STP) o desde el área de Garantía de servicios del Centro de cumplimiento de [Microsoft 365](https://compliance.office.com)

>[!NOTE]
>Consulte Introducción al Portal de confianza de servicios para suscripciones de Office 365 para empresas, Azure y Dynamics CRM Online para obtener más información sobre cómo obtener acceso al Portal de confianza de servicios. Se requiere una suscripción de Microsoft 365 para acceder al Centro de cumplimiento de Microsoft 365.

## <a name="attack-simulation"></a>Simulación de ataque

Microsoft participa en ejercicios continuos de simulación de ataques y pruebas de penetración en sitios en directo de nuestros planes de seguridad y respuesta con el objetivo de mejorar la capacidad de detección y respuesta. Microsoft simula regularmente infracciones del mundo real, lleva a cabo una supervisión de seguridad continua y realiza prácticas de respuesta a incidentes de seguridad para validar y mejorar la seguridad de Microsoft 365 y Azure.

Microsoft ejecuta una estrategia de seguridad contra infracciones de seguridad con dos equipos principales:

### <a name="red-teams"></a>Equipos rojos

El equipo rojo de seguridad de Microsoft 365 es un grupo de personal de tiempo completo dentro de Microsoft que se centra en vulnerar la infraestructura, la plataforma y los propios inquilinos y aplicaciones de Microsoft. Son el adversario dedicado (un grupo de hackers éticos) que realiza ataques dirigidos y persistentes contra servicios en línea (pero no aplicaciones o datos de clientes). Proporcionan validación continua de "espectro completo" (por ejemplo, controles técnicos, directiva de papel, respuesta humana, etc.) de las capacidades de respuesta a incidentes de servicio.

### <a name="blue-teams"></a>Equipos azules

El equipo azul de seguridad de Microsoft 365 está compuesto por un conjunto dedicado de respondedores de seguridad y miembros de todos los equipos de respuesta, ingeniería y operaciones ante incidentes de seguridad. Son independientes y funcionan por separado del equipo rojo. El equipo azul sigue los procesos de seguridad establecidos y usa las herramientas y tecnologías más recientes para detectar y responder a ataques e intentos de penetración. Al igual que los ataques reales, el equipo azul no sabe cuándo ni cómo se producirán los ataques del equipo rojo ni qué métodos se pueden usar. Su trabajo, ya sea un ataque de equipo rojo o un ataque real, es detectar y responder a todos los incidentes de seguridad. Por este motivo, el equipo azul está de llamada continuamente y debe reaccionar ante las infracciones del equipo rojo de la misma manera que lo haría con cualquier otro adversario.

Los miembros del personal de Microsoft separan los equipos rojos a tiempo completo y los equipos azules de Microsoft en distintas divisiones que realizan operaciones en todos los servicios y dentro de ellos. Denominado Red *Teaming*, el enfoque consiste en probar los sistemas y operaciones de los servicios Microsoft con las mismas tácticas, técnicas y procedimientos que los adversarios reales, frente a la infraestructura de producción en directo, sin el conocimiento previo de los equipos de ingeniería o operaciones de infraestructura y plataforma. Esto prueba la detección de seguridad y las capacidades de respuesta, y ayuda a identificar vulnerabilidades de producción, errores de configuración, suposiciones no válidas u otros problemas de seguridad de forma controlada. Cada infracción del equipo rojo va seguida de una divulgación completa entre el equipo rojo y el equipo azul, incluidos los equipos de servicio, para identificar las diferencias, abordar los resultados y mejorar significativamente la respuesta a las infracciones.

>[!NOTE]
>No se dirigirá ningún dato de cliente durante los ejercicios de penetración de red teaming o live site. Las pruebas están en contra de la infraestructura y plataformas de Microsoft 365 y Azure, así como de los propios inquilinos, aplicaciones y datos de Microsoft. Los inquilinos de clientes, las aplicaciones y los datos hospedados en Microsoft 365 o Azure nunca se dirigirán según las reglas de participación acordadas.

### <a name="joint-exercises"></a>Ejercicios conjuntos

En ocasiones, los equipos de seguridad azul y rojo de Microsoft 365 realizarán operaciones conjuntas en las que la relación durante la operación sea más asociada que adversaria con un conjunto selecto de empleados de cada equipo. Estos ejercicios están bien coordinados entre los equipos para impulsar un conjunto más específico de resultados a través de la colaboración en tiempo real entre hackers y respondedores de datos éticos. Estos ejercicios de "equipo púrpura" están muy adaptados para cada operación a fin de maximizar la oportunidad, pero fundamental para cada operación es el uso compartido de información de ancho de banda alto y la asociación para lograr los objetivos.

## <a name="related-articles"></a>Artículos relacionados

- [Administración de incidentes de seguridad de Microsoft 365](assurance-security-incident-management.md)
- [Análisis y detección de administración de incidentes de seguridad de Microsoft 365](assurance-sim-detection-analysis.md)
- [Contención, reactivación y recuperación de la administración de incidentes de seguridad de Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Actividad posterior a la incidencia de administración de incidentes de seguridad de Microsoft 365](assurance-sim-post-incident-activity.md)
