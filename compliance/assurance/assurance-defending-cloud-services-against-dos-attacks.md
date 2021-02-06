---
title: Defensa de los servicios en la nube de Microsoft 365 contra ataques por denegación de servicio
description: En este artículo, obtenga información sobre cómo Microsoft defenderá sus servicios en la nube frente a ataques por denegación de servicio (DoS).
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: e632c1524d5cc8c21aec9dab3d95d285a3b8801e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120579"
---
# <a name="defending-microsoft-365-cloud-services-against-denial-of-service-attacks"></a>Defensa de los servicios en la nube de Microsoft 365 contra ataques por denegación de servicio

Los centros de datos de Microsoft están protegidos por una seguridad de defensa en profundidad que incluye perímetro, cámaras de vídeo, personal de seguridad y entradas seguras que usan biometría, tarjeta inteligente y autenticación multifactor. La seguridad de defensa en profundidad continúa en cada área de la instalación y en cada unidad de servidor físico. Microsoft [Cloud Infrastructure and Operations Group](https://www.microsoft.com/cloud-platform/global-datacenters) proporciona la infraestructura principal y las tecnologías fundamentales para nuestros servicios en la nube. Nuestros centros de datos cumplen con los estándares de seguridad física y confiabilidad del sector y son administrados, supervisados y administrados por el personal de operaciones de Microsoft.

Para proteger aún más nuestros servicios en la nube, Microsoft proporciona un sistema de defensa DDoS que forma parte de los procesos de supervisión continua y prueba de penetración de Microsoft Azure. El sistema de defensa de DDoS de Azure está diseñado no solo para soportar ataques desde el exterior, sino también desde otros inquilinos de Azure. Azure usa técnicas estándar de detección y mitigación como cookies SYN, limitación de velocidad y límites de conexión para protegerse contra ataques DDoS.

Los servicios en la nube de Microsoft están sujetos a la amenaza de ataque de varios orígenes. Para mitigar y proteger contra las diversas amenazas DoS, se ha desarrollado e implementado un sistema de mitigación y detección de amenazas basado en Azure altamente escalable y dinámico con el objetivo principal de proteger la infraestructura subyacente de los ataques DoS y ayudar a evitar interrupciones del servicio para los clientes de servicios en la nube. El sistema de mitigación de Azure DoS protege el tráfico entrante, saliente y de región a región.

La mayoría de los ataques DoS se inician contra destinos [](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) en las capas red (L3) y transporte (L4) del modelo de interconexión de sistemas abiertos (OSI). Los ataques dirigidos a las capas L3 y L4 están diseñados para inundar una interfaz de red o un servicio con tráfico de ataques para saturar los recursos y denegar la capacidad de responder al tráfico legítimo. En concreto, los ataques L3 y L4 intentan saturar la capacidad de los vínculos de red, dispositivos o servicios, o saturan las CPU de los servidores o máquinas virtuales que admiten una aplicación.

Para protegerse contra los ataques L3 y L4, Microsoft ha diseñado, desarrollado e implementado una solución destinada específicamente a proteger la infraestructura y los objetivos de los clientes que se ven afectados por la protección de estas capas. La protección de la infraestructura garantiza que el tráfico de ataques destinado a un cliente no da como resultado daños colaterales ni una disminución de la calidad de servicio de la red para otros clientes. La solución usa datos de muestreo de tráfico de enrutadores de centros de datos. Un servicio de supervisión de red analiza estos datos para detectar ataques. Cuando se detecta un ataque, se inician mecanismos de defensa automatizados.

## <a name="application-level-defenses"></a>Application-Level defensas
Los equipos de ingeniería de Microsoft siguen los rigurosos estándares establecidos por [Microsoft Operational Security Assurance](https://www.microsoft.com/SDL/OperationalSecurityAssurance) para ayudar a proteger los datos de los clientes. Los servicios en la nube de Microsoft se han creado intencionadamente para admitir una carga muy alta, así como para proteger y mitigar los ataques DoS en el nivel de aplicación. Hemos implementado una arquitectura de escalado horizontal donde los servicios se distribuyen en varios centros de datos globales con características de aislamiento regional y limitación en algunas de las cargas de trabajo.

El país o la región de cada cliente, que el administrador del cliente identifica durante la configuración inicial de los servicios, determina la ubicación de almacenamiento principal de los datos de ese cliente. Los datos de los clientes se replican entre centros de datos redundantes según una estrategia principal o de copia de seguridad. Un centro de datos principal hospeda el software de la aplicación junto con todos los datos de cliente principales que se ejecutan en el software. Un centro de datos de copia de seguridad proporciona conmutación por error automática. Si el centro de datos principal deja de funcionar por cualquier motivo, las solicitudes se redirigen a la copia del software y los datos del cliente en el centro de datos de copia de seguridad. En cualquier momento dado, los datos de los clientes se pueden procesar en el centro de datos principal o en el centro de datos de copia de seguridad. La distribución de datos entre varios centros de datos reduce el área de superficie afectada en caso de ataque a un centro de datos. Además, los servicios del centro de datos afectado se pueden redirigir rápidamente al centro de datos secundario como uno de los mecanismos de recuperación y viceversa (se redirigen al centro de datos principal una vez restaurado el servicio).

Las cargas de trabajo individuales incluyen características integradas que administran el uso de recursos. Por ejemplo, los mecanismos de limitación de Exchange Online y SharePoint Online forman parte de un enfoque de varias capas para defenderse contra ataques DoS. La limitación para los usuarios de Exchange Online se basa en el nivel de recursos que consume el usuario final, independientemente de si los recursos están en Active Directory, el almacén de información de Exchange Online o en otro lugar. Se asigna un presupuesto a cada cliente para limitar los recursos que consume un usuario. La limitación de Exchange Online para la actividad del usuario y los componentes del sistema se basa en la administración [de cargas de trabajo.](https://technet.microsoft.com/library/jj150503(v=exchg.150).aspx) Una carga de trabajo de Exchange Online es una característica, protocolo o servicio de Exchange Online que se ha definido explícitamente para los fines de la administración de recursos del sistema de Exchange Online. Cada carga de trabajo de Exchange Online requiere recursos del sistema como CPU, operaciones de base de datos de buzones de correo o solicitudes de Active Directory para realizar solicitudes de usuario o trabajo en segundo plano. Algunos ejemplos de cargas de trabajo de Exchange Online son Outlook en la Web, Exchange ActiveSync, migración de buzones y asistentes de buzones. Los administradores de inquilinos pueden administrar la configuración de limitación de la administración de cargas de trabajo de Exchange para los usuarios con el Shell de administración de Exchange. Existen varias formas de limitación que se han implementado en Exchange Online, como PowerShell, Servicios Web Exchange y POP e IMAP, Exchange ActiveSync, conexiones de dispositivos móviles, destinatarios y mucho más. Aunque los administradores de implementaciones locales de Exchange pueden configurar directivas de limitación, los administradores no pueden configurar directivas de limitación para Exchange Online.

El desencadenador más común para la limitación en SharePoint Online es el código del modelo de objetos del lado cliente (CSOM) que realiza demasiadas acciones con una frecuencia demasiado alta. Con CSOM, muchas acciones se pueden realizar con una sola solicitud, lo que puede superar los límites de uso y provocar una limitación por usuario.

Independientemente de la actividad que pueda dar lugar a la limitación, cuando un usuario supera los límites de uso, SharePoint Online limita cualquier otra solicitud de esa cuenta de usuario, normalmente durante un breve período. Mientras haya una limitación de usuarios en vigor, todas las acciones de ese usuario se limitarán hasta que expire la limitación, según los criterios siguientes:
- Para las solicitudes realizadas por el usuario directamente en un explorador, SharePoint Online redirige a una página de información de limitación y se producirá un error en las solicitudes.
- Para todas las demás solicitudes, incluidas las llamadas de CSOM, SharePoint Online devuelve el código de estado HTTP 429 ("demasiadas solicitudes") y se producirá un error en las solicitudes.

Si el proceso ofensivo sigue superando los límites de uso, SharePoint Online puede bloquear completamente el proceso y devolver el código de estado HTTP 503 ("servicio no disponible").

## <a name="vulnerability-and-penetration-testing"></a>Pruebas de vulnerabilidad y penetración
Microsoft usa [](https://www.microsoft.com/trustcenter/security/threatmanagement) muchas tecnologías [](https://blogs.technet.microsoft.com/hybridcloud/2015/05/05/protecting-your-datacenter-and-cloud-from-emerging-threats/) y prácticas de seguridad para proteger su infraestructura en la nube y las redes locales frente a amenazas modernas y sofisticadas, incluido el uso de componentes y servicios antimalware para servicios en la nube, máquinas virtuales (VM) y otros sistemas. Análisis de amenazas avanzado, que supervisa los patrones de uso normal para redes, sistemas y usuarios, y emplea el aprendizaje automático para marcar cualquier comportamiento fuera de las pruebas de penetración normales y normales.

Además de realizar nuestras propias pruebas de penetración y ofrecer a nuestros clientes un programa de pruebas de penetración unificada de [Microsoft Cloud,](https://technet.microsoft.com/mt784683)también nos comprometemos con los profesionales de seguridad de terceros que realizan evaluaciones periódicas de vulnerabilidades y pruebas de penetración en nuestros servicios en la nube. Los informes de estas evaluaciones de vulnerabilidad de terceros están disponibles para su descarga desde los portales de [Confianza](https://aka.ms/STP) del servicio y [Garantía de](https://aka.ms/ServiceAssurance) servicios.
