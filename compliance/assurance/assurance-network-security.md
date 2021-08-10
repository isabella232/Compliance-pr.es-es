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
hideEdit: true
ms.openlocfilehash: 18f5bfa40fc8827ec840a764ae3224765aadae81156738fe30a51acd6ca244ab
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292767"
---
# <a name="network-security-overview"></a>Información general sobre seguridad de red

## <a name="how-do-microsoft-online-services-secure-the-network-boundary"></a>¿Cómo protegen los servicios en línea de Microsoft el límite de red?

Los servicios en línea de Microsoft emplean varias estrategias para proteger su límite de red, incluida la detección automatizada y la prevención de ataques basados en red, dispositivos de firewall especializados y Exchange Online Protection (EOP) para la protección contra correo no deseado y antimalware. Además, los servicios en línea de Microsoft separan sus entornos de producción en segmentos de red aislados lógicamente, con solo la comunicación necesaria permitida entre segmentos. El tráfico de red está protegido mediante firewalls de red adicionales en puntos de límite para ayudar a detectar, evitar y mitigar los ataques de red.

## <a name="how-do-microsoft-online-services-defend-against-ddos-attacks"></a>¿Cómo se defienden los servicios en línea de Microsoft frente a los ataques DDoS?

La gran presencia de Internet de Microsoft la aísla de los efectos negativos de muchos ataques distribuidos de denegación de servicio (DDoS). Las instancias distribuidas de cada servicio en línea de Microsoft y varias rutas a cada servicio limitan el impacto de los ataques DDoS en el sistema. Esta redundancia mejora la capacidad de los servicios en línea de Microsoft para absorber los ataques DDoS y aumenta la cantidad de tiempo disponible para detectar y mitigar los ataques de DDoS antes de que repercutan en la disponibilidad del servicio.

Además de la arquitectura redundante del sistema de Microsoft, Microsoft usa sofisticadas herramientas de detección y mitigación para responder a los ataques DDoS. Los firewalls de uso especial supervisan y sueltan el tráfico no deseado antes de cruzar el límite a la red, lo que reduce el estrés en los sistemas ubicados dentro del límite de red. Para proteger aún más nuestros servicios en la nube, Microsoft usa un sistema de defensa de DDoS implementado como parte de Microsoft Azure. El sistema de defensa de Azure DDoS está diseñado para resistir ataques desde el exterior y desde otros inquilinos de Azure.

## <a name="how-does-microsoft-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>¿Cómo protege Microsoft a los usuarios contra el correo no deseado y el malware que se cargan o envían a través de los servicios en línea?

Los servicios en línea de Microsoft crean protección antimalware en servicios que pueden ser vectores de código malintencionado, como Exchange Online y SharePoint Online. Exchange Online Protection (EOP) examina todos los correos electrónicos y datos adjuntos de correo electrónico en busca de malware a medida que entran y salen del sistema, lo que impide que se entreguen mensajes y datos adjuntos infectados. El filtrado de correo no deseado avanzado se aplica automáticamente a los mensajes entrantes y salientes para ayudar a evitar que las organizaciones de clientes reciban y envíen correo no deseado. Esta capa de protección protege contra ataques que aprovechan el correo electrónico no solicitado o no autorizado, como los ataques de suplantación de identidad. SharePoint Online usa el mismo motor de detección de virus para examinar selectivamente los archivos cargados en busca de malware. Si un archivo está marcado como infectado, se impide a los usuarios descargar o sincronizar el archivo para proteger los extremos de cliente. De forma similar, Azure compara los hashes relacionados con los archivos cargados en Azure Storage con los hash de malware conocido. Cuando se encuentran coincidencias, se genera una alerta en el Centro de seguridad de Azure, donde se toma una decisión sobre la legitimidad de la alerta y cómo debe tratarse.

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y certificaciones externas. Consulte la tabla siguiente para la validación de controles relacionados con la seguridad de red.

### <a name="azure-and-dynamics-365"></a>Azure y Dynamics 365

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | VM-1: Registro de eventos de seguridad <br> VM-3: detección y supervisión de intrusiones <br> VM-4: investigación de eventos malintencionados <br> VM-6: Análisis de vulnerabilidades <br> VM-7: Configuración de dispositivos de red <br> VM-8: pruebas de penetración <br> VM-9: Registro de eventos de seguridad de dispositivos de red <br> VM-13: Mitigación de vulnerabilidad de dispositivo de red | 31 de marzo. 2021 |

### <a name="office-365"></a>Office 365

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | SC-5: Protección contra denegación de servicio <br> SC-7: Protección de límites <br> SI-2: Corrección de defectos <br> SI-3: Protección contra código malintencionado <br> SI-8: Protección contra correo no deseado | 24 de septiembre de 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: Análisis de vulnerabilidades | 24 de diciembre de 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: Análisis de vulnerabilidades <br> CA-45: Antimalware | 24 de diciembre de 2020 |