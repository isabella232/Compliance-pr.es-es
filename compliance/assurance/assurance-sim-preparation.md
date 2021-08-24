---
title: 'Administración de incidentes de seguridad de Microsoft: Preparación'
description: En este artículo, se proporciona información general sobre el proceso de preparación de la administración de incidentes de seguridad en los servicios en línea de Microsoft.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: ca194511e000a7d98ddd89ae9ef85a1ee1ee01bd
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481672"
---
# <a name="microsoft-security-incident-management-preparation"></a>Administración de incidentes de seguridad de Microsoft: Preparación

## <a name="training-and-background-checks"></a>Comprobaciones de formación y antecedentes

Cada empleado que trabaja en los servicios en línea de Microsoft se proporciona formación sobre incidentes de seguridad y procedimientos de respuesta que son adecuados para su función. Cada empleado de Microsoft recibe formación al unirse y, a partir de entonces, formación anual de actualización. La formación está diseñada para proporcionar al empleado una comprensión básica del enfoque de Seguridad de Microsoft para que, una vez finalizada la formación, todos los empleados comprendan lo siguiente:

- Definición de un incidente de seguridad
- Responsabilidad de todos los empleados de informar sobre incidentes de seguridad
- Cómo escalar un posible incidente de seguridad al equipo de respuesta de seguridad de Microsoft adecuado
- Cómo responden los equipos de respuesta a incidentes de seguridad de Microsoft a incidentes de seguridad
- Preocupaciones especiales relacionadas con la privacidad, en particular la privacidad de los clientes
- Dónde encontrar información adicional sobre seguridad y privacidad, y contactos de escalamiento
- Cualquier otra área de seguridad relevante (según sea necesario)

Los empleados adecuados reciben formación de actualización sobre seguridad anualmente. La formación de actualización anual se centra en:

- Cualquier cambio realizado en los procedimientos operativos estándar del año anterior
- Responsabilidad de todos para informar sobre incidentes de seguridad y cómo hacerlo
- Dónde encontrar información adicional sobre seguridad y privacidad, y contactos de escalamiento
- Cualquier otra área de foco de seguridad que pueda ser relevante cada año

Cada empleado que trabaja en los servicios en línea de Microsoft está sujeto a una comprobación de antecedentes adecuada y exhaustiva que incluye la educación, el empleo, el historial criminal y otra información específica del candidato según las normativas de Estados Unidos, como la Ley de portabilidad y responsabilidad de seguros de salud (HIPAA), el Reglamento de tráfico internacional de armas (ITAR), el Programa federal de administración de riesgos y autorización (FedRAMP) y otros.

Las comprobaciones en segundo plano son obligatorias para todos los empleados que trabajan en ingeniería de Microsoft. Algunos entornos de servicio en línea de Microsoft y roles de operador también pueden requerir huellas digitales completa, requisitos de ciudadanía, requisitos de autorización del gobierno y otros controles más estrictos. Además, algunos equipos de servicio y roles pueden pasar por formación de seguridad especializada según sea necesario. Por último, los propios miembros del equipo de seguridad obtienen formación especializada y participación en conferencias relacionadas directamente con la seguridad. Este aprendizaje varía según la necesidad del equipo y los empleados, pero incluye cosas como conferencias del sector, conferencias internas de Microsoft Security y cursos de formación externos a través de proveedores de formación de seguridad conocidos en el sector. También tenemos artículos dedicados de formación en seguridad publicados a lo largo del año para la comunidad de seguridad en toda Microsoft y especializados en los servicios en línea de Microsoft de forma periódica.

## <a name="penetration-testing--assessment"></a>Evaluación de pruebas & penetración

Microsoft trabaja con diversos organismos del sector y expertos en seguridad para comprender las nuevas amenazas y las tendencias en evolución. Microsoft evalúa continuamente sus propios sistemas para las vulnerabilidades y contrata a varios expertos externos independientes que hacen lo mismo.

Las pruebas realizadas para el endurecimiento del servicio en los servicios en línea de Microsoft se pueden agrupar en cuatro categorías generales:

1. **Pruebas de seguridad automatizadas:** El personal interno y externo analiza periódicamente los entornos de servicio en línea de Microsoft en función de las prácticas de Microsoft SDL, los 10 principales riesgos de Open Web Application Security Project (OWASP) y las amenazas emergentes notificadas por distintos organismos del sector.
2. **Evaluaciones de vulnerabilidad:** Las interacciones formales con evaluadores independientes y de terceros validan periódicamente si los controles lógicos clave funcionan eficazmente para cumplir con las obligaciones de servicio de varios organismos reguladores. Las evaluaciones las lleva a cabo el personal certificado por el Consejo de evaluadores de seguridad éticos registrados (CREST) y se basan en los 10 riesgos principales de OWASP y otras amenazas aplicables al servicio. Se realiza un seguimiento de todas las amenazas encontradas hasta el cierre.
3. **Pruebas continuas de vulnerabilidad del sistema:** Microsoft realiza pruebas periódicas en las que los equipos intentan vulnerar el sistema mediante amenazas emergentes, amenazas mezcladas o amenazas persistentes avanzadas, mientras que otros equipos intentan bloquear dichos intentos de vulneración.
4. **Microsoft Online Services Bug Bounty Program:** este programa opera una directiva de permitir evaluaciones limitadas de vulnerabilidades originadas por el cliente en los servicios en línea de Microsoft. Para obtener más información, [consulte Microsoft Online Services Bug Bounty Terms](https://www.microsoft.com/msrc/bounty-terms).

Los equipos de ingeniería de servicios en línea de Microsoft publican periódicamente diversos documentos de cumplimiento. Varios de esos documentos están disponibles en virtud de un contrato de no divulgación del portal de confianza de [Microsoft Cloud Service](https://aka.ms/STP) o del área de Service Assurance de [la Centro de cumplimiento de Microsoft 365](https://compliance.office.com)

>[!NOTE]
>Consulte Introducción al Portal de confianza de servicio para Office 365 para empresas, Azure y suscripciones de Dynamics CRM Online para obtener más información sobre cómo obtener acceso al Portal de confianza de servicio. Se Microsoft 365 una suscripción para acceder a la Centro de cumplimiento de Microsoft 365.

## <a name="attack-simulation"></a>Simulación de ataque

Microsoft realiza ejercicios continuos de simulación de ataques y pruebas de penetración en sitios en directo de nuestros planes de seguridad y respuesta con el objetivo de mejorar la capacidad de detección y respuesta. Microsoft simula regularmente infracciones reales, lleva a cabo una supervisión de seguridad continua y realiza prácticas de respuesta a incidentes de seguridad para validar y mejorar la seguridad de los servicios en línea de Microsoft.

Microsoft ejecuta una estrategia de seguridad de infracción con dos equipos principales:

### <a name="red-teams"></a>Equipos rojos

Microsoft Red teams are groups of full-time staff within Microsoft that focus on breaching Microsoft's infrastructure, platform, and Microsoft's own tenants and applications. Son el adversario dedicado (un grupo de hackers éticos) que realiza ataques dirigidos y persistentes contra servicios en línea (pero no aplicaciones o datos de clientes). Proporcionan validación continua de "espectro completo" (por ejemplo, controles técnicos, directiva de papel, respuesta humana, etc.) de las capacidades de respuesta a incidentes de servicio.

### <a name="blue-teams"></a>Equipos azules

Los equipos de Microsoft Blue se componen de conjuntos dedicados de respondedores de seguridad y miembros de todos los equipos de respuesta a incidentes de seguridad, ingeniería y operaciones. Son independientes y funcionan por separado de los equipos rojos. Los equipos azules siguen los procesos de seguridad establecidos y usan las últimas herramientas y tecnologías para detectar y responder a ataques e intentos de penetración. Al igual que los ataques reales, los equipos azules no saben cuándo o cómo se producirán los ataques del equipo rojo ni qué métodos se pueden usar. Su trabajo, ya sea un ataque de equipo rojo o un ataque real, es detectar y responder a todos los incidentes de seguridad. Por este motivo, los equipos azules están continuamente en alerta y deben reaccionar a las infracciones del equipo rojo de la misma manera que lo harían con cualquier otro adversario.

Los empleados de Microsoft separan los equipos rojos a tiempo completo y los equipos azules de Microsoft en varias divisiones que realizan operaciones en todos los servicios y dentro de ellos. Denominado Red *Teaming,* el enfoque consiste en probar en los sistemas y operaciones de servicios Microsoft con las mismas tácticas, técnicas y procedimientos que los verdaderos adversarios, frente a la infraestructura de producción en directo, sin el conocimiento previo de los equipos de ingeniería u operaciones de la infraestructura y la plataforma. Esto prueba las capacidades de detección y respuesta de seguridad y ayuda a identificar vulnerabilidades de producción, errores de configuración, suposiciones no válidas u otros problemas de seguridad de forma controlada. Cada infracción de equipo rojo va seguida de una divulgación completa entre el equipo rojo y el equipo azul, incluidos los equipos de servicio, para identificar las diferencias, abordar los resultados y mejorar significativamente la respuesta a las infracciones.

>[!NOTE]
>No se ha dirigido ningún dato de cliente durante los ejercicios de selección de equipos rojos o de penetración de sitios en directo. Las pruebas están en Microsoft 365 infraestructura y plataformas de Azure, así como en los propios inquilinos, aplicaciones y datos de Microsoft. Los inquilinos de clientes, las aplicaciones y los datos hospedados en Azure, Dynamics 365 o Microsoft 365 nunca están dirigidos según las reglas de participación acordadas.

### <a name="joint-exercises"></a>Ejercicios conjuntos

En ocasiones, los equipos Azul y Rojo de Microsoft realizarán operaciones conjuntas en las que la relación durante la operación sea más asociada que adversaria con un conjunto selecto de empleados de cada equipo. Estos ejercicios están bien coordinados entre los equipos para impulsar un conjunto más específico de resultados mediante la colaboración en tiempo real entre los hackers y los respondedores éticos. Estos ejercicios de "equipo púrpura" están muy adaptados para cada operación para maximizar la oportunidad, pero fundamental para cada operación es el uso compartido de información de ancho de banda alto y la asociación para lograr los objetivos.

## <a name="related-articles"></a>Artículos relacionados

- [Administración de incidentes de seguridad de Microsoft](assurance-security-incident-management.md)
- [Administración de incidentes de seguridad de Microsoft: detección y análisis](assurance-sim-detection-analysis.md)
- [Administración de incidentes de seguridad de Microsoft: contención, eliminación y recuperación](assurance-sim-containment-eradication-recovery.md)
- [Administración de incidentes de seguridad de Microsoft: actividad posterior al incidente](assurance-sim-post-incident-activity.md)
- [Cómo registrar un vale de soporte de eventos de seguridad](/azure/security/fundamentals/event-support-ticket)
- [Azure y Dynamics 365 notificación de infracciones bajo el GDPR](/compliance/regulatory/gdpr-breach-azure-dynamics)