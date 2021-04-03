---
title: Controles de acceso empresarial de Microsoft 365 Yammer
description: Este artículo contiene un breve resumen sobre los controles de acceso empresarial de Yammer en el entorno de producción.
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
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: df345d922bbd0c9106cf0714377803a9c0870d82
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497352"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="c9d33-103">Controles de acceso empresarial de Yammer</span><span class="sxs-lookup"><span data-stu-id="c9d33-103">Yammer enterprise access controls</span></span> 

<span data-ttu-id="c9d33-104">El acceso físico y lógico al entorno de producción de Yammer está restringido a un pequeño conjunto de personas (infraestructura y operaciones).</span><span class="sxs-lookup"><span data-stu-id="c9d33-104">Physical and logical access to the Yammer production environment is restricted to a small set of people (infrastructure and operations).</span></span> <span data-ttu-id="c9d33-105">Al igual que con otros ingenieros de Microsoft 365, los ingenieros de Yammer no tienen acceso permanente a los datos de los clientes.</span><span class="sxs-lookup"><span data-stu-id="c9d33-105">As with other Microsoft 365 engineers, Yammer engineers have zero standing access to customer data.</span></span> <span data-ttu-id="c9d33-106">El acceso debe solicitarse mediante un sistema de control de acceso just-in-time basado en aprobación similar a Lockbox con un número limitado de aprobadores.</span><span class="sxs-lookup"><span data-stu-id="c9d33-106">Access must be requested using an approval-based just-in-time access control system similar to Lockbox with a limited number of approvers.</span></span> <span data-ttu-id="c9d33-107">Los aprobadores comprueban la solicitud (por ejemplo, comprueban si la solicitud es legítima en función de la necesidad, el caso empresarial, la hora, etc.) y, a continuación, aprueban o deniegan la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c9d33-107">Approvers verify the request (for example, they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request.</span></span> <span data-ttu-id="c9d33-108">Si se aprueba la solicitud, se concede acceso a JIT por un tiempo definido y limitado.</span><span class="sxs-lookup"><span data-stu-id="c9d33-108">If the request is approved, JIT access is granted for a defined and limited time.</span></span> <span data-ttu-id="c9d33-109">Una vez superado el tiempo de acceso, el acceso expira automáticamente.</span><span class="sxs-lookup"><span data-stu-id="c9d33-109">After access time is exceeded, the access automatically expires.</span></span>

<span data-ttu-id="c9d33-110">Al igual que con otros servicios de Microsoft 365, todo el acceso al entorno de producción de Yammer usa autenticación multifactor.</span><span class="sxs-lookup"><span data-stu-id="c9d33-110">As with other Microsoft 365 services, all access to the Yammer production environment uses multi-factor authentication.</span></span> <span data-ttu-id="c9d33-111">Todo el acceso y el historial de comandos se atribuyó a un usuario y el equipo de seguridad de Yammer lo registra y revisa periódicamente.</span><span class="sxs-lookup"><span data-stu-id="c9d33-111">All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="c9d33-112">Para obtener más información acerca de la administración y administración de Yammer, consulte [Ayuda de administración de Yammer](/yammer/yammer-landing-page).</span><span class="sxs-lookup"><span data-stu-id="c9d33-112">For more information about Yammer administration and management, see [Yammer admin help](/yammer/yammer-landing-page).</span></span>