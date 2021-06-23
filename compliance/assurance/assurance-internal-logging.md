---
title: Microsoft 365 registro interno para Microsoft 365 ingeniería
description: En este artículo, busque una explicación de cómo funciona el registro interno para Microsoft 365 de ingeniería.
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
hideEdit: true
ms.openlocfilehash: 71b08509ae920ad88ecfa1566b9a11d640b0534f
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088599"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a>Registro interno para la ingeniería de Microsoft 365

Además de los eventos y los datos de registro disponibles para los clientes, Microsoft mantiene un sistema interno de recopilación de datos de registro que está disponible para Microsoft 365 ingenieros. Muchos tipos diferentes de datos de registro se cargan desde servidores de Microsoft 365 a una solución de supervisión de seguridad propietaria para el análisis casi en tiempo real (NRT) y un servicio informático interno de big data (Cosmos) para el almacenamiento a largo plazo. Esta transferencia de datos se produce a través de una conexión TLS validada por FIPS 140-2 en puertos y protocolos aprobados mediante una herramienta de automatización propietaria denominada Office Data Loader (ODL). Las herramientas usadas en Microsoft 365 recopilar y procesar registros de auditoría no permiten cambios permanentes o irreversibles en el contenido del registro de auditoría original ni en el orden de tiempo.

Los equipos de servicio usan Cosmos como repositorio centralizado para realizar un análisis del uso de aplicaciones, medir el rendimiento operativo y del sistema y buscar anomalías y patrones que puedan indicar problemas o problemas de seguridad. Cada equipo de servicio carga una línea base que incluye:

- Registros de eventos
- Registros de AppLocker
- Datos de rendimiento
- System Center datos
- Registros de detalles de llamadas
- Datos de calidad de la experiencia
- Registros del servidor web iis
- SQL Server registros
- Datos de Syslog
- Registros de auditoría de seguridad

Antes de cargar, la aplicación ODL usa un servicio de depuración para quitar los campos que contienen datos de cliente, como información de inquilino e información identificable del usuario final, y reemplazar esos campos por un valor hash. Los registros de depuración se cargan en Cosmos y en la solución de supervisión de seguridad NRT que analiza los registros en busca de posibles eventos de seguridad e indicadores de rendimiento. El período de retención de datos del registro de auditoría Cosmos determina los equipos de servicio; La mayoría de los datos del registro de auditoría se conservan durante 90 días o más para admitir investigaciones de incidentes de seguridad y cumplir con los requisitos de retención normativos.

El acceso Microsoft 365 los datos almacenados en Cosmos está restringido al personal autorizado. Microsoft restringe la administración de registros de auditoría a un subconjunto limitado de miembros del equipo de seguridad responsables de la funcionalidad de auditoría. El equipo de seguridad no tiene acceso administrativo permanente a Cosmos y todos los cambios se registran y auditan.

Después del análisis NRT, cada equipo de servicio puede usar herramientas de análisis y paneles para la correlación de datos, consultas interactivas y análisis de datos. Estos informes se usan para supervisar y mejorar el rendimiento general del servicio.
