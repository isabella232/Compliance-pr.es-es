---
title: Controles de acceso administrativo en Microsoft 365
description: En este artículo se proporciona información general sobre los controles de acceso administrativo y la categorización de datos en Microsoft 365.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: d3d6cd30fbe682de979d5c04943c57cedc86552f
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120719"
---
# <a name="administrative-access-controls-in-microsoft-365"></a><span data-ttu-id="b5526-103">Controles de acceso administrativo en Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b5526-103">Administrative access controls in Microsoft 365</span></span> 

<span data-ttu-id="b5526-104">Microsoft ha invertido mucho en sistemas y controles que automatizan la mayoría de las operaciones de Microsoft 365, a la vez que limita intencionadamente el acceso al contenido de los clientes por parte de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b5526-104">Microsoft has invested heavily in systems and controls that automate most Microsoft 365 operations while intentionally limiting access to customer content by Microsoft.</span></span> <span data-ttu-id="b5526-105">Los humanos rigen el servicio y el software opera el servicio.</span><span class="sxs-lookup"><span data-stu-id="b5526-105">Humans govern the service, and software operates the service.</span></span> <span data-ttu-id="b5526-106">Esta estructura permite a Microsoft administrar Microsoft 365 a escala y administrar los riesgos de las amenazas internas para el contenido del cliente.</span><span class="sxs-lookup"><span data-stu-id="b5526-106">This structure enables Microsoft to manage Microsoft 365 at scale and manage the risks of internal threats to customer content.</span></span>

<span data-ttu-id="b5526-107">De forma predeterminada, los ingenieros de Microsoft tienen cero privilegios administrativos permanentes y ningún acceso permanente al contenido de los clientes en Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b5526-107">By default, Microsoft engineers have zero standing administrative privileges and zero standing access to customer content in Microsoft 365.</span></span> <span data-ttu-id="b5526-108">Un ingeniero de Microsoft puede tener acceso limitado, auditado y protegido al contenido de un cliente durante un período de tiempo limitado.</span><span class="sxs-lookup"><span data-stu-id="b5526-108">A Microsoft engineer can have limited, audited, and secured access to a customer's content for a limited amount of time.</span></span> <span data-ttu-id="b5526-109">El acceso es solo cuando es necesario para las operaciones de servicio y solo cuando lo aprueba un miembro de la administración superior de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b5526-109">Access is only when necessary for service operations and only when approved by a member of Microsoft senior management.</span></span> <span data-ttu-id="b5526-110">Para los clientes con licencia de caja de seguridad del cliente, el cliente proporciona la aprobación de acceso a su contenido hospedado en Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b5526-110">For Customer Lockbox licensed customers, the customer provides access approval to their content hosted on Microsoft 365.</span></span>

<span data-ttu-id="b5526-111">Microsoft proporciona servicios en línea con varias formas de entrega en la nube:</span><span class="sxs-lookup"><span data-stu-id="b5526-111">Microsoft provides online services using multiple forms of cloud delivery:</span></span>

- <span data-ttu-id="b5526-112">**Nubes públicas:** Incluye versiones multiinquilino de Microsoft 365, Azure y otros servicios hospedados en Norteamérica, América del Sur, Europa, Asia, Australia, etc.</span><span class="sxs-lookup"><span data-stu-id="b5526-112">**Public clouds:** Includes multi-tenant versions of Microsoft 365, Azure, and other services hosted in North America, South America, Europe, Asia, Australia, etc.</span></span>
- <span data-ttu-id="b5526-113">**Nubes nacionales:** Incluye todas las nubes soberanas y operadas por terceros fuera de los Estados Unidos (excepto las que se han indicado anteriormente), como Microsoft 365 en China (operado por 21Vianet) y Microsoft 365 en Alemania (operado por Microsoft, pero bajo un modelo en el que un administrador de datos alemán, Deutsche Telekom, controla y supervisa el acceso de Microsoft a los datos de clientes y sistemas que contienen datos de clientes).</span><span class="sxs-lookup"><span data-stu-id="b5526-113">**National clouds:** Includes all sovereign and third party-operated clouds outside of the United States (except ones noted previously), such as Microsoft 365 in China (operated by 21Vianet), and Microsoft 365 in Germany (operated by Microsoft, but under a model in which a German data trustee, Deutsche Telekom, controls and monitors Microsoft's access to customer data and systems that contain customer data).</span></span>
- <span data-ttu-id="b5526-114">**Nubes de administración pública:** Incluye los servicios de Microsoft 365 y Azure que están disponibles para los clientes gubernamentales de Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="b5526-114">**Government clouds:** Includes Microsoft 365 and Azure services that are available to United States government customers.</span></span>

<span data-ttu-id="b5526-115">Para este artículo, los servicios de Microsoft 365 incluyen:</span><span class="sxs-lookup"><span data-stu-id="b5526-115">For purposes of this article, Microsoft 365 services include:</span></span>

- [<span data-ttu-id="b5526-116">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b5526-116">Exchange Online</span></span>](/Exchange/exchange-online)
- [<span data-ttu-id="b5526-117">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="b5526-117">Exchange Online Protection</span></span>](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [<span data-ttu-id="b5526-118">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="b5526-118">SharePoint Online</span></span>](/sharepoint/sharepoint-online)
- [<span data-ttu-id="b5526-119">OneDrive para la Empresa</span><span class="sxs-lookup"><span data-stu-id="b5526-119">OneDrive for Business</span></span>](/OneDrive/onedrive)
- [<span data-ttu-id="b5526-120">Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="b5526-120">Skype for Business</span></span>](/SkypeForBusiness/skype-for-business-online)
- [<span data-ttu-id="b5526-121">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b5526-121">Microsoft Teams</span></span>](/MicrosoftTeams/Teams-overview)
- [<span data-ttu-id="b5526-122">Yammer</span><span class="sxs-lookup"><span data-stu-id="b5526-122">Yammer</span></span>](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a><span data-ttu-id="b5526-123">Controles de acceso de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b5526-123">Microsoft 365 access controls</span></span>

<span data-ttu-id="b5526-124">Con fines de control de acceso, Microsoft clasifica los datos de Microsoft 365 como datos de clientes u otros tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="b5526-124">For access control purposes, Microsoft categorizes Microsoft 365 data as customer data or other types of data.</span></span>

### <a name="customer-data"></a><span data-ttu-id="b5526-125">Datos de cliente</span><span class="sxs-lookup"><span data-stu-id="b5526-125">Customer data</span></span>

<span data-ttu-id="b5526-126">Los datos de cliente son todos los datos proporcionados por un cliente o en su nombre al usar los servicios de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b5526-126">Customer data is all data provided by or on behalf of a customer when using Microsoft 365 services.</span></span> <span data-ttu-id="b5526-127">Estos datos son contenido del cliente creado o cargado directamente por usuarios de Microsoft 365, incluidos:</span><span class="sxs-lookup"><span data-stu-id="b5526-127">This data is customer content directly created or uploaded by Microsoft 365 users, including:</span></span>

- <span data-ttu-id="b5526-128">Mensajes de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="b5526-128">Emails</span></span>
- <span data-ttu-id="b5526-129">Contenido de SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="b5526-129">SharePoint Online content</span></span>
- <span data-ttu-id="b5526-130">Mensajes instantáneos</span><span class="sxs-lookup"><span data-stu-id="b5526-130">Instant messages</span></span>
- <span data-ttu-id="b5526-131">Elementos de calendario</span><span class="sxs-lookup"><span data-stu-id="b5526-131">Calendar items</span></span>
- <span data-ttu-id="b5526-132">Documentos</span><span class="sxs-lookup"><span data-stu-id="b5526-132">Documents</span></span>
- <span data-ttu-id="b5526-133">Contactos</span><span class="sxs-lookup"><span data-stu-id="b5526-133">Contacts</span></span>
- <span data-ttu-id="b5526-134">Información identificable del usuario final (EUII) (datos que son exclusivos de un usuario o que se pueden vincular a un usuario individual pero que no incluyen contenido del cliente)</span><span class="sxs-lookup"><span data-stu-id="b5526-134">End-user identifiable information (EUII) (data that is unique to a user or that is linkable to an individual user but does not include customer content)</span></span>

### <a name="other-types-of-data"></a><span data-ttu-id="b5526-135">Otros tipos de datos</span><span class="sxs-lookup"><span data-stu-id="b5526-135">Other types of data</span></span>

<span data-ttu-id="b5526-136">Otros tipos de datos son:</span><span class="sxs-lookup"><span data-stu-id="b5526-136">Other types of data include:</span></span>

- <span data-ttu-id="b5526-137">**Datos de la cuenta:** Incluye datos administrativos (información proporcionada por los administradores al registrarse o comprar servicios) y datos de pago (información sobre instrumentos de pago, como los detalles de la tarjeta de crédito).</span><span class="sxs-lookup"><span data-stu-id="b5526-137">**Account data:** Includes administrative data (information provided by administrators when they sign-up or purchase services), and payment data (information about payment instruments, such as credit card details).</span></span>
- <span data-ttu-id="b5526-138">**Información de identificación organizativa:** Incluye datos usados para identificar un inquilino, datos de uso y no vinculables a un usuario individual o incluidos en el contenido del cliente.</span><span class="sxs-lookup"><span data-stu-id="b5526-138">**Organizationally identifiable information:** Includes data used to identify a tenant, usage data, and not linkable to an individual user or included in customer content.</span></span>
- <span data-ttu-id="b5526-139">**Metadatos del sistema:** Incluye registros de servicio que contienen opciones de configuración, estado del sistema, direcciones IP de Microsoft e información técnica sobre suscripciones e inquilinos.</span><span class="sxs-lookup"><span data-stu-id="b5526-139">**System metadata:** Includes service logs that contain configuration settings, system status, Microsoft IP addresses, and technical information about subscriptions and tenants.</span></span>

<span data-ttu-id="b5526-140">Microsoft ha establecido mecanismos de control de acceso para garantizar que nadie tiene acceso no aprobado a los datos de clientes ni a los datos de control de acceso.</span><span class="sxs-lookup"><span data-stu-id="b5526-140">Microsoft has established access control mechanisms to ensure that no one has unapproved access to Customer Data or access control data.</span></span> <span data-ttu-id="b5526-141">Los datos de control de acceso administran el acceso a otros tipos de datos o funciones dentro del entorno, incluido el acceso al contenido del cliente o EUII, las contraseñas de Microsoft, los certificados de seguridad y otros datos relacionados con la autenticación.</span><span class="sxs-lookup"><span data-stu-id="b5526-141">Access control data manages access to other types of data or functions within the environment, including access to customer content or EUII, Microsoft passwords, security certificates, and other authentication-related data.</span></span> <span data-ttu-id="b5526-142">Los mecanismos de control de acceso también protegen contra el acceso físico, lógico o remoto no aprobado al entorno de producción de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b5526-142">Access control mechanisms also guard against unapproved physical, logical, or remote access to the Microsoft 365 production environment.</span></span>

<span data-ttu-id="b5526-143">Hay tres categorías de controles de acceso usados por Microsoft para el funcionamiento de Microsoft 365:</span><span class="sxs-lookup"><span data-stu-id="b5526-143">There are three categories of access controls used by Microsoft for operating Microsoft 365:</span></span>

- <span data-ttu-id="b5526-144">Controles de aislamiento</span><span class="sxs-lookup"><span data-stu-id="b5526-144">Isolation controls</span></span>
- <span data-ttu-id="b5526-145">Controles de personal</span><span class="sxs-lookup"><span data-stu-id="b5526-145">Personnel controls</span></span>
- <span data-ttu-id="b5526-146">Controles de tecnología</span><span class="sxs-lookup"><span data-stu-id="b5526-146">Technology controls</span></span>

<span data-ttu-id="b5526-147">Cuando se combinan, estos controles ayudan a evitar y detectar acciones malintencionadas en Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b5526-147">When combined, these controls help prevent and detect malicious actions in Microsoft 365.</span></span> <span data-ttu-id="b5526-148">Además de los controles de aislamiento, personal y tecnología usados por Microsoft, hay una cuarta categoría de controles: los controles implementados por los clientes.</span><span class="sxs-lookup"><span data-stu-id="b5526-148">In addition to the isolation, personnel, and technology controls used by Microsoft, there is a fourth category of controls: those controls implemented by customers.</span></span>

<span data-ttu-id="b5526-149">Microsoft 365 le permite administrar los datos de la misma forma que los datos se administran en entornos locales.</span><span class="sxs-lookup"><span data-stu-id="b5526-149">Microsoft 365 allows you to manage data the same way data is managed in on-premises environments.</span></span> <span data-ttu-id="b5526-150">La persona que se suscribe a una organización para Microsoft 365 se convierte automáticamente en administrador global.</span><span class="sxs-lookup"><span data-stu-id="b5526-150">The person who signs up an organization for Microsoft 365 automatically becomes a global administrator.</span></span> <span data-ttu-id="b5526-151">El administrador global tiene acceso a todas las características de los portales de administración y puede:</span><span class="sxs-lookup"><span data-stu-id="b5526-151">The global admin has access to all features in Management Portals and can:</span></span>

- <span data-ttu-id="b5526-152">Crear o editar usuarios</span><span class="sxs-lookup"><span data-stu-id="b5526-152">Create or edit users</span></span>
- <span data-ttu-id="b5526-153">Asignar roles de administrador a otros usuarios</span><span class="sxs-lookup"><span data-stu-id="b5526-153">Assign admin roles to others</span></span>
- <span data-ttu-id="b5526-154">Restablecer contraseñas de usuario</span><span class="sxs-lookup"><span data-stu-id="b5526-154">Reset user passwords</span></span>
- <span data-ttu-id="b5526-155">Administrar licencias de usuario</span><span class="sxs-lookup"><span data-stu-id="b5526-155">Manage user licenses</span></span>
- <span data-ttu-id="b5526-156">Administrar dominios</span><span class="sxs-lookup"><span data-stu-id="b5526-156">Manage domains</span></span>
- <span data-ttu-id="b5526-157">Aprobar solicitudes de caja de seguridad del cliente</span><span class="sxs-lookup"><span data-stu-id="b5526-157">Approve Customer Lockbox requests</span></span>

<span data-ttu-id="b5526-158">Se recomienda que cada organización configure al menos dos cuentas de administrador.</span><span class="sxs-lookup"><span data-stu-id="b5526-158">We recommend that each organization configure at least two admin accounts.</span></span> <span data-ttu-id="b5526-159">Para las grandes organizaciones empresariales, se recomiendan cuentas de administrador especializadas que atienden diferentes funciones.</span><span class="sxs-lookup"><span data-stu-id="b5526-159">For large enterprise organizations, we recommend specialized admin accounts that serve different functions.</span></span>

<span data-ttu-id="b5526-160">Para obtener información acerca de la asignación de roles y permisos de administrador, vea [Asignar roles de administrador](/microsoft-365/admin/add-users/assign-admin-roles) y Acerca de los roles de [administrador.](/microsoft-365/admin/add-users/about-admin-roles)</span><span class="sxs-lookup"><span data-stu-id="b5526-160">For information about assigning admin roles and permissions, see [Assign admin roles](/microsoft-365/admin/add-users/assign-admin-roles) and [About admin roles](/microsoft-365/admin/add-users/about-admin-roles).</span></span>

## <a name="related-links"></a><span data-ttu-id="b5526-161">Vínculos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5526-161">Related Links</span></span>

- [<span data-ttu-id="b5526-162">Aislamiento en Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b5526-162">Isolation in Microsoft 365</span></span>](assurance-isolation-in-microsoft-365.md)
- [<span data-ttu-id="b5526-163">Filtrado previo al empleo de Microsoft</span><span class="sxs-lookup"><span data-stu-id="b5526-163">Microsoft pre-employment screening</span></span>](assurance-pre-employment-screening.md)
- [<span data-ttu-id="b5526-164">Comprobación de antecedentes en la nube de Microsoft</span><span class="sxs-lookup"><span data-stu-id="b5526-164">Microsoft cloud background check</span></span>](assurance-cloud-background-check.md)
- [<span data-ttu-id="b5526-165">Auditoría y supervisión de controles de acceso</span><span class="sxs-lookup"><span data-stu-id="b5526-165">Monitoring and Auditing Access Controls</span></span>](assurance-monitoring-and-auditing-access-controls.md)
- [<span data-ttu-id="b5526-166">Controles de acceso de Yammer Enterprise</span><span class="sxs-lookup"><span data-stu-id="b5526-166">Yammer Enterprise Access Controls</span></span>](assurance-yammer-enterprise-access-controls.md)
