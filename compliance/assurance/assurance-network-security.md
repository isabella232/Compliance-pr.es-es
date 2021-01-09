---
title: Seguridad de red
description: Más información sobre la seguridad de red en Microsoft 365
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
ms.openlocfilehash: e246cc3c84a17fe697baea29eda285599832b0fa
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787438"
---
# <a name="network-security-overview"></a>Información general sobre seguridad de red

## <a name="how-does-microsoft-365-secure-the-network-boundary"></a>¿Cómo protege Microsoft 365 el límite de red?

Microsoft 365 emplea varias estrategias para proteger sus límites de red, incluida la detección y prevención automatizadas de ataques basados en red, dispositivos de firewall especializados y Exchange Online Protection (EOP) para la protección contra correo electrónico no deseado y antimalware. Además, Microsoft 365 separa su entorno de producción en segmentos de red aislados lógicamente, con la comunicación necesaria permitida entre segmentos. El tráfico de red se protege mediante firewalls de red adicionales en puntos de límite para ayudar a detectar, evitar y mitigar los ataques de red.

## <a name="how-does-microsoft-365-defend-against-ddos-attacks"></a>¿Cómo se defenderá Microsoft 365 contra los ataques DDoS?

La gran presencia en Internet de Microsoft la aísla de los efectos negativos de muchos ataques distribuidos por denegación de servicio (DDoS). Las instancias distribuidas de cada servicio de Microsoft 365 y varias rutas a cada servicio limitan el impacto de los ataques DDoS en el sistema. Esta redundancia mejora la capacidad de Microsoft 365 para absorber los ataques DDoS y aumenta la cantidad de tiempo disponible para detectar y mitigar los ataques DDoS antes de que repercutan en la disponibilidad del servicio.

Además de la arquitectura redundante del sistema de Microsoft, Microsoft usa herramientas sofisticadas de detección y mitigación para responder a ataques DDoS. Los firewalls de uso especial supervisan y sueltan el tráfico no deseado antes de atravesar el límite de la red, lo que reduce el esfuerzo en los sistemas ubicados dentro del límite de la red. Para proteger aún más nuestros servicios en la nube, Microsoft usa un sistema de defensa de DDoS implementado como parte de Microsoft Azure. El sistema de defensa de DDoS de Azure está diseñado para soportar ataques desde el exterior, así como desde otros inquilinos de Azure.

## <a name="how-does-microsoft-365-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>¿Cómo protege Microsoft 365 a los usuarios contra correo no deseado y malware que se cargan o envían a través de servicios en línea?

Microsoft 365 crea protección antimalware en servicios que pueden ser vectores de código malintencionado, como Exchange Online y SharePoint Online. Exchange Online Protection (EOP) examina todos los correos electrónicos y datos adjuntos de correo electrónico en busca de malware al entrar y salir del sistema, evitando que se entreguen mensajes y datos adjuntos infectados. El filtrado avanzado de correo no deseado se aplica automáticamente a los mensajes entrantes y salientes para ayudar a evitar que las organizaciones de clientes reciban y envíen correo no deseado. Esta capa de protección protege contra ataques que aprovechan el correo electrónico no solicitado o no autorizado, como los ataques de suplantación de identidad. SharePoint Online usa el mismo motor de detección de virus para examinar selectivamente los archivos cargados en busca de malware. Si un archivo está marcado como infectado, se impide que los usuarios descarguen o sincronicen el archivo para proteger los extremos del cliente.

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las certificaciones y normativas externas. Consulte la tabla siguiente para validar los controles relacionados con la seguridad de la red.

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-5: protección por denegación de servicio <br> SC-7: Protección de límites <br> SI-2: Corrección de defectos <br> SI-3: Protección contra código malintencionado <br> SI-8: Protección contra correo no deseado | 24 de septiembre de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: Análisis de vulnerabilidades | 24 de diciembre de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: Análisis de vulnerabilidades <br> CA-45: Antimalware | 24 de diciembre de 2020 |