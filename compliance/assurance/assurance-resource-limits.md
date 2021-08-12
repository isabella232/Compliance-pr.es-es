---
title: Microsoft 365 Límites de recursos
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
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 2f64b1201077e25d28d99f49b573912078e4e428ccb51011e17934b1440f75ac
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "54290548"
---
# <a name="service-resource-limits"></a>Límites de recursos del servicio

Los límites de recursos se aplican mediante cuotas (límites) y limitación. Azure Active Directory (Azure AD) y los servicios de Microsoft 365 individuales usan ambos. Los límites son específicos del servicio y cambian con el tiempo a medida que se agregan nuevas funcionalidades. Para obtener información detallada sobre los límites actuales de los distintos servicios, consulte los siguientes temas:

- [Restricciones y límites de servicio de Azure AD](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [Límites de Exchange Online](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [SharePoint Límites y límites de software en línea](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Skype Empresarial Límites](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [Yammer Límites de velocidad y API de REST](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Límites de tamaño de archivo en Sway](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

Además de estos límites, se usan varios mecanismos de limitación en Azure AD y Microsoft 365. La limitación dentro del servicio es especialmente importante, dado que los recursos de red en los centros de datos de Microsoft están optimizados para el amplio conjunto de clientes que usan los servicios. Los mecanismos de limitación incluyen:

- Azure AD y Microsoft 365 limitación de nivel de usuario, que limitan el número de transacciones o llamadas simultáneas (por script o código) que puede realizar un solo usuario.
- Se asigna una directiva de limitación de PowerShell predeterminada a cada inquilino en la creación del espacio empresarial. Esta configuración afecta a otros elementos, como el número máximo de sesiones simultáneas de PowerShell que puede abrir un solo administrador.
- Cada cliente Exchange Online tiene una directiva predeterminada de Exchange Web Services (EWS) que se afina para las operaciones de cliente EWS y la limitación que se aplica a todos los Outlook cliente.
