---
title: Cifrado para datos en tránsito
description: En este artículo, busque una breve explicación de cómo Microsoft cifra los datos de cliente de Microsoft 365 en tránsito.
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 227f74140ecd9b6283b92e8b0e87bd70912ec8e3
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497251"
---
# <a name="encryption-for-data-in-transit"></a><span data-ttu-id="59933-103">Cifrado para datos en tránsito</span><span class="sxs-lookup"><span data-stu-id="59933-103">Encryption for data-in-transit</span></span>

<span data-ttu-id="59933-104">Además de proteger los datos de los clientes en reposo, Microsoft usa tecnologías de cifrado para proteger los datos de los clientes en tránsito.</span><span class="sxs-lookup"><span data-stu-id="59933-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect customer data in transit.</span></span> <span data-ttu-id="59933-105">Los datos están en tránsito:</span><span class="sxs-lookup"><span data-stu-id="59933-105">Data is in transit:</span></span>

- <span data-ttu-id="59933-106">cuando un equipo cliente se comunica con un servidor Microsoft;</span><span class="sxs-lookup"><span data-stu-id="59933-106">when a client machine communicates with a Microsoft server;</span></span>
- <span data-ttu-id="59933-107">cuando un servidor Microsoft se comunica con otro servidor de Microsoft; y</span><span class="sxs-lookup"><span data-stu-id="59933-107">when a Microsoft server communicates with another Microsoft server; and</span></span>
- <span data-ttu-id="59933-108">cuando un servidor de Microsoft se comunica con un servidor que no es de Microsoft (por ejemplo, Exchange Online entrega correo electrónico a un servidor de correo electrónico de terceros).</span><span class="sxs-lookup"><span data-stu-id="59933-108">when a Microsoft server communicates with a non-Microsoft server (for example, Exchange Online delivering email to a third-party email server).</span></span>

<span data-ttu-id="59933-109">Las comunicaciones entre centros de datos entre servidores de Microsoft tienen lugar a través de TLS o IPsec, y todos los servidores orientados al cliente negocian una sesión segura con TLS con máquinas cliente (por ejemplo, Exchange Online usa TLS 1.2 con una intensidad de cifrado de 256 bits (se valida FIPS 140-2 nivel 2).</span><span class="sxs-lookup"><span data-stu-id="59933-109">Inter-data center communications between Microsoft servers take place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (for example, Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated).</span></span> <span data-ttu-id="59933-110">(Consulte [Technical reference details about encryption](/microsoft-365/compliance/technical-reference-details-about-encryption) para obtener una lista de conjuntos de cifrado TLS admitidos por Office 365). Esto se aplica a los protocolos que usan clientes como Outlook, Skype Empresarial, Microsoft Teams y Outlook en la web (por ejemplo, HTTP, POP3, etc.).</span><span class="sxs-lookup"><span data-stu-id="59933-110">(See [Technical reference details about encryption](/microsoft-365/compliance/technical-reference-details-about-encryption) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, Microsoft Teams, and Outlook on the web (for example, HTTP, POP3, etc.).</span></span>

<span data-ttu-id="59933-111">Microsoft IT SSL emite los certificados públicos mediante SSLAdmin, una herramienta interna de Microsoft para proteger la confidencialidad de la información transmitida.</span><span class="sxs-lookup"><span data-stu-id="59933-111">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information.</span></span> <span data-ttu-id="59933-112">Todos los certificados emitidos por Microsoft IT tienen una longitud mínima de 2048 bits y el cumplimiento de la confianza web requiere SSLAdmin para asegurarse de que los certificados se emiten solo a direcciones IP públicas propiedad de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="59933-112">All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and Webtrust compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft.</span></span> <span data-ttu-id="59933-113">Las direcciones IP que no cumplan este criterio se enrutan a través de un proceso de excepción.</span><span class="sxs-lookup"><span data-stu-id="59933-113">Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="59933-114">Todos los detalles de implementación, como la versión de TLS que se usa, si el secreto de reenvío (FS) está habilitado, el orden de los conjuntos de cifrado, etc., están disponibles públicamente.</span><span class="sxs-lookup"><span data-stu-id="59933-114">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly.</span></span> <span data-ttu-id="59933-115">Una forma de ver estos detalles es usar un sitio web de terceros, como [Qualys SSL Labs](https://www.ssllabs.com).</span><span class="sxs-lookup"><span data-stu-id="59933-115">One way to see these details is to use a third-party website, such as [Qualys SSL Labs](https://www.ssllabs.com).</span></span> <span data-ttu-id="59933-116">A continuación se muestran los vínculos a páginas de prueba automatizadas de Qualys que muestran información para los siguientes servicios:</span><span class="sxs-lookup"><span data-stu-id="59933-116">Below are the links to automated test pages from Qualys that display information for the following services:</span></span>

- [<span data-ttu-id="59933-117">Office 365 Portal</span><span class="sxs-lookup"><span data-stu-id="59933-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="59933-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="59933-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="59933-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="59933-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="59933-120">Skype Empresarial (SIP)</span><span class="sxs-lookup"><span data-stu-id="59933-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="59933-121">Skype Empresarial (Web)</span><span class="sxs-lookup"><span data-stu-id="59933-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="59933-122">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="59933-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="59933-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="59933-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="59933-124">Para Exchange Online Protection, las direcciones URL varían según los nombres de inquilino; sin embargo, todos los clientes pueden probar Microsoft 365 con **microsoft-com.mail.protection.outlook.com**.</span><span class="sxs-lookup"><span data-stu-id="59933-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Microsoft 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>
