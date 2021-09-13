---
title: Microsoft 365 Yammer de acceso empresarial
description: Este artículo contiene un breve resumen sobre Yammer Enterprise controles de acceso en el entorno de producción.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
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
ms.openlocfilehash: 5bc064ccf982b9a67ec5cedc33e85f58e1d7dfc1
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160697"
---
# <a name="yammer-enterprise-access-controls"></a>Yammer de acceso empresarial 

El acceso físico y lógico al entorno Yammer de producción está restringido a un pequeño conjunto de personas (infraestructura y operaciones). Al igual que con otros Microsoft 365, los Yammer no tienen acceso permanente a los datos de los clientes. El acceso debe solicitarse mediante un sistema de control de acceso just-in-time basado en aprobación similar a Lockbox con un número limitado de aprobadores. Los aprobadores comprueban la solicitud (por ejemplo, comprueban si la solicitud es legítima en función de la necesidad, el caso empresarial, la hora, etc.) y, a continuación, aprueban o deniegan la solicitud. Si se aprueba la solicitud, se concede acceso a JIT por un tiempo definido y limitado. Una vez superado el tiempo de acceso, el acceso expira automáticamente.

Al igual que con otros Microsoft 365, todo el acceso al entorno de Yammer de producción usa la autenticación multifactor. Todo el acceso y el historial de comandos se atribuyó a un usuario y el equipo de seguridad Yammer revisión periódicamente.

Para obtener más información acerca Yammer administración y administración, consulte [Yammer ayuda de administración.](/yammer/yammer-landing-page)