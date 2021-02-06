---
title: Cifrado para datos en tránsito
description: En este artículo, busque una breve explicación de cómo Microsoft cifra los datos de clientes de Microsoft 365 en tránsito.
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: b6d6ae53ef2ade842e0e9205c01b44fe17891a97
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120539"
---
# <a name="encryption-for-data-in-transit"></a>Cifrado para datos en tránsito

Además de proteger los datos de los clientes en reposo, Microsoft usa tecnologías de cifrado para proteger los datos de los clientes en tránsito. Los datos están en tránsito:

- cuando un equipo cliente se comunica con un servidor de Microsoft;
- cuando un servidor de Microsoft se comunica con otro servidor de Microsoft; y
- cuando un servidor de Microsoft se comunica con un servidor que no es de Microsoft (por ejemplo, Exchange Online entrega correo electrónico a un servidor de correo electrónico de terceros).

Las comunicaciones entre centros de datos entre servidores de Microsoft tienen lugar a través de TLS o IPsec, y todos los servidores orientados al cliente negocian una sesión segura mediante TLS con equipos cliente (por ejemplo, Exchange Online usa TLS 1.2 con la intensidad de cifrado de 256 bits se usa (se valida fips 140-2 nivel 2). (Vea [los detalles de referencia técnica sobre el cifrado](/microsoft-365/compliance/technical-reference-details-about-encryption) para obtener una lista de conjuntos de cifrado TLS compatibles con Office 365). Esto se aplica a los protocolos que usan clientes como Outlook, Skype Empresarial, Microsoft Teams y Outlook en la Web (por ejemplo, HTTP, POP3, etc.).

Microsoft IT SSL emite los certificados públicos mediante SSLAdmin, una herramienta interna de Microsoft para proteger la confidencialidad de la información transmitida. Todos los certificados emitidos por MICROSOFT IT tienen una longitud mínima de 2048 bits, y el cumplimiento de webtrust requiere SSLAdmin para asegurarse de que los certificados se emiten solo a las direcciones IP públicas que son propiedad de Microsoft. Las direcciones IP que no cumplan este criterio se enrutan a través de un proceso de excepción.

Todos los detalles de implementación, como la versión de TLS que se usa, si está habilitado el secreto de reenvío (FS), el orden de los conjuntos de cifrado, etc., están disponibles públicamente. Una forma de ver estos detalles es usar un sitio web de terceros, como [Qualys SSL Labs](https://www.ssllabs.com). A continuación se muestran los vínculos a páginas de prueba automatizadas de Qualys que muestran información para los siguientes servicios:

- [Office 365 Portal](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype Empresarial (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype Empresarial (Web)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Exchange Online Protection](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Para Exchange Online Protection, las direcciones URL varían según los nombres de inquilino; sin embargo, todos los clientes pueden probar Microsoft 365 con **microsoft-com.mail.protection.outlook.com**.
