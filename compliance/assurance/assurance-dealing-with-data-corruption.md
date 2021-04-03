---
title: Microsoft 365 que se ocupa de la corrupción de datos
description: En este artículo se explica la corrupción de datos en Microsoft 365 y los esfuerzos realizados por Microsoft para evitar y recuperar datos.
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
ms.openlocfilehash: 9e9f0951f7e349cc70bc96bb6a2d62275848cf04
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497591"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a><span data-ttu-id="5cd0e-103">Tratamiento de daños en datos en Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5cd0e-103">Dealing with data corruption in Microsoft 365</span></span>

<span data-ttu-id="5cd0e-104">Uno de los aspectos desafiantes de la ejecución de un servicio en la nube a gran escala es cómo controlar la corrupción de datos, dado el gran volumen de datos y sistemas independientes.</span><span class="sxs-lookup"><span data-stu-id="5cd0e-104">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems.</span></span> <span data-ttu-id="5cd0e-105">Los daños en los datos pueden deberse a:</span><span class="sxs-lookup"><span data-stu-id="5cd0e-105">Data corruption can be caused by:</span></span>

- <span data-ttu-id="5cd0e-106">Errores de la aplicación o la infraestructura, que dañan parte o todo el estado de la aplicación</span><span class="sxs-lookup"><span data-stu-id="5cd0e-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span>
- <span data-ttu-id="5cd0e-107">Problemas de hardware que resultan en la pérdida de datos o la incapacidad para leer datos</span><span class="sxs-lookup"><span data-stu-id="5cd0e-107">Hardware issues that result in lost data or an inability to read data</span></span>
- <span data-ttu-id="5cd0e-108">Errores operativos humanos</span><span class="sxs-lookup"><span data-stu-id="5cd0e-108">Human operational errors</span></span>
- <span data-ttu-id="5cd0e-109">Hackers malintencionados y empleados inconformes</span><span class="sxs-lookup"><span data-stu-id="5cd0e-109">Malicious hackers and disgruntled employees</span></span>
- <span data-ttu-id="5cd0e-110">Incidentes en servicios externos que resultan en una pérdida de datos</span><span class="sxs-lookup"><span data-stu-id="5cd0e-110">Incidents in external services that result in some loss of data</span></span>

<span data-ttu-id="5cd0e-111">Dado que una mayor resistencia en la integridad de datos significa menos incidentes de corrupción de datos, Microsoft ha integrado mecanismos de protección de Microsoft 365 para evitar que se produjesen daños, así como sistemas y procesos que nos permiten recuperar datos si lo hace.</span><span class="sxs-lookup"><span data-stu-id="5cd0e-111">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Microsoft 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does.</span></span> <span data-ttu-id="5cd0e-112">Existen comprobaciones y procesos en las distintas etapas del proceso de versión de ingeniería para aumentar la resistencia frente a daños en los datos, incluidos:</span><span class="sxs-lookup"><span data-stu-id="5cd0e-112">Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>

- <span data-ttu-id="5cd0e-113">Diseño del sistema</span><span class="sxs-lookup"><span data-stu-id="5cd0e-113">System Design</span></span>
- <span data-ttu-id="5cd0e-114">Organización y estructura de código</span><span class="sxs-lookup"><span data-stu-id="5cd0e-114">Code organization and structure</span></span>
- <span data-ttu-id="5cd0e-115">Revisión de código</span><span class="sxs-lookup"><span data-stu-id="5cd0e-115">Code review</span></span>
- <span data-ttu-id="5cd0e-116">Pruebas unitarias, pruebas de integración y pruebas del sistema</span><span class="sxs-lookup"><span data-stu-id="5cd0e-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="5cd0e-117">Pruebas/puertas de cables de viaje</span><span class="sxs-lookup"><span data-stu-id="5cd0e-117">Trip wires tests/gates</span></span>

<span data-ttu-id="5cd0e-118">Dentro de los entornos de producción de Microsoft 365, la replicación del mismo nivel entre centros de datos garantiza que siempre haya varias copias en directo de los datos.</span><span class="sxs-lookup"><span data-stu-id="5cd0e-118">Within Microsoft 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data.</span></span> <span data-ttu-id="5cd0e-119">Las imágenes y scripts estándar se usan para recuperar servidores perdidos y los datos replicados se usan para restaurar los datos del cliente.</span><span class="sxs-lookup"><span data-stu-id="5cd0e-119">Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data.</span></span> <span data-ttu-id="5cd0e-120">Debido a los procesos y comprobaciones de resistencia de datos integrados, Microsoft solo mantiene copias de seguridad de la documentación del sistema de información de Microsoft 365 (incluida la documentación relacionada con la seguridad), mediante la replicación integrada en SharePoint Online y nuestra herramienta de repositorio de código interno, Source Depot.</span><span class="sxs-lookup"><span data-stu-id="5cd0e-120">Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Microsoft 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot.</span></span> <span data-ttu-id="5cd0e-121">La documentación del sistema se almacena en SharePoint Online y Source Depot contiene imágenes del sistema y de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5cd0e-121">System documentation is stored in SharePoint Online, and Source Depot contains system and application images.</span></span> <span data-ttu-id="5cd0e-122">SharePoint Online y Source Depot usan el control de versiones y se replican casi en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="5cd0e-122">Both SharePoint Online and Source Depot use versioning and are replicated in near real time.</span></span>
