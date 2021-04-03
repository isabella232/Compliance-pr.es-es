---
title: Microsoft 365 que se ocupa de la corrupción de datos
description: En este artículo se explica la corrupción de datos en Microsoft 365 y los esfuerzos realizados por Microsoft para evitar y recuperar datos.
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
ms.openlocfilehash: 9e9f0951f7e349cc70bc96bb6a2d62275848cf04
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497591"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a>Tratamiento de daños en datos en Microsoft 365

Uno de los aspectos desafiantes de la ejecución de un servicio en la nube a gran escala es cómo controlar la corrupción de datos, dado el gran volumen de datos y sistemas independientes. Los daños en los datos pueden deberse a:

- Errores de la aplicación o la infraestructura, que dañan parte o todo el estado de la aplicación
- Problemas de hardware que resultan en la pérdida de datos o la incapacidad para leer datos
- Errores operativos humanos
- Hackers malintencionados y empleados inconformes
- Incidentes en servicios externos que resultan en una pérdida de datos

Dado que una mayor resistencia en la integridad de datos significa menos incidentes de corrupción de datos, Microsoft ha integrado mecanismos de protección de Microsoft 365 para evitar que se produjesen daños, así como sistemas y procesos que nos permiten recuperar datos si lo hace. Existen comprobaciones y procesos en las distintas etapas del proceso de versión de ingeniería para aumentar la resistencia frente a daños en los datos, incluidos:

- Diseño del sistema
- Organización y estructura de código
- Revisión de código
- Pruebas unitarias, pruebas de integración y pruebas del sistema
- Pruebas/puertas de cables de viaje

Dentro de los entornos de producción de Microsoft 365, la replicación del mismo nivel entre centros de datos garantiza que siempre haya varias copias en directo de los datos. Las imágenes y scripts estándar se usan para recuperar servidores perdidos y los datos replicados se usan para restaurar los datos del cliente. Debido a los procesos y comprobaciones de resistencia de datos integrados, Microsoft solo mantiene copias de seguridad de la documentación del sistema de información de Microsoft 365 (incluida la documentación relacionada con la seguridad), mediante la replicación integrada en SharePoint Online y nuestra herramienta de repositorio de código interno, Source Depot. La documentación del sistema se almacena en SharePoint Online y Source Depot contiene imágenes del sistema y de la aplicación. SharePoint Online y Source Depot usan el control de versiones y se replican casi en tiempo real.
