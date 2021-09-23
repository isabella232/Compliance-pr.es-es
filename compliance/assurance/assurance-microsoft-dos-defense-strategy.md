---
title: Estrategia de defensa por denegación de servicio de Microsoft
description: En este artículo, encontrará una introducción a la estrategia de defensa de Microsoft para ataques de denegación de servicio (DoS).
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e1613765d3ffb7b43b80d07823fe8aef45719b70
ms.sourcegitcommit: cb0b058800d3a8f04921066b4c59fb427eb9c268
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/23/2021
ms.locfileid: "59486197"
---
# <a name="microsoft-denial-of-service-defense-strategy"></a>Estrategia de defensa por denegación de servicio de Microsoft

## <a name="denial-of-service-defense-strategy"></a>Estrategia de defensa de denegación de servicio

La estrategia de Microsoft para defenderse de los ataques de denegación de servicio distribuidos (DDoS) basados en la red es única debido a una gran superficie global, lo que permite a Microsoft usar estrategias y técnicas que no están disponibles para la mayoría de otras organizaciones. Además, Microsoft contribuye y se basa en conocimientos colectivos agregados por una extensa red de inteligencia contra amenazas, que incluye socios de Microsoft y la comunidad de seguridad de Internet más amplia. Esta inteligencia, junto con la información recopilada de los servicios en línea y la base de clientes global de Microsoft, mejora continuamente el sistema de defensa de DDoS de Microsoft que protege todos los activos de los servicios en línea de Microsoft.

La piedra angular de la estrategia DDoS de Microsoft es la presencia global. Microsoft se compromete con proveedores de Internet, proveedores de emparejamiento (públicos y privados) y empresas privadas de todo el mundo. Esta interacción proporciona a Microsoft una presencia significativa en Internet y permite a Microsoft absorber ataques en una gran superficie

A medida que la capacidad perimetral de Microsoft ha aumentado con el tiempo, la importancia de los ataques contra bordes individuales ha disminuido considerablemente. Debido a esta disminución, Microsoft ha separado los componentes de detección y mitigación de su sistema de prevención de DDoS. Microsoft implementa sistemas de detección de varios niveles en centros de datos regionales para detectar ataques más próximos a sus puntos de saturación y mantener la mitigación global en los nodos perimetrales. Esta estrategia garantiza que servicios Microsoft controlar varios ataques simultáneos.

Una de las defensas más eficaces y de bajo costo empleadas por Microsoft contra los ataques DDoS es reducir las superficies de ataque de servicio. El tráfico no deseado se descarta en el borde de red en lugar de analizar, procesar y limpiar los datos en línea.

En la interfaz con la red pública, Microsoft usa dispositivos de seguridad de uso especial para funciones de firewall, traducción de direcciones de red y filtrado de IP. Microsoft también usa el enrutamiento global de múltiples rutas de acceso (ECMP) de igual costo. El enrutamiento ECMP global es un marco de red para garantizar que hay varias rutas de acceso globales para llegar a un servicio. Con varias rutas de acceso a cada servicio, los ataques DDoS se limitan a la región desde la que se origina el ataque. Otras regiones no deberían estar afectadas por el ataque, ya que los usuarios finales usarían otras rutas de acceso para llegar al servicio en esas regiones. Microsoft también ha desarrollado sistemas internos de correlación y detección de DDoS que usan datos de flujo, métricas de rendimiento y otra información para detectar rápidamente ataques DDoS.

Para proteger aún más los servicios en la nube, Microsoft usa Azure DDoS Protection, un sistema de defensa de DDoS integrado en los procesos de supervisión continua y pruebas de penetración de Microsoft Azure. Azure DDoS Protection está diseñado no solo para resistir ataques externos, sino también ataques de otros inquilinos de Azure. Azure usa técnicas estándar de detección y mitigación, como cookies SYN, limitación de velocidad y límites de conexión para proteger contra ataques DDoS. Para admitir protecciones automatizadas, un equipo de respuesta a incidentes DDoS entre cargas de trabajo identifica los roles y responsabilidades entre equipos, los criterios de escalamiento y los protocolos para el tratamiento de incidentes en todos los equipos afectados.

La mayoría de los ataques DDoS lanzados contra objetivos se encuentran [](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) en las capas Red (L3) y Transporte (L4) del modelo de interconexión de sistemas abiertos (OSI). Los ataques dirigidos a las capas L3 y L4 están diseñados para inundar una interfaz de red o servicio con tráfico de ataques para saturar los recursos y denegar la capacidad de responder al tráfico legítimo. Para protegerse de los ataques L3 y L4, las soluciones DDoS de Microsoft usan datos de muestreo de tráfico de enrutadores de centros de datos para proteger la infraestructura y los destinos de los clientes. Un servicio de supervisión de red analiza los datos de muestreo de tráfico para detectar ataques. Cuando se detecta un ataque, los mecanismos de defensa automatizados se inician para mitigar el ataque y garantizar que el tráfico dirigido a un cliente no da como resultado daños colaterales o disminución de la calidad de servicio de la red para otros clientes.

Microsoft también adopta un enfoque ofensivo para la defensa de DDoS. Botnets are a common source of command and control for conducting DDoS attacks to amplify attacks and maintain anonymity. La Unidad de delitos digitales de Microsoft (DCU) se centra en identificar, investigar y interrumpir la infraestructura de comunicaciones y distribución de malware para reducir la escala y el impacto de las botnets.

## <a name="application-level-defenses"></a>Defensas de nivel de aplicación

Los equipos de ingeniería de Microsoft siguen los rigurosos estándares establecidos [por Microsoft Operational Security Assurance](https://www.microsoft.com/SDL/OperationalSecurityAssurance) para ayudar a proteger los datos de los clientes. Los servicios en la nube de Microsoft se han creado intencionadamente para admitir cargas elevadas, lo que ayuda a proteger contra ataques DDoS de nivel de aplicación. La arquitectura de escalado horizontal de Microsoft distribuye servicios en varios centros de datos globales con aislamiento regional y características de limitación específicas de la carga de trabajo para cargas de trabajo relevantes.

El país o la región de cada cliente, que el administrador del cliente identifica durante la configuración inicial de los servicios, determina la ubicación de almacenamiento principal para los datos de ese cliente. Los datos de los clientes se replican entre centros de datos redundantes de acuerdo con una estrategia principal/de copia de seguridad. Un centro de datos principal hospeda el software de la aplicación junto con todos los datos de cliente principales que se ejecutan en el software. Un centro de datos de copia de seguridad proporciona conmutación por error automática. Si el centro de datos principal deja de funcionar por cualquier motivo, las solicitudes se redirigen a la copia del software y los datos del cliente en el centro de datos de copia de seguridad. En cualquier momento, los datos de los clientes pueden procesarse en el centro de datos principal o en el centro de datos de copia de seguridad. La distribución de datos entre varios centros de datos reduce la superficie afectada en caso de que se ataque un centro de datos. Además, los servicios del centro de datos afectado se pueden redirigir rápidamente al centro de datos secundario para mantener la disponibilidad durante un ataque y redirigirlos al centro de datos principal una vez mitigado un ataque.

Como otra mitigación contra ataques DDoS, las cargas de trabajo individuales incluyen características integradas que administran el uso de recursos. Por ejemplo, los mecanismos de limitación de Exchange Online y SharePoint Online forman parte de un enfoque multicapa para defenderse de los ataques DDoS.

Azure SQL Database tiene una capa adicional de seguridad en forma de servicio de puerta de enlace denominado DoSGuard que realiza un seguimiento de los intentos de inicio de sesión fallidos en función de la dirección IP. Si se alcanza el umbral de intentos de inicio de sesión fallidos desde la misma IP, DoSGuard bloquea la dirección durante un período de tiempo predeterminado.

## <a name="resources"></a>Recursos

- [Introducción a Azure DDoS Protection Standard](/azure/ddos-protection/ddos-protection-overview)
- [Procedimientos recomendados fundamentales de Azure DDoS Protection Standard](/azure/ddos-protection/fundamental-best-practices)
- [Componentes de una estrategia de respuesta de DDoS](/azure/ddos-protection/ddos-response-strategy)
