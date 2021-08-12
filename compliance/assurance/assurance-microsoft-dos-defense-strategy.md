---
title: Estrategia de defensa por denegación de servicio de Microsoft 365
description: En este artículo, encontrará una introducción a la estrategia de defensa de Microsoft para ataques de denegación de servicio (DoS).
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 720925408016af86d0bb16590f341970c0c5f0d0958c91b12e6b810c9b8a939a
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "54290609"
---
# <a name="microsoft-365-denial-of-service-defense-strategy"></a>Estrategia de defensa por denegación de servicio de Microsoft 365

## <a name="core-principles-of-defense-against-denial-of-service-attacks"></a>Principios básicos de defensa contra ataques por denegación de servicio

Existen tres principios básicos al defenderse de los ataques de denegación de servicio (DoS) basados en la red: la absorción, la detección y la mitigación. La absorción se produce antes de la detección y la detección debe producirse antes de que pueda comenzar la mitigación. Si incluso un ataque DoS pequeño no se puede absorber, los servicios no sobrevivirán lo suficiente como para que se detecte el ataque. Al detectar un ataque antes de que el sistema se agote, los defensores pueden implementar un plan de respuesta.

La siguiente fórmula ayuda a aproximar el tiempo de impacto de un ataque DoS:

  **Capacidad máxima (en bytes/s) / Tasa de crecimiento (en bytes/seg. ) = Tiempo de impacto (en segundos)**

Si el tiempo de detección es mayor que el tiempo de impacto, es probable que el ataque DoS se realice correctamente. Si el tiempo de detección es menor que el tiempo de impacto, los servicios afectados deben permanecer en línea y accesibles si las estrategias de mitigación son correctas.

Por lo tanto, hay dos estrategias principales para defenderse de los ataques DoS:

- Aumentar la capacidad para elevar el límite máximo de capacidad (que a su vez proporciona más tiempo para detectar un ataque); o
- Reduzca el tiempo para detectar un ataque.

Una ventaja de seguridad del uso de los servicios en la nube de Microsoft es la forma en que los servicios Microsoft de gran escala proporcionan una protección de red sólida a los clientes de la nube de forma rentable. Incluso a gran escala, debe haber un equilibrio entre la absorción, la detección y la mitigación. Para encontrar ese equilibrio, Microsoft estudia las tasas de crecimiento de ataque para calcular cuánto servicios Microsoft debe absorber.

## <a name="denial-of-service-defense-strategy"></a>Estrategia de defensa de denegación de servicio

La estrategia de Microsoft para defenderse de los ataques DoS basados en red es única debido a nuestra escala y a nuestra superficie global. Esta escala permite a Microsoft usar estrategias y técnicas que no están disponibles para la mayoría de otras organizaciones. La base de nuestra estrategia de DoS es nuestra presencia global. Microsoft se compromete con proveedores de Internet, proveedores de emparejamiento (públicos y privados) y empresas privadas de todo el mundo. Esta interacción proporciona a Microsoft una presencia significativa en Internet y permite a Microsoft absorber los ataques en una gran superficie.

A medida que la capacidad perimetral de Microsoft ha aumentado con el tiempo, la importancia de los ataques contra bordes individuales ha disminuido considerablemente. Debido a esta disminución, Microsoft ha separado los componentes de detección y mitigación de su sistema de prevención doS. Microsoft implementa sistemas de detección de varios niveles en centros de datos regionales para detectar ataques más próximos a sus puntos de saturación y mantener la mitigación global en los nodos perimetrales. Esta estrategia garantiza que servicios Microsoft controlar varios ataques simultáneos.

Una de las defensas más eficaces y de bajo costo empleadas por Microsoft contra los ataques DoS es reducir las superficies de ataque de servicio. El tráfico no deseado se descarta en el borde de red en lugar de analizar, procesar y limpiar los datos en línea.

En la interfaz con la red pública, Microsoft usa dispositivos de seguridad de uso especial para funciones de firewall, traducción de direcciones de red y filtrado de IP. Microsoft también usa el enrutamiento global de múltiples rutas de acceso (ECMP) de igual costo. El enrutamiento ECMP global es un marco de red para garantizar que hay varias rutas de acceso globales para llegar a un servicio. Con varias rutas de acceso a cada servicio, los ataques DoS se limitan a la región desde la que se origina el ataque. Otras regiones no deberían estar afectadas por el ataque, ya que los usuarios finales usarían otras rutas de acceso para llegar al servicio en esas regiones. Microsoft también ha desarrollado sistemas internos de correlación y detección doS que usan datos de flujo, métricas de rendimiento y otra información para detectar rápidamente ataques DoS.

Para proteger aún más nuestros servicios en la nube, Microsoft 365 usa un sistema de defensa de denegación de servicio (DDoS) distribuido integrado en los procesos de supervisión continua y pruebas de penetración de Microsoft Azure. El sistema de defensa de Azure DDoS está diseñado no solo para resistir ataques externos, sino también ataques de otros inquilinos de Azure. Azure usa técnicas estándar de detección y mitigación, como cookies SYN, limitación de velocidad y límites de conexión para proteger contra ataques DDoS. Para admitir nuestras protecciones automatizadas, un equipo de respuesta a incidentes DoS entre cargas de trabajo identifica los roles y responsabilidades entre equipos, los criterios de escalamiento y los protocolos para el tratamiento de incidentes en todos los equipos afectados.

La mayoría de los ataques DoS que se inician contra objetivos se encuentran en las capas Red (L3) y Transporte (L4) [del](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) modelo de interconexión de sistemas abiertos (OSI). Los ataques dirigidos a las capas L3 y L4 están diseñados para inundar una interfaz de red o servicio con tráfico de ataques para saturar los recursos y denegar la capacidad de responder al tráfico legítimo. Para protegerse de los ataques L3 y L4, las soluciones DoS de Microsoft usan datos de muestreo de tráfico de enrutadores de centros de datos para proteger la infraestructura y los destinos de los clientes. Un servicio de supervisión de red analiza los datos de muestreo de tráfico para detectar ataques. Cuando se detecta un ataque, los mecanismos de defensa automatizados se inician para mitigar el ataque y garantizar que el tráfico dirigido a un cliente no da como resultado daños colaterales o disminución de la calidad de servicio de la red para otros clientes.

## <a name="application-level-defenses"></a>Defensas de nivel de aplicación

Los equipos de ingeniería de Microsoft siguen los rigurosos estándares establecidos [por Microsoft Operational Security Assurance](https://www.microsoft.com/SDL/OperationalSecurityAssurance) para ayudar a proteger los datos de los clientes. Los servicios en la nube de Microsoft se han creado intencionadamente para admitir cargas elevadas, lo que ayuda a proteger contra ataques DoS a nivel de aplicación. la arquitectura de escalado horizontal de Microsoft 365 distribuye servicios en varios centros de datos globales con características de aislamiento regional y limitación específica de cargas de trabajo para cargas de trabajo relevantes.

El país o región de cada cliente, que el administrador del cliente identifica durante la configuración inicial de los servicios, determina la ubicación de almacenamiento principal para los datos de ese cliente. Los datos de los clientes se replican entre centros de datos redundantes de acuerdo con una estrategia principal/de copia de seguridad. Un centro de datos principal hospeda el software de la aplicación junto con todos los datos de cliente principales que se ejecutan en el software. Un centro de datos de copia de seguridad proporciona conmutación por error automática. Si el centro de datos principal deja de funcionar por cualquier motivo, las solicitudes se redirigen a la copia del software y los datos del cliente en el centro de datos de copia de seguridad. En cualquier momento, los datos de los clientes pueden procesarse en el centro de datos principal o en el centro de datos de copia de seguridad. La distribución de datos entre varios centros de datos reduce la superficie afectada en caso de que se ataque un centro de datos. Además, los servicios del centro de datos afectado se pueden redirigir rápidamente al centro de datos secundario para mantener la disponibilidad durante un ataque y redirigirlos al centro de datos principal una vez mitigado un ataque.

Como otra mitigación contra ataques DoS, las cargas de trabajo individuales incluyen características integradas que administran el uso de recursos. Por ejemplo, los mecanismos de limitación de Exchange Online y SharePoint Online forman parte de un enfoque multicapa para defenderse de los ataques DoS.
