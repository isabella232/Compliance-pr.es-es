---
title: Retención, eliminación y destrucción de datos en Microsoft 365
description: Una introducción a las directivas de Microsoft para Microsoft 365 con respecto a la retención, eliminación y destrucción de datos.
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: c851b235a70104720457d08c51529ee7b25c65e4
ms.sourcegitcommit: 1fd50ef5f165228109a3f2f0aef4b0c2aa59b2ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2021
ms.locfileid: "58862360"
---
# <a name="data-retention-deletion-and-destruction-in-microsoft-365"></a>Retención, eliminación y destrucción de datos en Microsoft 365

Microsoft tiene una directiva estándar de tratamiento de datos Microsoft 365 que especifica cuánto tiempo se conservan los datos del cliente después de la eliminación. Por lo general, hay dos escenarios en los que se eliminan los datos del cliente:

- **Eliminación activa:** el inquilino tiene una suscripción activa y un usuario o administrador elimina los datos o los administradores eliminan un usuario.
- **Eliminación pasiva:** finaliza la suscripción al espacio empresarial.

## <a name="data-retention"></a>Retención de datos

Para cada uno de estos escenarios de eliminación, la tabla siguiente muestra el período máximo de retención de datos, por categoría y clasificación de datos:

| Categoría de datos | Clasificación de datos | Descripción | Ejemplos | Período de retención |
|-----------------|-----------------|-----------------|----------------------------------|-------------------------------|
| Datos de cliente | Contenido del cliente| Contenido proporcionado o creado directamente por administradores y usuarios <br><br> Incluye todo el texto, el sonido, el vídeo, los archivos de imagen y el software creado y almacenado en los centros de datos de Microsoft al usar los servicios en Microsoft 365 | Algunos ejemplos de las aplicaciones de Microsoft 365 que permiten a los usuarios crear datos son Word, Excel, PowerPoint, Outlook y OneNote <br><br> El contenido del cliente también incluye secretos de propiedad o proporcionados por el cliente (contraseñas, certificados, claves de cifrado, claves de almacenamiento) | **Escenario de eliminación activa:** como máximo 30 días <br><br> **Escenario de eliminación pasiva:** como máximo 180 días |
| Datos de cliente | Información de identificación del usuario final (EUII) | Datos que identifican o podrían usarse para identificar al usuario de un servicio de Microsoft. EUII no contiene contenido de cliente | Nombre de usuario o nombre para mostrar (DOMAIN\UserName) <br><br> Nombre principal de usuario (name@domain) <br><br>  Direcciones IP específicas del usuario | **Escenario de eliminación activa:** como máximo 180 días (solo una acción de administrador de inquilinos) <br><br> **Escenario de eliminación pasiva:** como máximo 180 días |
| Datos personales <br> (datos no incluidos en los datos del cliente) | Identificadores de seudónimos de usuario final (EUPI) | Identificador creado por Microsoft vinculado al usuario de un servicio de Microsoft. Cuando se combina con otra información, como una tabla de asignación, EUPI identifica al usuario final <br><br> EUPI no contiene información cargada o creada por el cliente | GUID de usuario, GUID o SID <br><br> IDs de sesión | **Escenario de eliminación activa:** como máximo 30 días <br><br> **Escenario de eliminación pasiva:** como máximo 180 días |

## <a name="subscription-retention"></a>Retención de suscripción

En el término de una suscripción activa, un suscriptor puede acceder, extraer o eliminar datos de clientes almacenados en Microsoft 365. Si finaliza o finaliza una suscripción de pago, Microsoft conserva los datos de clientes almacenados en Microsoft 365 en una cuenta de función limitada durante 90 días para permitir al suscriptor extraer los datos. Una vez que finaliza el período de retención de 90 días, Microsoft deshabilita la cuenta y elimina los datos del cliente. No más de 180 días después de la expiración o finalización de una suscripción a Microsoft 365, Microsoft deshabilita la cuenta y elimina todos los datos de clientes de la cuenta. Una vez transcurrido el período de retención máximo de los datos, los datos se representan comercialmente como irrecuperables.

Para una versión de prueba gratuita, tu cuenta pasa a un estado de gracia durante 30 días en la mayoría de los países y regiones. Durante este periodo de gracia, puede comprar Microsoft 365. Si decide no comprar Microsoft 365, puede cancelar la versión de prueba o permitir que el período de gracia expire y se eliminará la información de la cuenta de prueba y los datos.

## <a name="expedited-deletion"></a>Eliminación acelerada

Para cualquier suscripción, un suscriptor puede ponerse en contacto con Soporte técnico de Microsoft y solicitar el desaprovisionamiento rápido de la suscripción. En este proceso, todos los datos de usuario se eliminan tres días después de que el administrador escriba el código de bloqueo proporcionado por Microsoft. Esto incluye los datos de SharePoint Online y Exchange Online en espera o almacenados en buzones inactivos.

Para obtener más información sobre el desaprovisionamiento acelerado, vea [Cancelar la suscripción.](/microsoft-365/commerce/subscriptions/cancel-your-subscription)

## <a name="related-links"></a>Vínculos relacionados

- [Destrucción de dispositivos portadores de datos](assurance-data-bearing-device-destruction.md)
- [Inmutabilidad en Office 365](assurance-data-immutability.md)
- [Eliminación de datos en Exchange Online](assurance-exchange-online-data-deletion.md)
- [Eliminación de datos en SharePoint Online](assurance-sharepoint-online-data-deletion.md)
