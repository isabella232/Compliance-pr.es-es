---
title: 'Administración de incidentes de seguridad de Microsoft: detección y análisis'
description: En este artículo, se proporciona información general sobre el proceso de análisis y detección de incidentes de seguridad en los servicios en línea de Microsoft.
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
ms.openlocfilehash: 9ec3e0456934c178b32a6f5fac987d70c267ef8046ff5c361abce914a2cea90a
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "54291873"
---
# <a name="microsoft-security-incident-management-detection-and-analysis"></a>Administración de incidentes de seguridad de Microsoft: detección y análisis

Para detectar actividad malintencionada, cada uno de los servicios en línea de Microsoft registra centralmente eventos de seguridad y otros datos y realiza diversas técnicas analíticas para encontrar actividad anómala o sospechosa. Los archivos de registro se recopilan de los servidores y dispositivos de infraestructura de servicios en línea de Microsoft y se almacenan en bases de datos centrales y consolidadas.

Microsoft adopta un enfoque basado en riesgos para detectar actividad malintencionada. Usamos datos de incidentes e inteligencia de amenazas para definir y priorizar nuestras detecciones.

El empleo de un equipo de personas altamente experimentados, expertos y cualificados es uno de los pilares más importantes para el éxito en la fase de detección y análisis. Microsoft emplea varios equipos de servicio que incluyen empleados con competencias en todos los componentes de la pila, incluidos la red, los enrutadores, los firewalls, los equilibradores de carga, los sistemas operativos y las aplicaciones.

Los mecanismos de detección de seguridad en los servicios en línea de Microsoft también incluyen notificaciones y alertas iniciadas por diferentes orígenes. Los equipos de respuesta de seguridad de los servicios en línea de Microsoft son los orquestadores clave del proceso de escalamiento de incidentes de seguridad. Estos equipos reciben todas las escalaciones y son responsables de analizar y confirmar la validez del incidente de seguridad.

![Flujo de trabajo de administración de incidentes de seguridad](../media/assurance-sim-workflow.png)

Uno de los pilares principales de la detección es la notificación:

- Cada equipo de servicio es responsable de registrar cualquier acción o evento dentro del servicio en función de los requisitos del equipo de seguridad del servicio en línea. Todos los registros creados por los distintos equipos de servicio se procesan mediante una solución de administración de eventos y información de seguridad (SIEM) con reglas de seguridad y detección predefinidas. Estas reglas evolucionan en función de las recomendaciones del equipo de seguridad, en la información aprendida de incidentes de seguridad anteriores, para determinar si hay alguna actividad sospechosa o malintencionada.
- Si un cliente determina que hay un incidente de seguridad en curso, puede abrir un caso de soporte técnico con Microsoft, que se asigna al equipo de comunicaciones de Microsoft y se convierte en una escalación para todos los equipos adecuados.

Los equipos de servicio de Azure, Dynamics 365 y Microsoft 365 también usan la inteligencia obtenida en el análisis de tendencias a través de la supervisión de seguridad y el registro para detectar anomalías en los sistemas de información de servicios en línea de Microsoft que pueden indicar un ataque o un incidente de seguridad. Los sistemas de servicios en línea de Microsoft agregan resultados de estos registros en el entorno de producción a servidores de registro centralizados. Desde estos servidores de registro centralizados, los registros se examinan para detectar tendencias en todo el entorno de producción. Los datos agregados en los servidores centralizados se transmiten de forma segura a un servicio de registro para consultas avanzadas, creación de paneles y detección de actividad anómala y malintencionada. El servicio también usa el aprendizaje automático para detectar anomalías con la salida del registro.

Durante la fase de escalamiento y según la naturaleza del incidente de seguridad, los equipos de respuesta de seguridad pueden contratar a uno o más expertos en la materia de varios equipos de Microsoft:

- Equipo de seguridad y cumplimiento de servicios en línea
- Centro de inteligencia de amenazas de Microsoft (MSTIC)
- Centro de respuesta de seguridad de Microsoft (MSRC)
- Asuntos corporativos, externos y legales (CELA)
- Azure Security
- Microsoft 365 ingeniería y otros.

Antes de que se produzca una escalada a cualquier equipo de respuesta de seguridad, el equipo de servicio es responsable de determinar y establecer el nivel de gravedad del incidente de seguridad en función de criterios definidos como:

- Privacidad
- Impacto
- Ámbito
- Número de inquilinos afectados
- Región
- Servicio
- Detalles del incidente
- Normativas específicas de mercado o sector de clientes.

La priorización de incidentes se determina mediante factores distintos, incluidos, entre otros, el impacto funcional del incidente, el impacto informativo del incidente y la capacidad de recuperación del incidente.

Después de recibir una escalación sobre un incidente de seguridad, el equipo de seguridad organiza un equipo virtual (v-team) formado por miembros del equipo de respuesta de seguridad del servicio en línea de Microsoft, los equipos de servicio y el equipo de comunicación de incidentes. A continuación, el equipo v debe confirmar la legitimidad del incidente de seguridad y eliminar los falsos positivos. La precisión de la información proporcionada por los indicadores determinados durante la fase de preparación es fundamental. Al analizar esta información por categoría de ataque vectorial, el equipo v puede determinar si el incidente de seguridad es una preocupación legítima.

Al principio de la investigación, el equipo de respuesta a incidentes de seguridad registra toda la información sobre el incidente de acuerdo con nuestras directivas de administración de casos. A medida que avanza el caso, se realiza un seguimiento de las acciones en curso y se siguen los estándares de control de pruebas para recopilar, retener y proteger estos datos durante todo el ciclo de vida de los incidentes.

Algunos ejemplos de estas acciones incluirían:

- Un resumen, que es una breve descripción del incidente y su posible impacto
- Gravedad y prioridad del incidente, que se derivan al evaluar el impacto potencial
- Una lista de todos los indicadores identificados que llevaron a la detección del incidente
- Una lista de cualquier incidente relacionado
- Una lista de todas las acciones realizadas por el equipo virtual
- Cualquier evidencia recopilada, que también se conservará para el análisis post mortem y futuras investigaciones forenses
- Acciones y pasos siguientes recomendados

Después de la confirmación de incidentes de seguridad, los objetivos principales del equipo de respuesta de seguridad y el equipo de servicio adecuado son contener el ataque, proteger los servicios que se están atacando y evitar un mayor impacto global. Al mismo tiempo, los equipos de ingeniería adecuados trabajan para determinar la causa raíz y preparar el primer plan de recuperación.

En la siguiente fase, el equipo de respuesta de seguridad identifica los clientes afectados por el incidente de seguridad, si los hay. El ámbito de efecto puede tardar algún tiempo en determinar, en función de la región, el centro de datos, el servicio, la granja de servidores, el servidor, etc. El equipo de servicio y el equipo de comunicaciones de Microsoft correspondiente compilan la lista de clientes afectados, que administran el proceso de notificación del cliente dentro de las obligaciones contractuales y de cumplimiento.

## <a name="related-articles"></a>Artículos relacionados

- [Administración de incidentes de seguridad de Microsoft](assurance-security-incident-management.md)
- [Administración de incidentes de seguridad de Microsoft: Preparación](assurance-sim-preparation.md)
- [Administración de incidentes de seguridad de Microsoft: contención, eliminación y recuperación](assurance-sim-containment-eradication-recovery.md)
- [Administración de incidentes de seguridad de Microsoft: actividad posterior al incidente](assurance-sim-post-incident-activity.md)
- [Cómo registrar un vale de soporte de eventos de seguridad](/azure/security/fundamentals/event-support-ticket)
- [Azure y Dynamics 365 notificación de infracciones bajo el GDPR](/compliance/regulatory/gdpr-breach-azure-dynamics)
