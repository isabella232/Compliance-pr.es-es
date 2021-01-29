---
title: Administración de incidentes de seguridad de Microsoft 365
description: En este artículo se proporciona información general sobre el proceso de administración de incidentes de seguridad en Microsoft 365.
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
- MS-Compliance0
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 9a76a258edf77708786cf19b160c4c5ee7af7ee6
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040363"
---
# <a name="microsoft-365-security-incident-management"></a>Administración de incidentes de seguridad de Microsoft 365

Microsoft trabaja continuamente para proporcionar servicios de nivel empresarial altamente seguros para los clientes de Microsoft 365. En este documento se describe cómo Microsoft controla los incidentes de seguridad en Microsoft 365. Un incidente de seguridad hace referencia a cualquier acceso ilegal a los datos de los clientes almacenados en los equipos de Microsoft o en las instalaciones de Microsoft, o el acceso no autorizado a dichos equipos o instalaciones que puedan dar lugar a la pérdida, divulgación o modificación de los datos de los clientes. Los objetivos de Microsoft al responder a incidentes de seguridad son proteger los datos de los clientes y los servicios de Microsoft 365.

El equipo de seguridad de Microsoft 365 y los distintos equipos de servicio trabajan conjuntamente y toman el mismo enfoque para los incidentes de seguridad:

- Preparación
- Detección y análisis
- Contención
- Resalte
- Recuperación
- Actividad posterior al incidente

## <a name="microsoft-approach-to-security-incident-management"></a>Enfoque de Microsoft para la administración de incidentes de seguridad

El enfoque de Microsoft para administrar un incidente de seguridad se ajusta a la publicación especial (SP) 800-61 del Instituto Nacional de Estándares y Tecnología [(NIST).](https://www.nist.gov/) Microsoft tiene varios equipos dedicados que trabajan conjuntamente para prevenir, supervisar, detectar y responder a incidentes de seguridad.

|**Equipo o área**|**Descripción**|
|:------------|:--------------|
| Centro de respuesta de seguridad de Microsoft | Identifica, supervisa, resuelve y responde a incidentes de seguridad y vulnerabilidades de seguridad de software de Microsoft. |
| Centro de operaciones de Cyber Defense | El Centro de operaciones de Cyber Defense es la ubicación física que reúne equipos de respuesta de seguridad y expertos de toda la empresa para ayudar a proteger, detectar y responder a las amenazas en tiempo real. |
| Asuntos legales, externos y corporativos | Proporciona asesoramiento legal y normativo para un supuesto incidente de seguridad. |
| Equipo de respuesta de seguridad de Microsoft 365 | Se asocia con los equipos de servicio de Microsoft 365 para crear el proceso de administración de incidentes de seguridad adecuado y para impulsar cualquier respuesta a incidentes de seguridad. |
| Confianza de Office 365 | Proporciona instrucciones sobre los requisitos normativos, el cumplimiento y la privacidad. |
| Equipo de seguridad del centro de datos de Microsoft 365 | Equipo que se centra en los distintos servicios en inversiones comunes de ingeniería de seguridad para proteger, detectar y responder a los riesgos y amenazas de la arquitectura de servicio de Microsoft 365. |
| Equipos de servicio | Equipos de ingeniería para los servicios de Microsoft 365, como Exchange, SharePoint y Microsoft Teams, que son responsables de las directivas y decisiones relacionadas con la seguridad de cada servicio. |
| Centro de inteligencia sobre amenazas de Microsoft (MSTIC) | Proporciona el estado actual de las amenazas de seguridad digital contra la infraestructura y los activos de Microsoft, ayuda a los equipos asociados de Microsoft a priorizar los planes de acción de mitigación y prevención, y aumenta la protección mediante la adopción de la detección y supervisión de incidentes casi en tiempo real. |
| Equipos de seguridad de partners | Otros equipos de seguridad de asociados dentro de Microsoft que proporcionan servicios clave o son responsables de las dependencias clave de Microsoft 365, como el equipo de respuesta de seguridad de Azure, la respuesta de seguridad de identidad y los equipos de respuesta de seguridad corporativa de Microsoft. |
| Comunicaciones de experiencia del cliente de Microsoft 365 | Equipo de ingeniería responsable de todas las comunicaciones con los clientes sobre incidentes de seguridad y servicio. |

## <a name="response-management-process"></a>Proceso de administración de respuesta

El equipo de seguridad de Microsoft 365 y los equipos de servicio trabajan juntos y toman el mismo enfoque para los incidentes de seguridad, que se basa en las fases de administración de respuesta nist 800-61:

- **Preparación:** hace referencia a la preparación de la organización necesaria para poder responder, incluidas las herramientas, los procesos, las competencias y la preparación.
- **Análisis &** de detección: hace referencia a la actividad para detectar un incidente de seguridad en un entorno de producción y analizar todos los eventos para confirmar la autenticidad del incidente de seguridad.
- **Contención, reactivación, recuperación:** hace referencia a las acciones necesarias y apropiadas tomadas para contener el incidente de seguridad en función del análisis realizado en la fase anterior. Es posible que también sea necesario realizar más análisis en esta fase para la recuperación completa del incidente de seguridad.
- **Actividad posterior al incidente:** hace referencia al análisis posterior al análisis realizado después de la recuperación de un incidente de seguridad. Las acciones operativas realizadas durante el proceso se revisan para determinar si es necesario realizar cambios en las fases de preparación o detección y análisis.

## <a name="federated-security-response-model"></a>Modelo de respuesta de seguridad federada

Los servicios de Microsoft 365 incluyen servicios en línea principales de Microsoft (Exchange, SharePoint y Microsoft Teams, etc.) y otros servicios en la nube de Microsoft, como Azure Active Directory, la Plataforma comercial de Microsoft y MSTIC. Estos servicios son operados por equipos independientes con sus propios procesos operativos de seguridad. Otros equipos de Microsoft también participan en diversos aspectos de seguridad de Microsoft 365. Debido a la gran cantidad de equipos que trabajan en la administración de operaciones de seguridad en todos los distintos servicios que forma Microsoft 365, Microsoft ha implementado un modelo de respuesta de seguridad federada.

En esta tabla se presentan los límites operativos entre los distintos equipos de operaciones de seguridad de Microsoft 365 y los equipos de servicio de Microsoft 365:

|**Actividad**|**Operaciones del equipo de seguridad de Microsoft 365**|**Operaciones del equipo de servicio de Microsoft 365**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| Detección y análisis | - Requisitos de detección <br> - Supervisión y análisis de seguridad <br> - Indicador de peligro (IOC) barridos <br> - Búsqueda de infracciones <br> - 24 horas del día 7: líder de respuesta a incidentes y de seguridad en llamada | - Requisitos de detección <br> - Supervisión de la implementación de la infraestructura <br> - Análisis del servicio y perspectiva <br> - Triaje de eventos y alertas <br> - 24 x 7 ingeniería de servicio en llamada  |
| Contención, eliminación, recuperación | - Líder de respuesta a incidentes <br> - Investigación forense <br> - Consultoría y experiencia en seguridad <br> - Guía de recuperación | - Propietario del incidente de seguridad <br> - Conocimientos y experiencia del servicio <br> - Ejecutar la contención, la eliminación y la recuperación |
| Actividad posterior al incidente | - Líder de análisis posterior al incidente <br> - Recopilación y archivado de datos <br> - Lecciones aprendidas y solicitudes de errores <br> - Informes de incidentes | - Análisis de incidentes del lado del servicio <br> - Priorizar actividades de seguimiento <br> - Implementación de inversiones en seguridad <br> - Preparación de seguridad del servicio |

## <a name="related-articles"></a>Artículos relacionados

- [Preparación de la administración de incidentes de seguridad de Microsoft 365](assurance-sim-preparation.md)
- [Análisis y detección de administración de incidentes de seguridad de Microsoft 365](assurance-sim-detection-analysis.md)
- [Contención, reactivación y recuperación de la administración de incidentes de seguridad de Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Actividad posterior a la incidencia de administración de incidentes de seguridad de Microsoft 365](assurance-sim-post-incident-activity.md)
