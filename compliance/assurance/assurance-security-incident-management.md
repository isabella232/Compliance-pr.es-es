---
title: Administración de incidentes de seguridad de Microsoft
description: En este artículo, se proporciona información general sobre el proceso de administración de incidentes de seguridad en los servicios en línea de Microsoft.
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
ms.openlocfilehash: cb9d27f02ec53c98e2f00d3106f8e4be8798d78f
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947354"
---
# <a name="microsoft-security-incident-management"></a>Administración de incidentes de seguridad de Microsoft

Microsoft trabaja continuamente para proporcionar servicios de nivel empresarial altamente seguros para los clientes de Microsoft, pero los incidentes de seguridad son una realidad inevitable que debe administrarse de forma exhaustiva y rápida. En este documento se proporciona información general sobre cómo Microsoft controla los incidentes de seguridad mediante métodos y tecnologías probados y verdaderos para minimizar su posible impacto. Un incidente de seguridad hace referencia a cualquier acceso ilegal a los datos de clientes almacenados en el equipo de Microsoft o en las instalaciones de Microsoft, o el acceso no autorizado a dichos equipos o instalaciones que pueden dar lugar a la pérdida, divulgación o alteración de los datos de los clientes. Los objetivos de Microsoft al responder a incidentes de seguridad son proteger los datos de los clientes y los servicios en línea de Microsoft.

Los equipos de seguridad de servicios en línea de Microsoft y los distintos equipos de servicio trabajan conjuntamente y toman el mismo enfoque en los incidentes de seguridad:

- Preparación
- Detección y análisis
- Contención, eliminación y recuperación
- Actividad posterior al incidente

## <a name="microsoft-approach-to-security-incident-management"></a>Enfoque de Microsoft para la administración de incidentes de seguridad

El enfoque de Microsoft para administrar un incidente de seguridad se ajusta a la Publicación especial (SP) 800-61 del Instituto Nacional de Estándares y Tecnología [(NIST).](https://www.nist.gov/) Microsoft tiene varios equipos dedicados que trabajan juntos para prevenir, supervisar, detectar y responder a incidentes de seguridad.

|**Equipo o área**|**Descripción**|
|:------------|:--------------|
| Centro de respuestas de seguridad de Microsoft | Identifica, supervisa, resuelve y responde a incidentes de seguridad y vulnerabilidades de seguridad de software de Microsoft. |
| Centro de operaciones de Cyber Defense | El Centro de operaciones de Ciberdefensa es la ubicación física que reúne a equipos de respuesta de seguridad y expertos de toda la compañía para ayudar a proteger, detectar y responder a las amenazas en tiempo real. |
| Asuntos corporativos, externos y legales | Proporciona consejos legales y normativos para un incidente de seguridad sospechoso. |
| Equipo de seguridad de Microsoft Datacenter | Equipo que se centra en los distintos servicios en inversiones comunes de ingeniería de seguridad para proteger, detectar y responder a los riesgos y amenazas de la arquitectura de servicio. |
| Equipos de respuesta de seguridad de Microsoft | Azure independiente, Dynamics 365 y Microsoft 365 de seguridad que se asocian con los equipos de servicio para crear el proceso de administración de incidentes de seguridad adecuado y para impulsar cualquier respuesta a incidentes de seguridad. |
| Equipos de Gobierno, Riesgo y Cumplimiento de Microsoft (GRC) | Proporcionar instrucciones sobre los requisitos normativos, el cumplimiento y la privacidad. |
| Equipos de servicio | Los equipos de ingeniería de Azure, Dynamics 365, Microsoft 365 responsables de las directivas y decisiones relacionadas con la seguridad de cada servicio. |
| Administradores de operaciones de Azure | Supervisa la investigación y resolución de incidentes de privacidad y seguridad relacionados con Azure. |
| Centro de inteligencia de amenazas de Microsoft (MSTIC) | Proporciona el estado actual de las amenazas de seguridad digital contra la infraestructura y los activos de Microsoft, ayuda a los equipos asociados de Microsoft a priorizar los planes de acción de mitigación y prevención y aumenta la protección mediante la adopción de la supervisión y detección de incidentes casi en tiempo real. |
| Equipos de comunicación de experiencia del cliente | Equipos de ingeniería responsables de todas las comunicaciones de clientes sobre incidentes de seguridad y servicio. Los equipos independientes están dedicados a Azure, Dynamics 365 y Microsoft 365. |

## <a name="response-management-process"></a>Proceso de administración de respuesta

Los equipos de seguridad de servicios en línea de Microsoft y los equipos de servicio trabajan juntos y toman el mismo enfoque de los incidentes de seguridad, que se basa en las fases de administración de respuesta de NIST 800-61:

- **Preparación:** se refiere a la preparación organizativa necesaria para poder responder, incluidas las herramientas, los procesos, las competencias y la preparación.
- **Análisis &** de detección: hace referencia a la actividad para detectar un incidente de seguridad en un entorno de producción y analizar todos los eventos para confirmar la autenticidad del incidente de seguridad.
- **Contención, eliminación,** recuperación: hace referencia a las acciones necesarias y apropiadas tomadas para contener el incidente de seguridad en función del análisis realizado en la fase anterior. Es posible que también sea necesario realizar más análisis en esta fase para recuperarse completamente del incidente de seguridad.
- **Actividad posterior al incidente:** hace referencia al análisis posterior a la mortem realizado después de la recuperación de un incidente de seguridad. Las acciones operativas realizadas durante el proceso se revisan para determinar si es necesario realizar cambios en las fases de preparación o detección y análisis.

![Fases de administración de incidentes de seguridad.](../media/assurance-sim-phases.png)

## <a name="federated-security-response-model"></a>Modelo de respuesta de seguridad federada

Los servicios en línea de Microsoft constan de productos principales de Microsoft, incluidos Azure, Dynamics 365 y Microsoft 365. Cada uno de estos servicios son operados por equipos independientes con sus propios procesos operativos de seguridad. Otros equipos de Microsoft, como MSTIC, también participan en diversos aspectos de seguridad de los servicios en línea de Microsoft. Debido a la gran cantidad de equipos que trabajan en la administración de operaciones de seguridad en todos los distintos servicios que formaban los servicios en línea de Microsoft, Microsoft ha implementado un modelo de respuesta de seguridad federada.

En esta tabla se presentan los límites operativos entre los distintos equipos de operaciones de seguridad del servicio en línea de Microsoft y los equipos de servicio de Microsoft:

|**Actividad**|**Operaciones del equipo de seguridad de Microsoft**|**Operaciones del equipo de servicio de Microsoft**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| Detección y análisis | - Requisitos de detección <br> - Supervisión y análisis de seguridad <br> - Barridos de indicador de compromiso (IOC) <br> - Búsqueda de infracciones <br> - 24 x 7 de seguridad en la llamada y el líder de respuesta a incidentes | - Requisitos de detección <br> - Supervisión de la implementación de infraestructura <br> - Análisis e información del servicio <br> - Triaje de eventos y alertas <br> - Ingeniería de servicio 24 x 7 de llamada  |
| Contención, eliminación, recuperación | - Lead de respuesta a incidentes <br> - Investigación forense <br> - Consultoría y experiencia en seguridad <br> - Guía de recuperación | - Propietario de incidentes de seguridad <br> - Conocimiento y experiencia del servicio <br> - Ejecutar la contención, la eliminación y la recuperación |
| Actividad posterior al incidente | - Cliente potencial de análisis posterior al incidente <br> - Recopilación de datos y archivo <br> - Lecciones aprendidas y solicitudes de errores <br> - Informes de incidentes | - Análisis de incidentes del lado del servicio <br> - Priorizar actividades de seguimiento <br> - Inversiones de seguridad de implementación <br> - Preparación de seguridad del servicio |

## <a name="related-articles"></a>Artículos relacionados

- [Administración de incidentes de seguridad de Microsoft: Preparación](assurance-sim-preparation.md)
- [Administración de incidentes de seguridad de Microsoft: detección y análisis](assurance-sim-detection-analysis.md)
- [Administración de incidentes de seguridad de Microsoft: contención, eliminación y recuperación](assurance-sim-containment-eradication-recovery.md)
- [Administración de incidentes de seguridad de Microsoft: actividad posterior al incidente](assurance-sim-post-incident-activity.md)
