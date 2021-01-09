---
title: Información general sobre el cifrado y la administración de claves
description: Más información sobre el cifrado y la administración de claves en Microsoft 365
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
ms.openlocfilehash: ca13c5dfb229acd46ef0dd027b537afc2ac20b5a
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787349"
---
# <a name="encryption-and-key-management-overview"></a>Información general sobre el cifrado y la administración de claves

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>¿Qué papel desempeña el cifrado en la protección del contenido de los clientes?

La mayoría de los servicios empresariales en la nube de Microsoft son multiusos, lo que significa que el contenido del cliente puede almacenarse en el mismo hardware físico que el de otros clientes. Para proteger la confidencialidad del contenido de los clientes, Microsoft 365 cifra todos los datos en reposo y en tránsito con algunos de los protocolos de cifrado más seguros y seguros disponibles.

El cifrado no sustituye a los controles de acceso sólidos. La directiva de control de acceso de Acceso cero (ZSA) de Microsoft 365 protege el contenido de los clientes contra el acceso no autorizado por parte de los empleados de Microsoft. El cifrado complementa el control de acceso protegiendo la confidencialidad del contenido del cliente donde se almacena y evitando que el contenido se lea mientras está en tránsito entre los sistemas de Microsoft 365 o entre Microsoft 365 y el cliente.

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>¿Cómo cifra Microsoft 365 los datos en reposo?

Todo el contenido de los clientes de Microsoft 365 está protegido por una o varias formas de cifrado. Los servidores de Microsoft usan BitLocker para cifrar las unidades de disco que contienen contenido del cliente en el nivel de volumen. El cifrado proporcionado por BitLocker protege el contenido del cliente en caso de fallos en otros procesos o controles (por ejemplo, control de acceso o reciclaje de hardware) que podrían dar lugar al acceso físico no autorizado a discos que contienen contenido del cliente.

Exchange Online, Microsoft Teams, SharePoint Online y OneDrive para la Empresa también usan el cifrado de servicio en el nivel de aplicación para cifrar el contenido del cliente. El cifrado de servicios proporciona características de administración y protección de derechos además de una protección de cifrado segura. También permite la separación entre los sistemas operativos Windows y los datos de clientes almacenados o procesados por dichos sistemas operativos.

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>¿Cómo cifra Microsoft 365 los datos en tránsito?

Los productos y servicios de Microsoft 365 usan protocolos de transporte seguros, como TLS, para evitar que partes no autorizadas interceptan datos de clientes mientras se mueve a través de una red. Algunos ejemplos de datos en tránsito son los mensajes de correo que se están entregando, las conversaciones que tienen lugar en una reunión en línea o los archivos que se replican entre centros de datos.

En Microsoft 365, los datos se consideran "en tránsito" siempre que el dispositivo de un usuario se comunica con un servidor de Microsoft o cuando un servidor de Microsoft se comunica con otro servidor. Exchange Online, SharePoint Online, Microsoft Teams y Office Online usan TLS para garantizar que los datos permanecen confidenciales mientras están en tránsito.

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>¿Cómo administra Microsoft 365 las claves usadas para el cifrado?

El cifrado seguro solo es tan seguro como las claves usadas para cifrar datos. Microsoft usa sus propios certificados de seguridad para cifrar las conexiones TLS para los datos en tránsito. Para los datos en reposo, los volúmenes protegidos con BitLocker se cifran con una clave de cifrado de volumen completo, que se cifra con una clave maestra de volumen, que a su vez está enlazada al Módulo de plataforma segura (TPM) en el servidor. BitLocker usa algoritmos compatibles con FIPS para garantizar que las claves de cifrado nunca se almacenan ni se envían a través de la conexión de forma clara.

El cifrado de servicio proporciona una capa adicional de cifrado para los datos en reposo de los clientes en Exchange Online, Microsoft Teams, SharePoint Online y OneDrive para la Empresa. Cifrado de servicio ofrece a los clientes dos opciones para la administración de claves de cifrado: claves administradas por Microsoft o clave de cliente. Al usar claves administradas por Microsoft, los servicios de Microsoft 365 generan automáticamente y almacenan de forma segura las claves raíz que se usan para el cifrado de servicios.

Los clientes con requisitos para controlar sus propias claves de cifrado raíz pueden aprovechar el cifrado de servicio con clave de cliente. Con la clave de cliente, los clientes pueden generar sus propias claves criptográficas mediante un módulo de servicio de hardware ( MODULE) local o Azure Key Vault (AKV). Las claves raíz del cliente se almacenan en AKV, donde se pueden usar como raíz de una de las cadenas de claves que cifran los archivos o los datos del buzón del cliente. El código de servicio de Microsoft 365 solo puede acceder indirectamente a las claves raíz del cliente para el cifrado de datos y no pueden acceder directamente los empleados de Microsoft.

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las certificaciones y normativas externas. Consulte la tabla siguiente para validar los controles relacionados con el cifrado y la administración de claves.

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8: confidencialidad e integridad de la transmisión <br> SC-13: Uso de criptografía <br> SC-28: Protección de la información en reposo <br>  | 24 de septiembre de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Controles criptográficos <br> A.18.1.5: Controles criptográficos | 22 de febrero de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Controles criptográficos <br> A.18.1.5: Controles criptográficos | 22 de febrero de 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: Cifrado de PII transmitido a través de redes públicas de transmisión de datos | 22 de febrero de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44: Cifrado de datos en tránsito <br> CA-54: Cifrado de datos en reposo <br> CA-62: Cifrado de buzón de correo de clave de cliente <br> CA-63: Eliminación de datos de clave de cliente <br> CA-64: Clave de cliente | 24 de diciembre de 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16: Claves de cifrado de cliente <br> CUEC-17: Almacén de claves de cliente <br>  CUEC-18: Rotación de claves del cliente| 24 de diciembre de 2020 |
