---
title: 'Administración de incidentes de seguridad de Microsoft: actividad posterior al incidente'
description: En este artículo, se proporciona información general sobre el proceso de actividad posterior a la incidencia de administración de incidentes de seguridad en los servicios en línea de Microsoft.
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
ms.openlocfilehash: 820c912dc55d5cc98cedc38676b5039591cf5baa
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947355"
---
# <a name="microsoft-security-incident-management-post-incident-activity"></a>Administración de incidentes de seguridad de Microsoft: actividad posterior al incidente

## <a name="postmortem"></a>Postmortem

Algunos incidentes de seguridad, especialmente los incidentes que afectan al cliente o resultan en una vulneración de datos, están sujetos a un postmortem completo de incidentes. El equipo de respuesta de seguridad lleva a cabo un postmortem detallado con todas las partes implicadas en la respuesta a incidentes de seguridad para:

- Documente la secuencia de eventos que provocaron el incidente.
- Cree un resumen técnico del incidente tal como lo admiten las pruebas que incluyen los actores implicados en la infracción (si se conoce). Este resumen incluirá cómo se ejecutó la respuesta y otras claves.
- Identifique lapsos técnicos, errores de procedimiento, errores manuales, defectos de proceso y problemas de comunicación, o cualquier vector de ataque desconocido anteriormente que se identificara durante la respuesta a incidentes de seguridad.

The postmortem will directly influence Microsoft online service improvement, operational processes, and documentation by setting new priorities in the Microsoft online services engineering development cycle.

## <a name="documentation"></a>Documentación

Todas las conclusiones técnicas clave del proceso postmortem se capturan en un informe y las inversiones de servicio o correcciones en forma de errores o solicitudes de cambio de desarrollo. Estos resultados se siguen con los equipos de ingeniería adecuados. Para los errores de proceso y problemas entre organizaciones, los problemas se documentan en la base de datos del equipo de respuesta de seguridad y se siguen con los grupos adecuados para solucionarlos.

## <a name="process-improvement"></a>Mejora de procesos

Responder a un incidente de seguridad en los servicios en línea de Microsoft implica la coordinación con varios grupos repartidos entre distintas organizaciones dentro de Microsoft, e incluso organizaciones externas potencialmente adecuadas, como las fuerzas del orden. Sabemos que es fundamental evaluar nuestras respuestas después de cada incidente de seguridad para la suficiencia y la integridad. Para las mejoras o cambios identificados, el equipo de respuesta de seguridad evalúa las sugerencias en consulta con los equipos y partes interesadas adecuados, y, si procede, las incorpora en los procedimientos operativos estándar. Todos los cambios, errores o mejoras de servicio necesarios identificados durante la respuesta a incidentes de seguridad o la actividad postmortem se registran y se realiza un seguimiento en una base de datos de ingeniería interna de Microsoft. Todos los posibles errores o características se asignan al propietario adecuado. El equipo de respuesta de seguridad de Microsoft revisa todas las entradas hasta que se resuelve el problema.

## <a name="related-articles"></a>Artículos relacionados

- [Administración de incidentes de seguridad de Microsoft](assurance-security-incident-management.md)
- [Administración de incidentes de seguridad de Microsoft: Preparación](assurance-sim-preparation.md)
- [Administración de incidentes de seguridad de Microsoft: detección y análisis](assurance-sim-detection-analysis.md)
- [Administración de incidentes de seguridad de Microsoft: contención, eliminación y recuperación](assurance-sim-containment-eradication-recovery.md)
- [Cómo registrar un vale de soporte de eventos de seguridad](/azure/security/fundamentals/event-support-ticket)
- [Azure y Dynamics 365 notificación de infracciones bajo el GDPR](/compliance/regulatory/gdpr-breach-azure-dynamics)
