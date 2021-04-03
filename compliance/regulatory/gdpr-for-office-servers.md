---
title: RGPD para servidores de Office
description: Aprenda a cumplir con los requisitos del Reglamento general de protección de datos (GDPR) en los servidores de la oficina.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.collection: MS-Compliance
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: 58f3d9108fe36175c2ce879054a35c2cc94d93c8
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496080"
---
# <a name="gdpr-for-office-on-premises-servers"></a><span data-ttu-id="b40b1-103">RGPD para servidores locales de Office</span><span class="sxs-lookup"><span data-stu-id="b40b1-103">GDPR for Office on-premises Servers</span></span>

<span data-ttu-id="b40b1-p101">El Reglamento general de protección de datos (RGPD) presenta requisitos para que las organizaciones protejan los datos personales y respondan correctamente a las solicitudes de datos personales. Esta serie de artículos proporciona enfoques recomendados para cargas de trabajo locales:</span><span class="sxs-lookup"><span data-stu-id="b40b1-p101">The General Data Protection Regulation (GDPR) introduces requirements for organizations to protect personal data and respond appropriately to data subject requests. This series of articles provides recommended approaches for on-premises workloads:</span></span>

- [<span data-ttu-id="b40b1-106">SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="b40b1-106">SharePoint Server</span></span>](gdpr-for-sharepoint-server.md)

- [<span data-ttu-id="b40b1-107">Exchange Server</span><span class="sxs-lookup"><span data-stu-id="b40b1-107">Exchange Server</span></span>](gdpr-for-exchange-server.md)

- [<span data-ttu-id="b40b1-108">Skype Empresarial Server</span><span class="sxs-lookup"><span data-stu-id="b40b1-108">Skype for Business Server</span></span>](gdpr-for-skype-for-business-server.md)

- [<span data-ttu-id="b40b1-109">Project Server</span><span class="sxs-lookup"><span data-stu-id="b40b1-109">Project Server</span></span>](gdpr-for-project-server.md)

- [<span data-ttu-id="b40b1-110">Office Web Apps Server y Office Online Server</span><span class="sxs-lookup"><span data-stu-id="b40b1-110">Office Web Apps Server and Office Online Server</span></span>](gdpr-for-office-online-server.md)

- [<span data-ttu-id="b40b1-111">Uso compartido de archivos locales</span><span class="sxs-lookup"><span data-stu-id="b40b1-111">On-premises file shares</span></span>](gdpr-for-on-premises-file-shares.md)

<span data-ttu-id="b40b1-112">Para obtener más información sobre el RGPD y cómo puede ayudarle Microsoft, consulte el [Centro de confianza de Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview
).</span><span class="sxs-lookup"><span data-stu-id="b40b1-112">For more information about the GDPR and how Microsoft can help you, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center/privacy/gdpr-overview
).</span></span>

<span data-ttu-id="b40b1-p102">Antes de realizar cualquier trabajo con los datos locales, consulte con sus equipos legales y de cumplimiento para buscar orientación y obtener información sobre los métodos de clasificación existentes para trabajar con datos personales y esquemas. Microsoft ofrece recomendaciones para desarrollar y ampliar esquemas de clasificación en el Kit de herramientas de detección de datos de RGPD de Microsoft en [https://aka.ms/gdprpartners](<https://aka.ms/gdprpartners>). Este kit de herramientas también describe métodos para mover datos locales a la nube donde puede usar funciones de gobierno de datos más complejas, si así lo desea. Los artículos de esta sección proporcionan recomendaciones para datos que se pretende que permanezcan en un entorno local.</span><span class="sxs-lookup"><span data-stu-id="b40b1-p102">Before doing any work with on-premises data, consult with your legal and compliance teams to seek guidance and to learn about existing classification schemas and approaches to working with personal data. Microsoft provides recommendations for developing and extending classifications schemas in the Microsoft GDPR Data Discovery Toolkit at [https://aka.ms/gdprpartners](<https://aka.ms/gdprpartners>). This toolkit also describes approaches for moving on-premises data to the cloud where you can use more sophisticated data governance capabilities, if this is desired. The articles in this section provide recommendations for data that is intended to remain on premises.</span></span>

<span data-ttu-id="b40b1-p103">La siguiente ilustración enumera las capacidades recomendadas que se deben usar en cada una de estas cargas de trabajo para descubrir, clasificar, proteger y vigilar los datos personales. Consulte los artículos de esta sección para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="b40b1-p103">The following illustration lists recommended capabilities to use across each of these workloads to discover, classify, protect, and monitor personal data. See the articles in this section for more information.</span></span>

![Diagrama en el que se describen las funcionalidades para descubrir, clasificar, proteger y supervisar datos personales en distintas cargas de trabajo](../media/gdpr-for-office-servers-image1.png)

## <a name="illustration-description"></a><span data-ttu-id="b40b1-120">Descripción de la ilustración</span><span class="sxs-lookup"><span data-stu-id="b40b1-120">Illustration description</span></span>

<span data-ttu-id="b40b1-121">Por motivos de accesibilidad, en la tabla siguiente se incluyen los mismos ejemplos que en la ilustración.</span><span class="sxs-lookup"><span data-stu-id="b40b1-121">For accessibility, the following table provides the same examples in the illustration.</span></span>

****

|<span data-ttu-id="b40b1-122">Acción</span><span class="sxs-lookup"><span data-stu-id="b40b1-122">Action</span></span>|<span data-ttu-id="b40b1-123">Recursos compartidos de archivos de Windows Server</span><span class="sxs-lookup"><span data-stu-id="b40b1-123">Windows Server file shares</span></span>|<span data-ttu-id="b40b1-124">SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="b40b1-124">SharePoint Server</span></span>|<span data-ttu-id="b40b1-125">Exchange Server</span><span class="sxs-lookup"><span data-stu-id="b40b1-125">Exchange Server</span></span>|<span data-ttu-id="b40b1-126">Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="b40b1-126">Skype for Business</span></span>|<span data-ttu-id="b40b1-127">Project Server</span><span class="sxs-lookup"><span data-stu-id="b40b1-127">Project Server</span></span>|
|---|---|---|---|---|---|
|<span data-ttu-id="b40b1-128">Detectar</span><span class="sxs-lookup"><span data-stu-id="b40b1-128">Discover</span></span>|<span data-ttu-id="b40b1-129">Escáner de Azure Information Protection<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="b40b1-129">Azure Information Protection scanner<sup>\*</sup></span></span>|<span data-ttu-id="b40b1-130">Centro de búsqueda o eDiscovery (después de clasificar los datos)</span><span class="sxs-lookup"><span data-stu-id="b40b1-130">Search Center or eDiscovery (after data is classified)</span></span> <br/><br/> <span data-ttu-id="b40b1-131">Escáner de Azure Information Protection<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="b40b1-131">Azure Information Protection scanner<sup>\*</sup></span></span>|<span data-ttu-id="b40b1-132">Portal de eDiscovery de Exchange</span><span class="sxs-lookup"><span data-stu-id="b40b1-132">Exchange eDiscovery Portal</span></span>|<span data-ttu-id="b40b1-133">Portal de eDiscovery de Exchange</span><span class="sxs-lookup"><span data-stu-id="b40b1-133">Exchange eDiscovery portal</span></span>|<span data-ttu-id="b40b1-134">Scripts SQL de detección y exportación</span><span class="sxs-lookup"><span data-stu-id="b40b1-134">SQL scripts for discovery and exporting</span></span>|
|<span data-ttu-id="b40b1-135">Clasificar</span><span class="sxs-lookup"><span data-stu-id="b40b1-135">Classify</span></span>|<span data-ttu-id="b40b1-136">Escáner de Azure Information Protection<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="b40b1-136">Azure Information Protection scanner<sup>\*</sup></span></span> <br/><br/> <span data-ttu-id="b40b1-137">Tipos de información confidencial de Office 365</span><span class="sxs-lookup"><span data-stu-id="b40b1-137">Office 365 sensitive information types</span></span>|<span data-ttu-id="b40b1-138">Escáner de Azure Information Protection<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="b40b1-138">Azure Information Protection scanner<sup>\*</sup></span></span> <br/><br/> <span data-ttu-id="b40b1-139">Tipos de información confidencial de Office 365</span><span class="sxs-lookup"><span data-stu-id="b40b1-139">Office 365 sensitive information types</span></span>|<span data-ttu-id="b40b1-140">Etiquetas de retención y directivas de retención de Exchange</span><span class="sxs-lookup"><span data-stu-id="b40b1-140">Exchange retention tags and retention policies</span></span>|<span data-ttu-id="b40b1-141">Etiquetas de retención y directivas de retención de Exchange</span><span class="sxs-lookup"><span data-stu-id="b40b1-141">Exchange retention tags and retention policies</span></span>||
|<span data-ttu-id="b40b1-142">Proteger</span><span class="sxs-lookup"><span data-stu-id="b40b1-142">Protect</span></span>||<span data-ttu-id="b40b1-143">Reglas de prevención de pérdida de datos de Exchange Server</span><span class="sxs-lookup"><span data-stu-id="b40b1-143">Exchange Server data loss prevention rules</span></span> <br/><br/> <span data-ttu-id="b40b1-144">Permisos y protección IRM para las bibliotecas</span><span class="sxs-lookup"><span data-stu-id="b40b1-144">Permissions, IRM-protection for libraries</span></span>|<span data-ttu-id="b40b1-145">Reglas de prevención de pérdida de datos de Exchange Server</span><span class="sxs-lookup"><span data-stu-id="b40b1-145">Exchange Server data loss prevention rules</span></span> <br/><br/> <span data-ttu-id="b40b1-146">Integración IRM con Exchange Server</span><span class="sxs-lookup"><span data-stu-id="b40b1-146">IRM integration with Exchange Server</span></span>|||
|<span data-ttu-id="b40b1-147">Monitorear</span><span class="sxs-lookup"><span data-stu-id="b40b1-147">Monitor</span></span>|<span data-ttu-id="b40b1-148">Integrar registros con herramientas SIEM</span><span class="sxs-lookup"><span data-stu-id="b40b1-148">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="b40b1-149">Integrar registros con herramientas SIEM</span><span class="sxs-lookup"><span data-stu-id="b40b1-149">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="b40b1-150">Integrar registros con herramientas SIEM</span><span class="sxs-lookup"><span data-stu-id="b40b1-150">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="b40b1-151">Integrar registros con herramientas SIEM</span><span class="sxs-lookup"><span data-stu-id="b40b1-151">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="b40b1-152">Integrar registros con herramientas SIEM</span><span class="sxs-lookup"><span data-stu-id="b40b1-152">Integrate logs with SIEM tools</span></span>|
|

<span data-ttu-id="b40b1-153"><sup>\*</sup> Tenga en cuenta que la protección cifra el archivo.</span><span class="sxs-lookup"><span data-stu-id="b40b1-153"><sup>\*</sup> Note that protection encrypts the file.</span></span> <span data-ttu-id="b40b1-154">Por lo tanto, SharePoint Server no puede encontrar tipos de información confidencial en los archivos protegidos.</span><span class="sxs-lookup"><span data-stu-id="b40b1-154">Consequently, SharePoint Server can't find the sensitive information types in protected files.</span></span>
