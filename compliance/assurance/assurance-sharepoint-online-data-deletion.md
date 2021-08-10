---
title: Microsoft 365 SharePoint eliminación de datos en línea
description: Obtenga información sobre cómo funciona la eliminación de datos en SharePoint Online, como dónde se almacena el contenido eliminado y durante cuánto tiempo.
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
- SPO_Content
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 5a507dcd68aeda46ccf744e31828559aa6102a4f0fc50987f97041c6da8ab56f
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292048"
---
# <a name="sharepoint-online-data-deletion-in-microsoft-365"></a>SharePoint Eliminación de datos en línea en Microsoft 365

SharePoint Online almacena objetos como código abstracto en bases de datos de aplicaciones. Cuando un usuario carga un archivo en SharePoint Online, ese archivo se desensambla y se traduce en código de aplicación y se almacena en varias tablas en varias bases de datos. En SharePoint Online, todo el contenido que carga un cliente se divide en fragmentos, cifrado (potencialmente con varias claves de AES de 256 bits) y distribuido en todo el centro de datos. Para obtener detalles específicos sobre el proceso de fragmentación y cifrado, vea [Encryption in the Microsoft Cloud](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview). 

En SharePoint Online, los elementos se conservan durante 93 días desde el momento en que los elimina de su ubicación original. Permanecen en la Papelera de reciclaje del sitio todo el tiempo, a menos que alguien la elimine de allí o la vacíe. En ese caso, los elementos van a la papelera de reciclaje de la colección de sitios, donde permanecen durante el resto de los 93 días. Para obtener información sobre cómo restaurar elementos eliminados, consulta Restaurar elementos en la papelera de reciclaje de un sitio [SharePoint](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) y Restaurar elementos eliminados de la papelera de reciclaje de [la colección de sitios](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b). El tiempo de retención de la Papelera de reciclaje no se puede configurar en SharePoint Online.

Al eliminar una colección de sitios, también se elimina la jerarquía de sitios de la colección y todo el contenido dentro de ellos:

- Documentos y bibliotecas de documentos
- Listas y datos de lista
- Configuración del sitio
- Información de seguridad y roles relacionada con el sitio o sus subsitios
- Subsitios del sitio web de nivel superior, su contenido e información de usuario

Si elimina accidentalmente una colección de sitios, puede restaurarla un administrador global o SharePoint mediante el centro SharePoint administración.

Las colecciones de sitios eliminadas se conservan durante 93 días. Después de 93 días, los sitios y todo su contenido y configuración se eliminan de forma permanente, incluidas las listas, las bibliotecas, las páginas y los subsitios.

La eliminación permanente se produce cuando un usuario purga elementos eliminados de la Papelera de reciclaje de la colección de sitios, cuando expiran los períodos de retención y copia de seguridad, o cuando un administrador elimina permanentemente una colección de sitios mediante el [cmdlet Remove-SPODeletedSite](/powershell/module/sharepoint-online/remove-spodeletedsite). Cuando un usuario elimina (elimina o purga permanentemente) contenido de SharePoint Online, también se eliminan todas las claves de cifrado de los fragmentos eliminados. Los bloques de los discos que almacenaban previamente los fragmentos eliminados se marcan como no usados y están disponibles para su nuevo uso.
