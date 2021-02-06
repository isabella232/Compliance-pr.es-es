---
title: Límites de recursos de Microsoft 365
description: En este artículo, encontrará información sobre los límites de recursos para las distintas aplicaciones de Microsoft 365.
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
ms.openlocfilehash: 632a0b78c5c5ba02a59f8863c2e751f009cc968e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120759"
---
# <a name="service-resource-limits"></a>Límites de recursos del servicio

Los límites de recursos se aplican mediante cuotas (límites) y limitación. Azure Active Directory (Azure AD) y los servicios individuales de Microsoft 365 usan ambos. Los límites son específicos del servicio y cambian con el tiempo a medida que se agregan nuevas funcionalidades. Para obtener más información sobre los límites actuales de los distintos servicios, consulte los siguientes temas:

- [Restricciones y límites de servicio de Azure AD](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [Límites de Exchange Online](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [Límites y límites del software de SharePoint Online](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Límites de Skype Empresarial](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [API de REST de Yammer y límites de velocidad](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Límites de tamaño de archivo en Sway](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

Además de estos límites, se usan varios mecanismos de limitación en Azure AD y Microsoft 365. La limitación dentro del servicio es especialmente importante, dado que los recursos de red de los centros de datos de Microsoft están optimizados para el amplio conjunto de clientes que usan los servicios. Entre los mecanismos de limitación se incluyen:

- Azure AD y Microsoft 365 ofrecen limitación de nivel de usuario, que limita el número de transacciones o llamadas simultáneas (por script o código) que puede realizar un solo usuario.
- Se asigna una directiva de limitación de PowerShell predeterminada a cada inquilino durante la creación del espacio empresarial. Esta configuración afecta a otros elementos, como el número máximo de sesiones simultáneas de PowerShell que puede abrir un único administrador.
- Cada cliente de Exchange Online tiene una directiva predeterminada de Servicios Web Exchange (EWS) que está ajustada para las operaciones del cliente EWS y la limitación que se aplica a todos los clientes de Outlook.
