---
title: 'Administración de incidentes de seguridad de Microsoft 365: contención, reactivación y recuperación'
description: En este artículo se proporciona información general sobre el proceso de contención, eliminación y recuperación de incidentes de seguridad en Microsoft 365.
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
ms.openlocfilehash: 702735ed2ba35a4f3b0a02123f0c58b5fb4d397e
ms.sourcegitcommit: d67e4d4fdc664f1da450c8ef2f6732e19bdd403a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "50037636"
---
# <a name="microsoft-365-security-incident-management-containment-eradication-and-recovery"></a>Administración de incidentes de seguridad de Microsoft 365: contención, reactivación y recuperación

Basándose en el análisis realizado por el equipo de respuesta de seguridad de Microsoft 365, el equipo de servicio y otros, se desarrolla un plan de contención y recuperación adecuado para minimizar el efecto del incidente de seguridad. A continuación, los equipos de servicio adecuados aplican ese plan en producción con el soporte del equipo de respuesta de seguridad de Microsoft 365.

## <a name="containment"></a>Contención

Después de detectar un incidente de seguridad, es importante contener la intrusión antes de que el adversario pueda acceder a más recursos o causar más daños. El objetivo principal de nuestros procedimientos de respuesta a incidentes de seguridad es limitar el impacto en los clientes o sus datos, o en los sistemas, servicios y aplicaciones de Microsoft.

## <a name="eradication"></a>Resalte

La erradicación es el proceso de eliminar la causa principal del incidente de seguridad con un alto grado de confianza. El objetivo es doble:

- para desalojar completamente al adversario del entorno
- para mitigar la vulnerabilidad (si se conoce) que habilitaba o podía permitir que el adversario vuelva a entrar en el entorno.

Según la naturaleza del incidente, el ámbito del incidente de seguridad, la profundidad de la penetración y las posibles repercusiones, el equipo de respuesta de seguridad de Microsoft 365 recomendará que los equipos de servicio adopten técnicas de eliminación. Teniendo en cuenta el posible impacto en el negocio que puede deberse a estos pasos de la erradicación, los equipos de servicio y el equipo de respuesta de seguridad de Microsoft 365 tomarán estas decisiones después de un análisis detallado y la aprobación del Administrador ejecutivo de incidentes (si es necesario).

## <a name="recovery"></a>Recuperación

A medida que el equipo de respuesta obtiene un nivel razonable de confianza de que el adversario ha sido desalojado del entorno y se han eliminado todas las rutas vulnerables conocidas, los equipos de servicio individuales iniciarán los pasos de restauración para llevar el servicio a una configuración conocida y correcta. Estos pasos de restauración estarán en consulta con el equipo de respuesta de seguridad de Microsoft 365. Esta actividad incluye la identificación del último buen estado conocido del servicio, la restauración desde copias de seguridad a este estado, la inspección de rutas de ataque vulnerables en el estado restaurado, etc. El equipo de respuesta de seguridad de Microsoft 365, en consulta con los equipos de servicio, determinará el mejor plan de recuperación posible para el entorno.

Un aspecto clave de la recuperación es tener controles y alertas mejorados para validar que el plan de recuperación se ha ejecutado correctamente y que no existen signos de infracción en el entorno.

## <a name="customer-notification-of-security-incident"></a>Notificación al cliente del incidente de seguridad

Si Microsoft determina que se ha producido un incidente de seguridad, le notificaremos con un retraso no debido y dentro de los requisitos contractuales y de cumplimiento que hemos aceptado. Después de identificar todos los inquilinos afectados, el equipo de comunicaciones de Microsoft 365 Customer Experience (CxP) trabaja para identificar cualquier normativa relevante que pueda aplicarse a los inquilinos afectados. El equipo de comunicaciones de Microsoft 365 CxP usa el canal de comunicación adecuado definido en las normativas aplicables para notificar al contacto de inquilino adecuado.

La notificación incluirá información detallada sobre el incidente, como una descripción del incidente, el efecto en los datos de los clientes, si los hay, las acciones realizadas por Microsoft o las acciones sugeridas que deben realizar los clientes para resolver el problema y evitar la periodicidad. La notificación se entregará a los administradores designados del inquilino de Microsoft 365. Para asegurarse de que se reciben las notificaciones, debe asegurarse de que los administradores proporcionen y mantengan información de contacto precisa en sus perfiles de inquilino. Además, según la naturaleza del incidente, también se puede notificar a los clientes[](http://status.yammer.com/) a través del Panel de estado del servicio de Microsoft 365.

## <a name="related-articles"></a>Artículos relacionados

- [Administración de incidentes de seguridad de Microsoft 365](assurance-security-incident-management.md)
- [Preparación de la administración de incidentes de seguridad de Microsoft 365](assurance-sim-preparation.md)
- [Análisis y detección de administración de incidentes de seguridad de Microsoft 365](assurance-sim-detection-analysis.md)
- [Actividad posterior a la incidencia de administración de incidentes de seguridad de Microsoft 365](assurance-sim-post-incident-activity.md)
