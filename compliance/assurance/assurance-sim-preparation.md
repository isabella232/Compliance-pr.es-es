---
title: 'Administración de incidentes de seguridad de Microsoft 365: Preparación'
description: En este artículo, se proporciona información general sobre el proceso de preparación de la administración de incidentes de seguridad en Microsoft 365.
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
hideEdit: true
ms.openlocfilehash: b3f16620564d525245c21c375bbc9a3f5b0923b7
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497388"
---
# <a name="microsoft-365-security-incident-management-preparation"></a>Administración de incidentes de seguridad de Microsoft 365: Preparación

## <a name="training-and-background-checks"></a>Comprobaciones de formación y antecedentes

Cada empleado que trabaja en Microsoft 365 tiene formación sobre incidentes de seguridad y procedimientos de respuesta adecuados para su función. Cada empleado de Microsoft 365 recibe formación al unirse y, a partir de entonces, formación anual de actualización. La formación está diseñada para proporcionar al empleado una comprensión básica del enfoque de Seguridad de Microsoft para que, una vez finalizada la formación, todos los empleados comprendan lo siguiente:

- Definición de un incidente de seguridad
- Responsabilidad de todos los empleados de informar sobre incidentes de seguridad
- Cómo escalar un posible incidente de seguridad al equipo de respuesta de seguridad de Microsoft 365
- Cómo responde el equipo de respuesta a incidentes de seguridad de Microsoft 365 a incidentes de seguridad
- Preocupaciones especiales relacionadas con la privacidad, en particular la privacidad de los clientes
- Dónde encontrar información adicional sobre seguridad y privacidad, y contactos de escalamiento
- Cualquier otra área de seguridad relevante (según sea necesario)

Los empleados adecuados reciben formación de actualización sobre seguridad anualmente. La formación de actualización anual se centra en:

- Cualquier cambio realizado en los procedimientos operativos estándar del año anterior
- Responsabilidad de todos para informar sobre incidentes de seguridad y cómo hacerlo
- Dónde encontrar información adicional sobre seguridad y privacidad, y contactos de escalamiento
- Cualquier otra área de foco de seguridad que pueda ser relevante cada año

Cada empleado que trabaja en Microsoft 365 también pasa por una comprobación de antecedentes apropiada y exhaustiva que incluye la educación, el empleo, el historial criminal del candidato y otra información específica según las normativas de Estados Unidos, como la Ley de portabilidad y responsabilidad de seguros de salud (HIPAA), el Reglamento de tráfico internacional de armas (ITAR), el Programa federal de administración de riesgos y autorización (FedRAMP) y otros.

Las comprobaciones en segundo plano son obligatorias para todos los empleados que trabajan en ingeniería de Microsoft 365. Algunos entornos y roles de operador de Microsoft 365 también pueden requerir huellas digitales completa, requisitos de ciudadanía, requisitos de autorización del gobierno y otros controles más estrictos. Además, algunos equipos de servicio y roles pueden pasar por formación de seguridad especializada según sea necesario. Por último, los propios miembros del equipo de seguridad obtienen formación especializada y participación en conferencias relacionadas directamente con la seguridad. Este aprendizaje varía según la necesidad del equipo y los empleados, pero incluye cosas como conferencias del sector, conferencias internas de Microsoft Security y cursos de formación externos a través de proveedores de formación de seguridad conocidos en el sector. También tenemos artículos dedicados de formación en seguridad publicados a lo largo del año para la comunidad de seguridad en toda Microsoft y especializados para Microsoft 365 regularmente.

## <a name="penetration-testing--assessment"></a>Evaluación de pruebas & penetración

Microsoft trabaja con diversos organismos del sector y expertos en seguridad para comprender las nuevas amenazas y las tendencias en evolución. Microsoft evalúa continuamente sus propios sistemas para las vulnerabilidades y contrata a varios expertos externos independientes que hacen lo mismo.

Las pruebas realizadas para el endurecimiento del servicio en Microsoft 365 se pueden agrupar en cuatro categorías generales:

1. **Pruebas de seguridad automatizadas:** El personal interno y externo analiza periódicamente el entorno de Microsoft 365 en función de las prácticas de Microsoft SDL, los 10 principales riesgos de Open Web Application Security Project (OWASP) y las amenazas emergentes notificadas por distintos organismos del sector.
2. **Evaluaciones de vulnerabilidad:** Las interacciones formales con evaluadores independientes y de terceros validan periódicamente si los controles lógicos clave funcionan eficazmente para cumplir con las obligaciones de servicio de varios organismos reguladores. Las evaluaciones las lleva a cabo el personal certificado por el Consejo de evaluadores de seguridad éticos registrados (CREST) y se basan en los 10 riesgos principales de OWASP y otras amenazas aplicables al servicio. Se realiza un seguimiento de todas las amenazas encontradas hasta el cierre.
3. **Pruebas continuas de vulnerabilidad del sistema:** Microsoft realiza pruebas periódicas en las que los equipos intentan vulnerar el sistema mediante amenazas emergentes, amenazas mezcladas o amenazas persistentes avanzadas, mientras que otros equipos intentan bloquear dichos intentos de vulneración.
4. **Microsoft Online Services Bug Bounty Program:** este programa funciona con una directiva de permitir evaluaciones limitadas de vulnerabilidades originadas por el cliente en Microsoft 365. Para obtener más información, [consulte Microsoft Online Services Bug Bounty Terms](https://www.microsoft.com/msrc/bounty-terms).

El equipo de ingeniería de Microsoft 365 publica periódicamente diversos documentos de cumplimiento. Varios de esos documentos están disponibles en virtud de un contrato de no divulgación del Portal de confianza del servicio en la nube de [Microsoft](https://aka.ms/STP) o del área de Service Assurance del Centro de cumplimiento de [Microsoft 365](https://compliance.office.com)

>[!NOTE]
>Vea Introducción a las suscripciones del Portal de confianza de servicio para Office 365 para empresas, Azure y Dynamics CRM Online para obtener más información sobre cómo obtener acceso al Portal de confianza de servicio. Se requiere una suscripción a Microsoft 365 para tener acceso al Centro de cumplimiento de Microsoft 365.

## <a name="attack-simulation"></a>Simulación de ataque

Microsoft realiza ejercicios continuos de simulación de ataques y pruebas de penetración en sitios en directo de nuestros planes de seguridad y respuesta con el objetivo de mejorar la capacidad de detección y respuesta. Microsoft simula regularmente infracciones reales, lleva a cabo una supervisión de seguridad continua y realiza prácticas de respuesta a incidentes de seguridad para validar y mejorar la seguridad de Microsoft 365 y Azure.

Microsoft ejecuta una estrategia de seguridad de infracción con dos equipos principales:

### <a name="red-teams"></a>Equipos rojos

El equipo rojo de seguridad de Microsoft 365 es un grupo de personal de tiempo completo dentro de Microsoft que se centra en vulnerar la infraestructura, la plataforma y las propias aplicaciones y inquilinos de Microsoft. Son el adversario dedicado (un grupo de hackers éticos) que realiza ataques dirigidos y persistentes contra servicios en línea (pero no aplicaciones o datos de clientes). Proporcionan validación continua de "espectro completo" (por ejemplo, controles técnicos, directiva de papel, respuesta humana, etc.) de las capacidades de respuesta a incidentes de servicio.

### <a name="blue-teams"></a>Equipos azules

El equipo azul de seguridad de Microsoft 365 está compuesto por un conjunto dedicado de respondedores de seguridad y miembros de todos los equipos de respuesta a incidentes de seguridad, ingeniería y operaciones. Son independientes y funcionan por separado del equipo rojo. El equipo azul sigue los procesos de seguridad establecidos y usa las últimas herramientas y tecnologías para detectar y responder a ataques e intentos de penetración. Al igual que los ataques reales, el equipo azul no sabe cuándo ni cómo se producirán los ataques del equipo rojo ni qué métodos se pueden usar. Su trabajo, ya sea un ataque de equipo rojo o un ataque real, es detectar y responder a todos los incidentes de seguridad. Por este motivo, el equipo azul está de llamada continuamente y debe reaccionar a las infracciones del equipo rojo del mismo modo que lo harían con cualquier otro adversario.

Los empleados de Microsoft separan los equipos rojos a tiempo completo y los equipos azules de Microsoft en varias divisiones que realizan operaciones en todos los servicios y dentro de ellos. Denominado Red *Teaming,* el enfoque consiste en probar en todos los sistemas y operaciones de los servicios Microsoft las mismas tácticas, técnicas y procedimientos que los verdaderos adversarios, frente a la infraestructura de producción en directo, sin el conocimiento previo de los equipos de ingeniería o operaciones de infraestructura y plataforma. Esto prueba las capacidades de detección y respuesta de seguridad y ayuda a identificar vulnerabilidades de producción, errores de configuración, suposiciones no válidas u otros problemas de seguridad de forma controlada. Cada infracción del equipo rojo va seguida de una divulgación completa entre el equipo rojo y el equipo azul, incluidos los equipos de servicio, para identificar las diferencias, abordar los resultados y mejorar significativamente la respuesta a las infracciones.

>[!NOTE]
>No se ha dirigido ningún dato de cliente durante los ejercicios de selección de equipos rojos o de penetración de sitios en directo. Las pruebas se realizan con la infraestructura y plataformas de Microsoft 365 y Azure, así como con los propios inquilinos, aplicaciones y datos de Microsoft. Los inquilinos de clientes, las aplicaciones y los datos hospedados en Microsoft 365 o Azure nunca están dirigidos según las reglas de participación acordadas.

### <a name="joint-exercises"></a>Ejercicios conjuntos

En ocasiones, los equipos azul y rojo de seguridad de Microsoft 365 realizarán operaciones conjuntas en las que la relación durante la operación sea más de socio que de conflicto con un conjunto selecto de empleados de cada equipo. Estos ejercicios están bien coordinados entre los equipos para impulsar un conjunto más específico de resultados mediante la colaboración en tiempo real entre los hackers y los respondedores éticos. Estos ejercicios de "equipo púrpura" están muy adaptados para cada operación para maximizar la oportunidad, pero fundamental para cada operación es el uso compartido de información de ancho de banda alto y la asociación para lograr los objetivos.

## <a name="related-articles"></a>Artículos relacionados

- [Administración de incidentes de seguridad de Microsoft 365](assurance-security-incident-management.md)
- [Análisis y detección de incidentes de seguridad de Microsoft 365](assurance-sim-detection-analysis.md)
- [Contención, eliminación y recuperación de la administración de incidentes de seguridad de Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Actividad posterior a la incidencia de administración de incidentes de seguridad de Microsoft 365](assurance-sim-post-incident-activity.md)
