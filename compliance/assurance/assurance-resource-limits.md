---
title: Límites de recursos de Microsoft 365
description: En este artículo, puede encontrar información sobre los límites de recursos para las distintas aplicaciones de Microsoft 365.
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
ms.openlocfilehash: 54ea001e542cdd1ab078546cf96bd011e27ab1dc
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497500"
---
# <a name="service-resource-limits"></a><span data-ttu-id="c4a12-103">Límites de recursos del servicio</span><span class="sxs-lookup"><span data-stu-id="c4a12-103">Service resource limits</span></span>

<span data-ttu-id="c4a12-104">Los límites de recursos se aplican mediante cuotas (límites) y limitación.</span><span class="sxs-lookup"><span data-stu-id="c4a12-104">Resource limits are enforced using quotas (limits) and throttling.</span></span> <span data-ttu-id="c4a12-105">Azure Active Directory (Azure AD) y los servicios individuales de Microsoft 365 usan ambos.</span><span class="sxs-lookup"><span data-stu-id="c4a12-105">Azure Active Directory (Azure AD) and the individual Microsoft 365 services use both.</span></span> <span data-ttu-id="c4a12-106">Los límites son específicos del servicio y cambian con el tiempo a medida que se agregan nuevas funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="c4a12-106">Limits are service-specific and change over time as new capabilities are added.</span></span> <span data-ttu-id="c4a12-107">Para obtener información detallada sobre los límites actuales de los distintos servicios, consulte los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="c4a12-107">For details on the current limits for the various services, see the following topics:</span></span>

- [<span data-ttu-id="c4a12-108">Restricciones y límites de servicio de Azure AD</span><span class="sxs-lookup"><span data-stu-id="c4a12-108">Azure AD service limits and restrictions</span></span>](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [<span data-ttu-id="c4a12-109">Límites de Exchange Online</span><span class="sxs-lookup"><span data-stu-id="c4a12-109">Exchange Online Limits</span></span>](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [<span data-ttu-id="c4a12-110">Límites y límites de software de SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="c4a12-110">SharePoint Online software boundaries and limits</span></span>](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [<span data-ttu-id="c4a12-111">Límites de Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="c4a12-111">Skype for Business Limits</span></span>](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [<span data-ttu-id="c4a12-112">Límites de velocidad y API de REST de Yammer</span><span class="sxs-lookup"><span data-stu-id="c4a12-112">Yammer REST API and Rate Limits</span></span>](https://developer.yammer.com/docs/rest-api-rate-limits)
- [<span data-ttu-id="c4a12-113">Límites de tamaño de archivo en Sway</span><span class="sxs-lookup"><span data-stu-id="c4a12-113">File Size Limits in Sway</span></span>](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

<span data-ttu-id="c4a12-114">Además de estos límites, se usan varios mecanismos de limitación en Azure AD y Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c4a12-114">In addition to these limits, several throttling mechanisms are used throughout Azure AD and Microsoft 365.</span></span> <span data-ttu-id="c4a12-115">La limitación dentro del servicio es especialmente importante, dado que los recursos de red en los centros de datos de Microsoft están optimizados para el amplio conjunto de clientes que usan los servicios.</span><span class="sxs-lookup"><span data-stu-id="c4a12-115">Throttling within the service is especially important, given that network resources in Microsoft's datacenters are optimized for the broad set of customers that use the services.</span></span> <span data-ttu-id="c4a12-116">Los mecanismos de limitación incluyen:</span><span class="sxs-lookup"><span data-stu-id="c4a12-116">Throttling mechanisms include:</span></span>

- <span data-ttu-id="c4a12-117">Azure AD y Microsoft 365 presentan limitaciones de nivel de usuario, que limitan el número de transacciones o llamadas simultáneas (por script o código) que puede realizar un solo usuario.</span><span class="sxs-lookup"><span data-stu-id="c4a12-117">Azure AD and Microsoft 365 feature user-level throttling, which limit the number of transactions or concurrent calls (by script or code) that can be performed by a single user.</span></span>
- <span data-ttu-id="c4a12-118">Se asigna una directiva de limitación de PowerShell predeterminada a cada inquilino en la creación del espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="c4a12-118">A default PowerShell throttling policy is assigned to each tenant at tenant creation.</span></span> <span data-ttu-id="c4a12-119">Esta configuración afecta a otros elementos, como el número máximo de sesiones simultáneas de PowerShell que puede abrir un solo administrador.</span><span class="sxs-lookup"><span data-stu-id="c4a12-119">These settings affect other items, such as the maximum number of simultaneous PowerShell sessions that can be opened by a single administrator.</span></span>
- <span data-ttu-id="c4a12-120">Cada cliente de Exchange Online tiene una directiva predeterminada de Servicios web de Exchange (EWS) que se afina para las operaciones de cliente ews y limitación que se aplica a todos los clientes de Outlook.</span><span class="sxs-lookup"><span data-stu-id="c4a12-120">Each Exchange Online customer has a default Exchange Web Services (EWS) policy that is tuned for EWS client operations, and throttling that applies to all Outlook clients.</span></span>
