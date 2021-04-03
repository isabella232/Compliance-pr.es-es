---
title: 'Administración de incidentes de seguridad de Microsoft 365: Detección y análisis'
description: En este artículo, se proporciona información general sobre el proceso de análisis y detección de incidentes de seguridad en Microsoft 365.
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
ms.openlocfilehash: 433b8da98e25c4f465473143074eda055419234d
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497401"
---
# <a name="microsoft-365-security-incident-management-detection-and-analysis"></a>Administración de incidentes de seguridad de Microsoft 365: Detección y análisis

Para detectar actividad malintencionada, Microsoft 365 registra centralmente eventos de seguridad y otros datos y realiza diversas técnicas analíticas para encontrar actividad anómala o sospechosa. Los archivos de registro se recopilan de servidores y dispositivos de infraestructura de Microsoft 365 y se almacenan en una base de datos central y consolidada.

Microsoft adopta un enfoque basado en riesgos para detectar actividad malintencionada. Usamos datos de incidentes e inteligencia de amenazas para definir y priorizar nuestras detecciones.

El empleo de un equipo de personas altamente experimentados, expertos y cualificados es uno de los pilares más importantes para el éxito en la fase de detección y análisis. Microsoft 365 emplea varios equipos de servicio y estos equipos incluyen empleados con competencias en todos los componentes de la pila, incluidos la red, los enrutadores, los firewalls, los equilibradores de carga, los sistemas operativos y las aplicaciones.

Los mecanismos de detección de seguridad en Microsoft 365 también incluyen notificaciones y alertas iniciadas por diferentes orígenes. El equipo de respuesta de seguridad de Microsoft 365 es el orquestador clave del proceso de escalamiento de incidentes de seguridad. Este equipo recibe todas las escalaciones y es responsable de analizar y confirmar la validez del incidente de seguridad.

Uno de los pilares principales de la detección es la notificación:

- Cada equipo de servicio es responsable de registrar cualquier acción o evento dentro del servicio en función de los requisitos del equipo de seguridad de Microsoft 365. Todos los registros creados por los distintos equipos de servicio se procesan mediante una solución de administración de eventos y información de seguridad (SIEM) con reglas de seguridad y detección predefinidas. Estas reglas evolucionan en función de la recomendación del equipo de seguridad de Microsoft 365, con información aprendida de incidentes de seguridad anteriores, para determinar si hay alguna actividad sospechosa o malintencionada.
- Si un cliente determina que hay un incidente de seguridad en curso, puede abrir un caso de soporte técnico con Microsoft, que se asigna al equipo de comunicaciones de Experiencia del cliente (CxP) de Microsoft 365 y se convierte en una escalación para todos los equipos adecuados.

Los equipos de servicio de Microsoft 365 también usan la inteligencia obtenida en el análisis de tendencias a través de la supervisión de seguridad y el registro para detectar anomalías en sistemas de información de Microsoft 365 que puedan indicar un ataque o un incidente de seguridad. Los servidores de Microsoft 365 agregan resultados de estos registros en el entorno de producción a un servidor de registro centralizado. Desde este servidor de registro centralizado, los registros se examinan para detectar tendencias en todo el entorno de producción. Los datos agregados en el servidor centralizado se transmiten de forma segura a un servicio de registro para consultas avanzadas, creación de paneles y detección de actividad anómala y malintencionada. El servicio también usa el aprendizaje automático para detectar anomalías con la salida del registro.

Durante la fase de escalamiento y según la naturaleza del incidente de seguridad, el equipo de respuesta de seguridad de Microsoft 365 puede contratar a uno o más expertos en la materia de varios equipos de Microsoft:

- Equipo de seguridad y cumplimiento de servicios en línea
- Centro de inteligencia de amenazas de Microsoft (MSTIC)
- Centro de respuesta de seguridad de Microsoft (MSRC)
- Asuntos corporativos, externos y legales (CELA)
- Azure Security
- Ingeniería de Microsoft 365 y otros.

Antes de que se produzca cualquier escalamiento al equipo de respuesta de seguridad de Microsoft 365, el equipo de servicio es responsable de determinar y establecer el nivel de gravedad del incidente de seguridad en función de criterios definidos como:

- Privacidad
- Impacto
- Ámbito
- Número de inquilinos afectados
- Región
- Servicio
- Detalles del incidente
- Normativas específicas de mercado o sector de clientes.

La priorización de incidentes se determina mediante factores distintos, incluidos, entre otros, el impacto funcional del incidente, el impacto informativo del incidente y la capacidad de recuperación del incidente.

Después de recibir una escalada sobre un incidente de seguridad, el equipo de seguridad de Microsoft 365 organiza un equipo virtual (v-team) formado por miembros del equipo de respuesta de seguridad de Microsoft 365, los equipos de servicio y el equipo de comunicación de incidentes de Microsoft 365. La parte más compleja de las actividades de este equipo virtual es confirmar el incidente de seguridad y eliminar los falsos positivos. La precisión de la información proporcionada por los indicadores determinados en la fase de preparación es fundamental. Al analizar esta información por categoría de ataque vectorial, el equipo v puede determinar si el incidente de seguridad es una preocupación legítima.

Al principio de la investigación, el equipo de respuesta a incidentes de seguridad de Office registra toda la información sobre el incidente de acuerdo con nuestras directivas de administración de casos. A medida que avanza el caso, se realiza un seguimiento de las acciones en curso y se siguen los estándares de control de pruebas para recopilar, retener y proteger estos datos durante todo el ciclo de vida de los incidentes.

Algunos ejemplos de estas acciones incluirían:

- Un resumen, que es una breve descripción del incidente y su posible impacto
- Gravedad y prioridad del incidente, que se derivan al evaluar el impacto potencial
- Una lista de todos los indicadores identificados que llevaron a la detección del incidente
- Una lista de incidentes relacionados
- Una lista de todas las acciones realizadas por el equipo virtual
- Cualquier evidencia recopilada, que también se conservará para el análisis post mortem y futuras investigaciones forenses
- Pasos y acciones recomendados

Después de la confirmación de incidentes de seguridad, los objetivos principales del equipo de respuesta de seguridad de Microsoft 365 y el equipo de servicio adecuado son contener el ataque, proteger los servicios que se están atacando y evitar un mayor impacto global. Al mismo tiempo, los equipos de ingeniería adecuados trabajan para determinar la causa raíz y preparar el primer plan de recuperación.

En la siguiente fase, el equipo de respuesta de seguridad de Microsoft 365 identifica los clientes afectados por el incidente de seguridad, si los hay. El ámbito de efecto puede tardar algún tiempo en determinar, en función de la región, el centro de datos, el servicio, la granja de servidores, el servidor, etc. El equipo de servicio y el equipo de comunicaciones de Microsoft 365 CxP compilan la lista de clientes afectados, que a continuación administran el proceso de notificación del cliente dentro de las obligaciones contractuales y de cumplimiento.

## <a name="related-articles"></a>Artículos relacionados

- [Administración de incidentes de seguridad de Microsoft 365](assurance-security-incident-management.md)
- [Preparación de la administración de incidentes de seguridad de Microsoft 365](assurance-sim-preparation.md)
- [Contención, eliminación y recuperación de la administración de incidentes de seguridad de Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Actividad posterior a la incidencia de administración de incidentes de seguridad de Microsoft 365](assurance-sim-post-incident-activity.md)
