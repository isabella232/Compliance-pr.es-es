---
title: Registro interno de Microsoft 365 para ingeniería de Microsoft 365
description: En este artículo, busque una explicación de cómo funciona el registro interno para microsoft 365 Engineering teams.
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
ms.openlocfilehash: 110a61c27a00380eede4d4f2303acfb025a27a1f
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497074"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a>Registro interno para la ingeniería de Microsoft 365

Además de los eventos y los datos de registro disponibles para los clientes, también hay un sistema interno de recopilación de datos de registro que está disponible para los ingenieros de Microsoft 365 en Microsoft. Muchos tipos diferentes de datos de registro se cargan desde servidores de Microsoft 365 a un servicio informático interno de big data denominado Cosmos. Cada equipo de servicio carga los registros de auditoría de sus respectivos servidores en la base de datos de Cosmos para su agregación y análisis. Esta transferencia de datos se produce a través de una conexión TLS validada por FIPS 140-2 en puertos y protocolos aprobados específicamente mediante una herramienta de automatización propietaria denominada Office Data Loader (ODL). Las herramientas usadas en Microsoft 365 para recopilar y procesar registros de auditoría no permiten cambios permanentes o irreversibles en el contenido del registro de auditoría original ni en el orden de tiempo.

Los equipos de servicio usan Cosmos como repositorio centralizado para realizar un análisis del uso de aplicaciones, medir el rendimiento operativo y del sistema y buscar anomalías y patrones que puedan indicar problemas o problemas de seguridad. Cada equipo de servicio carga una línea base de registros en Cosmos, en función de lo que estén buscando analizar, que a menudo incluyen:

- Registros de eventos
- Registros de AppLocker
- Datos de rendimiento
- Datos de System Center
- Registros de detalles de llamadas
- Datos de calidad de la experiencia
- Registros del servidor web iis
- SQL Server registros
- Datos de Syslog
- Registros de auditoría de seguridad

Antes de cargar datos en Cosmos, la aplicación ODL usa un servicio de depuración para ofuscar los campos que contienen datos de clientes, como información de inquilino e información identificable del usuario final, y reemplazar esos campos por un valor hash. Los registros anonimizados y hash se reescriben y, a continuación, se cargan en Cosmos. Los equipos de servicio ejecutan consultas con ámbito en sus datos en Cosmos para la correlación, alertas e informes. El período de retención de datos del registro de auditoría en Cosmos lo determinan los equipos de servicio; La mayoría de los datos del registro de auditoría se conservan durante 90 días o más para admitir investigaciones de incidentes de seguridad y cumplir con los requisitos de retención normativos.

El acceso a los datos de Microsoft 365 almacenados en Cosmos está restringido al personal autorizado. Microsoft restringe la administración de la funcionalidad de auditoría al subconjunto limitado de miembros del equipo de servicio que son responsables de la funcionalidad de auditoría. Estos miembros del equipo no tienen la capacidad de modificar o eliminar datos de Cosmos y todos los cambios en los mecanismos de registro de Cosmos se registran y auditan.

Cada equipo de servicio tiene acceso a sus datos de registro para su análisis mediante la autorización de determinadas aplicaciones para realizar análisis específicos. Por ejemplo, el equipo de seguridad de Microsoft 365 usa datos de Cosmos a través de un analizador de registro de eventos propietario para correlacionar, alertar y generar informes prácticos sobre posibles actividades sospechosas en el entorno de producción de Microsoft 365. Los informes de estos datos se usan para corregir vulnerabilidades y mejorar el rendimiento general del servicio. Si una alerta o informe específico requiere una investigación adicional, el personal de servicio puede solicitar que los datos se vuelvan a importar al servicio de Microsoft 365. Dado que el registro específico que se importa de Cosmos está cifrado y el personal de servicio no tiene acceso a claves de descifrado, el registro de destino se pasa mediante programación a través de un servicio de descifrado que devuelve resultados con ámbito al personal de servicio autorizado. Las vulnerabilidades encontradas en este ejercicio se notifican y se escalan mediante los canales estándar de administración de incidentes de seguridad de Microsoft.
