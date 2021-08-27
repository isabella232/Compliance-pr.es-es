---
title: 'Administración de incidentes de seguridad de Microsoft: contención, eliminación y recuperación'
description: En este artículo, se proporciona información general sobre el proceso de contención, eliminación y recuperación de la administración de incidentes de seguridad en los servicios en línea de Microsoft.
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
ms.openlocfilehash: 0c99c28ee6a291acbcfe913a87aa107d3be5c75a
ms.sourcegitcommit: 9766d656d0e270f478437bd39c0546ad2e4d846f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2021
ms.locfileid: "58676809"
---
# <a name="microsoft-security-incident-management-containment-eradication-and-recovery"></a>Administración de incidentes de seguridad de Microsoft: contención, eliminación y recuperación

En función del análisis realizado por el equipo de respuesta de seguridad, el equipo de servicio y otros, se desarrolla un plan de contención y recuperación adecuado para minimizar el efecto del incidente de seguridad. A continuación, los equipos de servicio adecuados aplican ese plan en producción con el soporte del equipo de respuesta de seguridad.

## <a name="containment"></a>Contención

Después de detectar un incidente de seguridad, es importante contener la intrusión antes de que el adversario pueda acceder a más recursos o causar más daños. El objetivo principal de nuestros procedimientos de respuesta a incidentes de seguridad es limitar el impacto en los clientes o sus datos, o en los sistemas, servicios y aplicaciones de Microsoft.

## <a name="eradication"></a>Erradicación

La confidencialidad es el proceso de eliminación de la causa principal del incidente de seguridad con un alto grado de confianza. El objetivo es doble:

- para desalojar completamente al adversario del entorno
- para mitigar la vulnerabilidad (si se conoce) que habilitaba o podía permitir al adversario volver a entrar en el entorno.

Según la naturaleza del incidente, el ámbito del incidente de seguridad, la profundidad de la penetración y las posibles repercusiones, el equipo de respuesta de seguridad recomendará que los equipos de servicio adopten técnicas de eliminación. Teniendo en cuenta el posible impacto empresarial que pueden causar estos pasos de eliminación, los equipos de servicio y el equipo de respuesta a la seguridad tomarán estas decisiones después de un análisis detallado y la aprobación del Administrador de incidentes ejecutivo (si es necesario).

## <a name="recovery"></a>Recuperación

A medida que el equipo de respuesta obtiene un nivel razonable de confianza de que el adversario ha sido desalojado del entorno y se han eliminado todas las rutas vulnerables conocidas, los equipos de servicio individuales iniciarán los pasos de restauración para llevar el servicio a una configuración conocida y buena. Estos pasos de restauración estarán en consulta con el equipo de respuesta de seguridad. Esta actividad incluye la identificación del último buen estado conocido del servicio, la restauración de copias de seguridad a este estado, la inspección de rutas de ataque vulnerables en el estado restaurado, etc. El equipo de respuesta de seguridad, en consulta con los equipos de servicio, determinará el mejor plan de recuperación posible para el entorno.

Un aspecto clave de la recuperación es tener una mayor vigilancia y controles para validar que el plan de recuperación se ha ejecutado correctamente y que no existen signos de infracción en el entorno.

## <a name="customer-notification-of-security-incident"></a>Notificación de cliente de incidentes de seguridad

Si Microsoft determina que se ha producido un incidente de seguridad, le notificaremos con retraso indebido y dentro de los requisitos contractuales y de cumplimiento que hemos aceptado. Después de identificar todos los inquilinos afectados, el equipo de comunicaciones correspondiente trabaja para identificar cualquier normativa relevante que se pueda aplicar a los inquilinos afectados. El equipo de comunicaciones usa el canal de comunicación adecuado definido en las normativas aplicables para notificar al contacto de inquilino correspondiente.

![Proceso de respuesta a incidentes.](../media/assurance-incident-response-process.png)

La notificación incluirá información detallada sobre el incidente, como una descripción del incidente, el efecto en los datos de los clientes, si los hay, las acciones realizadas por Microsoft o las acciones sugeridas para que los clientes tomen medidas para resolver el problema y evitar la periodicidad. La notificación se entregará a los administradores designados del inquilino de servicios en línea de Microsoft. Para asegurarse de que se reciben notificaciones, debe asegurarse de que los administradores proporcionan y mantienen información de contacto precisa en sus perfiles de inquilino. Además, en función de la naturaleza del incidente, Microsoft 365 los clientes también pueden recibir una notificación a través del Panel de mantenimiento Microsoft 365 [servicio.](http://status.yammer.com/)

## <a name="related-articles"></a>Artículos relacionados

- [Administración de incidentes de seguridad de Microsoft](assurance-security-incident-management.md)
- [Administración de incidentes de seguridad de Microsoft: Preparación](assurance-sim-preparation.md)
- [Administración de incidentes de seguridad de Microsoft: detección y análisis](assurance-sim-detection-analysis.md)
- [Administración de incidentes de seguridad de Microsoft: actividad posterior al incidente](assurance-sim-post-incident-activity.md)
- [Cómo registrar un vale de soporte de eventos de seguridad](/azure/security/fundamentals/event-support-ticket)
- [Azure y Dynamics 365 notificación de infracciones bajo el GDPR](/compliance/regulatory/gdpr-breach-azure-dynamics)
