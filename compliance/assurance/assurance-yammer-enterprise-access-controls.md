---
title: Controles de acceso empresarial de Microsoft 365 Yammer
description: Este artículo contiene un breve resumen sobre los controles de acceso de Yammer Enterprise en el entorno de producción.
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
ms.openlocfilehash: 916f26d5f2defdfb21cb9babe3a64cf618e8cd4a
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120369"
---
# <a name="yammer-enterprise-access-controls"></a>Controles de acceso empresarial de Yammer 

El acceso físico y lógico al entorno de producción de Yammer está restringido a un pequeño conjunto de personas (infraestructura y operaciones). Al igual que otros ingenieros de Microsoft 365, los ingenieros de Yammer no tienen acceso permanente a los datos de los clientes. El acceso debe solicitarse mediante un sistema de control de acceso just-in-time basado en aprobación similar a la Caja de seguridad con un número limitado de aprobadores. Los aprobadores comprueban la solicitud (por ejemplo, comprueban si la solicitud es legítima en función de la necesidad, caso empresarial, tiempo, etc.) y, a continuación, aprueban o deniegan la solicitud. Si se aprueba la solicitud, el acceso a JIT se concede durante un tiempo definido y limitado. Una vez superado el tiempo de acceso, el acceso expira automáticamente.

Al igual que con otros servicios de Microsoft 365, todo el acceso al entorno de producción de Yammer usa la autenticación multifactor. Todo el historial de acceso y comandos se atribuye a un usuario y el equipo de seguridad de Yammer lo registra y revisa periódicamente.

Para obtener más información acerca de la administración y administración de Yammer, vea [la ayuda de administración de Yammer.](/yammer/yammer-landing-page)