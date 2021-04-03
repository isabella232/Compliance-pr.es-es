---
title: RGPD para Skype Empresarial Server
description: Obtenga información sobre cómo cumplir los requisitos de RGPD en Skype Empresarial Server local y Lync Server.
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
hideEdit: true
ms.openlocfilehash: f0c59e0b4fb6fd80fd13521a3ed4996e787474bc
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496012"
---
# <a name="gdpr-for-skype-for-business-server-and-lync-server"></a>RGPD para Skype Empresarial Server y Lync Server

La mayoría de los datos de Skype Empresarial Server y Lync Server se almacenan en Exchange Server. Esto incluye:

-   El historial de conversaciones

-   Las transcripciones y las notificaciones de correo de voz

-   Las invitaciones a reuniones

Use los procedimientos descritos para [RGPD para Exchange Server](gdpr-for-exchange-server.md) para buscar, exportar o eliminar estos tipos de datos para las solicitudes de RGPD.

Las listas de contactos se almacenan en la base de datos de SQL Server. Se pueden exportar de las siguientes maneras:

-   Los propios usuarios finales pueden exportar los contactos haciendo clic con el botón derecho en el encabezado de grupo y seleccionando Copiar. Esto copiará todos los contactos de ese grupo en el portapapeles, que después pueden pegarse en cualquier aplicación.

-   Puede usar el cmdlet [Export-CsUserData](/powershell/module/skype/export-csuserdata) para exportar los datos.

El contenido cargado en reuniones (como documentos o archivos de PowerPoint) o el que se genera en una reunión (como la pizarra, los sondeos y las preguntas y respuestas) se almacena en el archivador. También puede exportarse si los usuarios finales inician sesión en una reunión que no ha caducado y descargan el contenido cargado o realizan capturas de pantalla en el caso del contenido generado.

Las reuniones MeetNow que no están en el calendario de Exchange, la lista de contactos y los derechos de contactos (familia, compañeros de trabajo, etc.) están en la base de datos de usuario. En Lync Server 2013 y versiones posteriores, puede usar el cmdlet [Export-CsUserData](/powershell/module/skype/export-csuserdata) para exportar los datos.
