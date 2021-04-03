---
title: 'Administración de incidentes de seguridad de Microsoft 365: actividad posterior al incidente'
description: En este artículo, se proporciona información general sobre el proceso de actividad posterior a la incidencia de administración de incidentes de seguridad en Microsoft 365.
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
ms.openlocfilehash: 4ebd31c16f8abb3eddd6ed924a045d88597aba40
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496711"
---
# <a name="microsoft-365-security-incident-management-post-incident-activity"></a>Administración de incidentes de seguridad de Microsoft 365: actividad posterior al incidente

## <a name="postmortem"></a>Postmortem

Algunos incidentes de seguridad, especialmente los incidentes que afectan al cliente o resultan en una vulneración de datos, están sujetos a un postmortem completo de incidentes. El equipo de respuesta de seguridad de Microsoft 365 lleva a cabo un postmortem detallado con todas las partes implicadas en la respuesta a incidentes de seguridad a:

- Documentar la secuencia de eventos que provocaron el incidente
- Cree un resumen técnico del incidente tal como lo admiten las pruebas que incluyen los actores implicados en la infracción (si se conoce). Este resumen incluirá cómo se ejecutó la respuesta y otras claves.
- Identifique lapsos técnicos, errores de procedimiento, errores manuales, defectos de proceso y problemas de comunicación, o cualquier vector de ataque desconocido anteriormente que se identificara durante la respuesta a incidentes de seguridad.

The postmortem will directly influence Microsoft 365 service improvement, operational processes, and documentation by setting new priorities in the Microsoft 365 engineering development cycle.

## <a name="documentation"></a>Documentación

Todas las conclusiones técnicas clave del proceso postmortem se capturan en un informe y las inversiones de servicio o correcciones en forma de errores o solicitudes de cambio de desarrollo. Estos resultados se siguen con los equipos de ingeniería adecuados. Para los errores de proceso y problemas entre organizaciones, los problemas se documentan en la base de datos del equipo de respuesta de seguridad de Microsoft 365 y se siguen con los grupos adecuados para solucionarlos.

## <a name="process-improvement"></a>Mejora de procesos

Responder a un incidente de seguridad en Microsoft 365 implica la coordinación con varios grupos repartidos entre diferentes organizaciones dentro de Microsoft, e incluso organizaciones externas potencialmente apropiadas, como las fuerzas del orden. Sabemos que es fundamental evaluar nuestras respuestas después de cada incidente de seguridad para la suficiencia y la integridad. Para las mejoras o cambios identificados, el equipo de respuesta de seguridad de Microsoft 365 evalúa las sugerencias en consulta con los equipos y partes interesadas adecuados y, en su caso, las incorpora en los procedimientos operativos estándar. Todos los cambios, errores o mejoras de servicio necesarios identificados durante la respuesta a incidentes de seguridad o la actividad postmortem se registran y se realiza un seguimiento en una base de datos de ingeniería interna de Microsoft 365. Todos los posibles errores o características se asignan al propietario adecuado. El equipo de respuesta de seguridad de Microsoft 365 revisa todas las entradas hasta que se resuelva el problema.

## <a name="related-articles"></a>Artículos relacionados

- [Administración de incidentes de seguridad de Microsoft 365](assurance-security-incident-management.md)
- [Preparación de la administración de incidentes de seguridad de Microsoft 365](assurance-sim-preparation.md)
- [Análisis y detección de incidentes de seguridad de Microsoft 365](assurance-sim-detection-analysis.md)
- [Contención, eliminación y recuperación de la administración de incidentes de seguridad de Microsoft 365](assurance-sim-containment-eradication-recovery.md)
