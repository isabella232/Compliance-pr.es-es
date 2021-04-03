---
title: RGPD para Project Server
description: Aprenda a cumplir con los requisitos de la Normativa general de protección de datos (GDPR) en un Servidor de proyectos in situ.
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
ms.custom: seo-marvel-apr2020
ms.collection: MS-Compliance
hideEdit: true
ms.openlocfilehash: ddbf22523caf1869d0253599216fff07ee14f751
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "51495949"
---
# <a name="gdpr-for-project-server"></a>RGPD para Project Server

Project Server usa scripts personalizados para exportar y redactar datos de usuario en Project Web App. El proceso básico es:

1.  Busque los sitios de Project Web App en la granja de servidores.

2.  Busque los proyectos en cada sitio que contiene el usuario.

3.  Exporte y revise los tipos de datos que desee revisar.

4.  Redacte los datos según sea necesario.

Estos pasos se tratan con detalle en los siguientes artículos:

- [Exportar datos de usuario de Project Server](/Project/export-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)

- [Eliminar datos de usuario de Project Server](/Project/delete-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)


Tenga en cuenta que Project Server se basa en SharePoint Server y registra los eventos en los registros de ULS de SharePoint y la base de datos de uso. Para obtener más información, vea [RGPD para SharePoint Server](gdpr-for-sharepoint-server.md).
