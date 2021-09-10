---
title: Resistencia del servicio integrado en Microsoft 365
description: Descripción de Microsoft 365 resistencia del servicio
author: robmazz
ms.author: robmazz
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: o365-solutions
ms.localizationpriority: medium
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 592cfcdf3da33e6c26e90d5a83fb6bcd3b4241e0
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947315"
---
# <a name="built-in-service-resiliency-in-microsoft-365"></a>Resistencia del servicio integrado en Microsoft 365

Como proveedor de colaboración en la nube, Microsoft reconoce la necesidad de ganar su confianza continuamente proporcionando soluciones que funcionen sistemáticamente y que gusten a los usuarios. Cuando un servicio determinado no está disponible, se denomina tiempo de inactividad. La definición de tiempo de inactividad varía en función de cada servicio de Microsoft 365, pero normalmente se refiere a un período de tiempo en el que los usuarios no pueden usar la funcionalidad esencial del servicio. Por ejemplo, la definición de tiempo de inactividad para SharePoint Online según el contrato de nivel de servicio de Microsoft 365 es esta:

**"Inactividad de SharePoint Online**: cualquier período de tiempo en el que los usuarios no puedan leer ni escribir ninguna parte de una colección de sitios de SharePoint Online para la que tengan los permisos adecuados".

Puede encontrar las definiciones de tiempo de inactividad para cada servicio en los [contratos de nivel de servicio](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=37).

Para minimizar el tiempo de inactividad, tanto planeado como imprevisto, los servicios de Microsoft 365 están diseñados y se pueden gestionar para que estén altamente disponibles y sean resilientes frente a errores centrándose en cuatro áreas:

## <a name="activeactive-design"></a>Diseño activo/activo

In Microsoft 365, we are driving towards having all services architected and operated in an active/active design that increases resiliency. Este diseño significa que siempre hay varias instancias de un servicio en ejecución que pueden responder a las solicitudes de los usuarios y que se hospedan en centros de datos dispersos geográficamente. Todo el tráfico de usuarios entra a través del servicio Front Door de Microsoft y se redirige automáticamente a una instancia localizada de forma óptima del servicio y evitando cualquier error de servicio para prevenir o reducir el impacto en nuestros clientes.

## <a name="reduce-incident-scope"></a>Reducir el ámbito de la incidencia

El ámbito de una incidencia de servicio se mide en función de su gravedad, el tiempo que dura y cuántos clientes se ven afectados. Nos esforzamos por limitar el alcance de cada incidencia:

- proporcionando varias instancias de cada servicio compartimentadas entre sí
- implementando actualizaciones de una forma controlada y graduada mediante anillos de validación, de modo que los problemas que puedan surgir de la actualización se puedan detectar y mitigar anticipadamente en el proceso de implementación. Este diseño permite la regresión de la actualización si es necesario y se produce primero en un grupo pequeño dentro de Microsoft (anillo interno) antes de que se implemente para grupos más grandes como los 140.000 empleados de Microsoft (anillo 2), luego para los anillos de adopción temprana (anillo 3) y, en última instancia, para todos los clientes globalmente (anillo 4).
- promoviendo las mejoras en la supervisión gracias a la automatización. Microsoft 365 es un servicio grande y el tiempo de actividad de destino de SLA es alto. Al principio de una incidencia del servicio, si los seres humanos tuvieran que intervenir en la detección y respuesta, no podríamos responder lo suficientemente rápido para cumplir los SLA. La automatización es la clave para que la detección y respuesta de una incidencia de servicio sea rápida y eficaz. Cuanto más pronto tengamos conocimiento de algo, más rápido se podrá solucionar.

Junto con las capacidades activas y activas integradas en Microsoft 365 de servicio, estos esfuerzos mitigan la gravedad, la duración y el número de clientes afectados durante un incidente de servicio.  

## <a name="fault-isolation"></a>Aislamiento de fallos

Al igual que los servicios se diseñan y funcionan de un modo activo/activo y se compartimentan entre sí para evitar que uno de los errores afecte a otro, la base del código del servicio se desarrolla mediante principios de compartimentación similares llamados aislamiento de fallos. Las medidas de aislamiento de fallos son protecciones incrementales que se llevan a cabo en la propia base del código. Estas medidas ayudan a evitar que un problema en un área afecte a otras áreas de operación.
Las medidas de aislamiento de errores se aplican en varias etapas del desarrollo y la entrega de un servicio, incluido el desarrollo de código, la implementación del servicio, el equilibrio de carga y la replicación de bases de datos.

El Ciclo de vida de desarrollo de seguridad de Microsoft (SDL) promueve la resiliencia y consta de un conjunto de prácticas que admiten requisitos de seguridad y cumplimiento. El SDL guía a nuestros desarrolladores para crear servicios resilientes, seguros y compatibles. Entre los elementos clave del SDL se incluyen las revisiones de código, el modelado de amenazas, las pruebas de penetración y los procesos normalizados de respuesta ante incidencias en la nube de Microsoft.

Microsoft 365 servicios están altamente interconectados, pero los sistemas y la tecnología subyacentes están diseñados de forma que se limita el impacto de un incidente de servicio a otros servicios. Por ejemplo, un problema que afecte a Exchange Online no afectará a la funcionalidad principal de Teams o un problema con la funcionalidad de búsqueda en SharePoint Online no afectará a la capacidad de los usuarios para cargar o descargar archivos.

## <a name="continuous-service-improvement"></a>Mejora continua del servicio

Cuando se experimenta una incidencia, nos lo tomamos en serio. Después de todo, la arquitectura redundante de la nube y los estrictos procesos internos tienen como objetivo mantener la accesibilidad a nuestros servicios. Durante un incidente, nuestra supervisión detecta rápidamente los servicios afectados y, si su inquilino se ve afectado, se le notificará inmediatamente a través de varios canales. Simultáneamente, los ingenieros siguen procesos bien definidos para clasificar el problema y llevar a cabo los pasos necesarios para restaurar el funcionamiento normal lo más rápido posible. Una vez que el servicio funciona con normalidad de nuevo, realizamos un examen posterior de incidencias como parte del ciclo de mejora continua del servicio. Durante la revisión posterior de incidencias, identificamos las causas principales de la incidencia y lo que fue necesario para corregir los problemas. Luego, teniendo en cuenta lo aprendido de la situación, lo aplicamos al diseño y a las operaciones de la totalidad de nuestra serie de ofertas. Con este conocimiento, podemos evitar que la misma causa raíz repercuta en otros servicios y clientes adicionales.
