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
# <a name="internal-logging-for-microsoft-365-engineering"></a><span data-ttu-id="2c923-103">Registro interno para la ingeniería de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2c923-103">Internal logging for Microsoft 365 engineering</span></span>

<span data-ttu-id="2c923-104">Además de los eventos y los datos de registro disponibles para los clientes, Microsoft mantiene un sistema interno de recopilación de datos de registro que está disponible para Microsoft 365 ingenieros.</span><span class="sxs-lookup"><span data-stu-id="2c923-104">In addition to the events and log data available for customers, Microsoft maintains an internal log data collection system that is available to Microsoft 365 engineers.</span></span> <span data-ttu-id="2c923-105">Muchos tipos diferentes de datos de registro se cargan desde servidores de Microsoft 365 a una solución de supervisión de seguridad propietaria para el análisis casi en tiempo real (NRT) y un servicio informático interno de big data (Cosmos) para el almacenamiento a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="2c923-105">Many different types of log data are uploaded from Microsoft 365 servers to a proprietary security monitoring solution for near real-time (NRT) analysis and an internal, big data computing service (Cosmos) for long-term storage.</span></span> <span data-ttu-id="2c923-106">Esta transferencia de datos se produce a través de una conexión TLS validada por FIPS 140-2 en puertos y protocolos aprobados mediante una herramienta de automatización propietaria denominada Office Data Loader (ODL).</span><span class="sxs-lookup"><span data-stu-id="2c923-106">This data transfer occurs over a FIPS 140-2-validated TLS connection on approved ports and protocols using a proprietary automation tool called the Office Data Loader (ODL).</span></span> <span data-ttu-id="2c923-107">Las herramientas usadas en Microsoft 365 recopilar y procesar registros de auditoría no permiten cambios permanentes o irreversibles en el contenido del registro de auditoría original ni en el orden de tiempo.</span><span class="sxs-lookup"><span data-stu-id="2c923-107">The tools used in Microsoft 365 to collect and process audit records do not allow permanent or irreversible changes to the original audit record content or time ordering.</span></span>

<span data-ttu-id="2c923-108">Los equipos de servicio usan Cosmos como repositorio centralizado para realizar un análisis del uso de aplicaciones, medir el rendimiento operativo y del sistema y buscar anomalías y patrones que puedan indicar problemas o problemas de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2c923-108">Service teams use Cosmos as a centralized repository to conduct an analysis of application usage, to measure system and operational performance, and to look for abnormalities and patterns that may indicate problems or security issues.</span></span> <span data-ttu-id="2c923-109">Cada equipo de servicio carga una línea base que incluye:</span><span class="sxs-lookup"><span data-stu-id="2c923-109">Each service team uploads a baseline that includes:</span></span>

- <span data-ttu-id="2c923-110">Registros de eventos</span><span class="sxs-lookup"><span data-stu-id="2c923-110">Event logs</span></span>
- <span data-ttu-id="2c923-111">Registros de AppLocker</span><span class="sxs-lookup"><span data-stu-id="2c923-111">AppLocker logs</span></span>
- <span data-ttu-id="2c923-112">Datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="2c923-112">Performance data</span></span>
- <span data-ttu-id="2c923-113">System Center datos</span><span class="sxs-lookup"><span data-stu-id="2c923-113">System Center data</span></span>
- <span data-ttu-id="2c923-114">Registros de detalles de llamadas</span><span class="sxs-lookup"><span data-stu-id="2c923-114">Call detail records</span></span>
- <span data-ttu-id="2c923-115">Datos de calidad de la experiencia</span><span class="sxs-lookup"><span data-stu-id="2c923-115">Quality of experience data</span></span>
- <span data-ttu-id="2c923-116">Registros del servidor web iis</span><span class="sxs-lookup"><span data-stu-id="2c923-116">IIS Web Server logs</span></span>
- <span data-ttu-id="2c923-117">SQL Server registros</span><span class="sxs-lookup"><span data-stu-id="2c923-117">SQL Server logs</span></span>
- <span data-ttu-id="2c923-118">Datos de Syslog</span><span class="sxs-lookup"><span data-stu-id="2c923-118">Syslog data</span></span>
- <span data-ttu-id="2c923-119">Registros de auditoría de seguridad</span><span class="sxs-lookup"><span data-stu-id="2c923-119">Security audit logs</span></span>

<span data-ttu-id="2c923-120">Antes de cargar, la aplicación ODL usa un servicio de depuración para quitar los campos que contienen datos de cliente, como información de inquilino e información identificable del usuario final, y reemplazar esos campos por un valor hash.</span><span class="sxs-lookup"><span data-stu-id="2c923-120">Prior to uploading, the ODL application uses a scrubbing service to remove any fields that contain customer data, such as tenant information and end-user identifiable information, and replace those fields with a hash value.</span></span> <span data-ttu-id="2c923-121">Los registros de depuración se cargan en Cosmos y en la solución de supervisión de seguridad NRT que analiza los registros en busca de posibles eventos de seguridad e indicadores de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="2c923-121">The scrubbed logs are uploaded to Cosmos and to the NRT security monitoring solution that analyzes the logs for potential security events and performance indicators.</span></span> <span data-ttu-id="2c923-122">El período de retención de datos del registro de auditoría Cosmos determina los equipos de servicio; La mayoría de los datos del registro de auditoría se conservan durante 90 días o más para admitir investigaciones de incidentes de seguridad y cumplir con los requisitos de retención normativos.</span><span class="sxs-lookup"><span data-stu-id="2c923-122">The period of audit log data retention in Cosmos is determined by the service teams; most audit log data is retained for 90 days or longer to support security incident investigations and to meet regulatory retention requirements.</span></span>

<span data-ttu-id="2c923-123">El acceso Microsoft 365 los datos almacenados en Cosmos está restringido al personal autorizado.</span><span class="sxs-lookup"><span data-stu-id="2c923-123">Access to Microsoft 365 data stored in Cosmos is restricted to authorized personnel.</span></span> <span data-ttu-id="2c923-124">Microsoft restringe la administración de registros de auditoría a un subconjunto limitado de miembros del equipo de seguridad responsables de la funcionalidad de auditoría.</span><span class="sxs-lookup"><span data-stu-id="2c923-124">Microsoft restricts the management of audit logs to a limited subset of Security Team members responsible for audit functionality.</span></span> <span data-ttu-id="2c923-125">El equipo de seguridad no tiene acceso administrativo permanente a Cosmos y todos los cambios se registran y auditan.</span><span class="sxs-lookup"><span data-stu-id="2c923-125">The Security Team does not have standing administrative access to Cosmos, and all changes are recorded and audited.</span></span>

<span data-ttu-id="2c923-126">Después del análisis NRT, cada equipo de servicio puede usar herramientas de análisis y paneles para la correlación de datos, consultas interactivas y análisis de datos.</span><span class="sxs-lookup"><span data-stu-id="2c923-126">After NRT analysis, each service team can use analysis tools and dashboards for data correlation, interactive queries, and data analytics.</span></span> <span data-ttu-id="2c923-127">Estos informes se usan para supervisar y mejorar el rendimiento general del servicio.</span><span class="sxs-lookup"><span data-stu-id="2c923-127">These reports are used to monitor and improve the overall performance of the service.</span></span>
