---
title: Seguridad de red
description: Obtenga información sobre la seguridad de red en Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: c063460fdfba44265b3a1504a049a4772b484dff
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507762"
---
# <a name="network-security-overview"></a>Introducción a la seguridad de red

## <a name="how-does-microsoft-365-secure-the-network-boundary"></a>¿Cómo protege Microsoft 365 el límite de red?

Microsoft 365 emplea varias estrategias para proteger su límite de red, lo que incluye la detección automatizada y la prevención de ataques basados en red, los dispositivos de Firewall especializados y la protección en línea de Exchange (EOP) para la protección contra correo no deseado y antimalware. Además, Microsoft 365 separa su entorno de producción en segmentos de red aislados lógicamente, en los que solo se permite la comunicación necesaria entre segmentos. El tráfico de red se protege mediante firewalls de red adicionales en puntos límite para ayudar a detectar, prevenir y mitigar los ataques de red.

## <a name="how-does-microsoft-365-defend-against-ddos-attacks"></a>¿Cómo defiende Microsoft 365 contra los ataques DDoS?

La gran presencia en Internet de Microsoft aísla a los efectos negativos de muchos ataques de denegación de servicio (DDoS) distribuidos. Las instancias distribuidas de cada servicio de Microsoft 365 y varias rutas a cada servicio limitan el impacto de los ataques DDoS en el sistema. Esta redundancia mejora la capacidad de Microsoft 365 de absorber ataques DDoS y aumenta la cantidad de tiempo disponible para detectar y mitigar los ataques DDoS antes de que afecten a la disponibilidad del servicio.

Además de la arquitectura de sistema redundante de Microsoft, Microsoft usa herramientas sofisticadas de detección y mitigación para responder a ataques DDoS. Los servidores de seguridad de propósito especial supervisan y eliminan el tráfico no deseado antes de que crucen el límite en la red, lo que reduce el estrés en sistemas ubicados dentro de los límites de la red. Para proteger aún más nuestros servicios en la nube, Microsoft usa un sistema de defensa DDoS implementado como parte de Microsoft Azure. El sistema de defensa DDoS de Azure está diseñado para resistir ataques desde el exterior y desde otros inquilinos de Azure.

## <a name="how-does-microsoft-365-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>¿Cómo protege Microsoft 365 a los usuarios contra el correo no deseado y el malware que se cargan o envían a través de servicios en línea?

Microsoft 365 genera protección antimalware en servicios que pueden ser vectores para código malintencionado, como Exchange Online y SharePoint Online. Exchange Online Protection (EOP) analiza todos los correos electrónicos y los archivos adjuntos de correo electrónico en busca de malware mientras entran y salen del sistema, evitando que se entreguen los mensajes y los datos adjuntos infectados. El filtrado avanzado de correo no deseado se aplica automáticamente a los mensajes entrantes y salientes para ayudar a evitar que las organizaciones del cliente reciban y envíen correo no deseado. Este nivel de protección protege contra los ataques que aprovechan el correo no deseado o no solicitado, como los ataques de suplantación de identidad (phishing). SharePoint Online usa el mismo motor de detección de virus para analizar selectivamente los archivos cargados para detectar malware. Si un archivo se marca como infectado, se impide que los usuarios descarguen o sincronicen el archivo para proteger los extremos de cliente.

## <a name="related-external-regulations--certifications"></a>Certificaciones & de las reglamentaciones externas relacionadas

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y las certificaciones externas. Consulte la tabla siguiente para validar los controles relacionados con la seguridad de la red.

| **Auditorías externas** | **Section** | **Fecha del informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-5: protección contra denegación de servicio <br> SC-7: protección de límites <br> SI-2: corrección de errores <br> SI-3: protección contra código malintencionado <br> SI-8: protección contra correo no deseado | 24 de septiembre de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-27: Análisis de vulnerabilidad | 30 de septiembre de 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-27: Análisis de vulnerabilidad <br> CA-45: anti-malware | 30 de septiembre de 2019 |