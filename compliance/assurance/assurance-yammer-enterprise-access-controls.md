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
# <a name="yammer-enterprise-access-controls"></a>Controles de acceso empresarial de Yammer 

El acceso físico y lógico al entorno de producción de Yammer está restringido a un pequeño conjunto de personas (infraestructura y operaciones). Al igual que con otros ingenieros de Microsoft 365, los ingenieros de Yammer no tienen acceso permanente a los datos de los clientes. El acceso debe solicitarse mediante un sistema de control de acceso just-in-time basado en aprobación similar a Lockbox con un número limitado de aprobadores. Los aprobadores comprueban la solicitud (por ejemplo, comprueban si la solicitud es legítima en función de la necesidad, el caso empresarial, la hora, etc.) y, a continuación, aprueban o deniegan la solicitud. Si se aprueba la solicitud, se concede acceso a JIT por un tiempo definido y limitado. Una vez superado el tiempo de acceso, el acceso expira automáticamente.

Al igual que con otros servicios de Microsoft 365, todo el acceso al entorno de producción de Yammer usa autenticación multifactor. Todo el acceso y el historial de comandos se atribuyó a un usuario y el equipo de seguridad de Yammer lo registra y revisa periódicamente.

Para obtener más información acerca de la administración y administración de Yammer, consulte [Ayuda de administración de Yammer](/yammer/yammer-landing-page).