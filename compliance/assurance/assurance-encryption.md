---
title: Información general sobre cifrado y administración de claves
description: Obtenga información sobre el cifrado y la administración de claves en Microsoft 365
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
ms.openlocfilehash: 96a3871657dc1e6021949ca9fc2376df382fe15b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508202"
---
# <a name="encryption-and-key-management-overview"></a>Información general sobre cifrado y administración de claves

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>¿Qué rol desempeña el cifrado en la protección del contenido de los clientes?

La mayoría de los servicios en la nube de Microsoft Business son varios inquilinos, lo que significa que el contenido del cliente se puede almacenar en el mismo hardware físico que el de otros clientes. Para proteger la confidencialidad del contenido de los clientes, Microsoft 365 cifra todos los datos en reposo y en tránsito con algunos de los protocolos de cifrado más seguros disponibles.

El cifrado no es un sustituto de los controles de acceso seguros. La Directiva de control de acceso de Microsoft 365 de acceso a cero (ZSA) protege el contenido de los clientes del acceso no autorizado por parte de los empleados de Microsoft. El cifrado complementa el control de acceso al proteger la confidencialidad del contenido del cliente en cualquier lugar en el que se almacene, evitando que se lea el contenido mientras se transmite entre los sistemas Microsoft 365 o entre Microsoft 365 y el cliente.

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>¿Cómo cifra Microsoft 365 los datos en reposo?

Todo el contenido de los clientes de Microsoft 365 está protegido por una o más formas de cifrado. Los servidores de Microsoft usan BitLocker para cifrar las unidades de disco que contienen contenido de clientes en el nivel de volumen. El cifrado proporcionado por BitLocker protege el contenido de los clientes en caso de que se produzcan fallos en otros procesos o controles (por ejemplo, el control de acceso o el reciclaje de hardware) que podría llevar a un acceso físico no autorizado a los discos que contienen contenido de clientes.

Exchange Online, Microsoft Teams, SharePoint Online y OneDrive para la empresa también usan el cifrado de servicio en el nivel de aplicación para cifrar el contenido del cliente. El cifrado de servicio ofrece características de protección y administración de derechos sobre la protección de cifrado de alta seguridad. También permite la separación entre los sistemas operativos Windows y los datos del cliente almacenados o procesados por esos sistemas operativos.

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>¿Cómo cifra Microsoft 365 los datos en tránsito?

Los productos y servicios de Microsoft 365 usan protocolos de transporte fuertes, como TLS, para evitar que partes no autorizadas intercepten datos de clientes mientras se mueven a través de una red. Algunos ejemplos de datos en tránsito son los mensajes de correo que están en proceso de entrega, las conversaciones que se realizan en una reunión en línea o los archivos que se replican entre los centros de datos.

En Microsoft 365, los datos se consideran "en tránsito" siempre que el dispositivo de un usuario se comunica con un servidor de Microsoft o un servidor de Microsoft se está comunicando con otro servidor. Exchange Online, SharePoint Online, Microsoft Teams y Office Online deben usar TLS para asegurarse de que los datos sigan siendo confidenciales mientras están en tránsito.

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>¿Cómo administra Microsoft 365 las claves usadas para el cifrado?

El cifrado seguro es tan seguro como las claves que se usan para cifrar datos. Microsoft usa sus propios certificados de seguridad para cifrar las conexiones TLS para los datos en tránsito. Para los datos en reposo, los volúmenes protegidos con BitLocker están cifrados con una clave de cifrado de volumen completo, cifrada con una clave maestra de volumen, que a su vez se enlaza al módulo de plataforma de confianza (TPM) del servidor. BitLocker usa algoritmos compatibles con FIPS para garantizar que las claves de cifrado nunca se almacenan ni se envían a través de la red sin cifrar.

El cifrado de servicio proporciona un nivel adicional de cifrado para los datos en reposo de los clientes en Exchange Online, Microsoft Teams, SharePoint Online y OneDrive para la empresa. El cifrado de servicio da a los clientes dos opciones para la administración de claves de cifrado: claves administradas por Microsoft o clave de cliente. Cuando se usan claves administradas por Microsoft, los servicios de 365 de Microsoft generan automáticamente y almacenan de forma segura las claves raíz que se usan para el cifrado del servicio.

Los clientes con requisitos para controlar sus propias claves de cifrado raíz pueden aprovechar el cifrado de servicio con la clave de cliente. Mediante el uso de la clave de cliente, los clientes pueden generar sus propias claves criptográficas mediante un módulo de servicio de hardware (HSM) local o Azure Key Vault (AKV). Las claves raíz del cliente se almacenan en AKV, donde se pueden usar como la raíz de una de las llaves que cifran los archivos o datos de buzones de correo del cliente. El código de servicio 365 de Microsoft para el cifrado de datos solo puede tener acceso directo a las claves raíz del cliente, y los empleados de Microsoft no pueden acceder a ellas.

## <a name="related-external-regulations--certifications"></a>Certificaciones & de las reglamentaciones externas relacionadas

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y las certificaciones externas. Consulte la tabla siguiente para validar los controles relacionados con el cifrado y la administración de claves.

| **Auditorías externas** | **Section** | **Fecha del informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8: confidencialidad e integridad de la transmisión <br> SC-13: uso de la criptografía <br> SC-28: protección de la información en reposo <br>  | 24 de septiembre de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 10.1: controles criptográficos <br> A. 18.1.5: controles criptográficos | 22 de febrero de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 10.1: controles criptográficos <br> A. 18.1.5: controles criptográficos | 22 de febrero de 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 11.6: cifrado de PII transmitido a través de redes públicas de transmisión de datos | 22 de febrero de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-44: cifrado de datos en tránsito <br> CA-54: cifrado de datos en reposo <br> CA-62: cifrado de buzón de clave de cliente <br> CA-63: eliminación de datos de clave de cliente <br> CA-64: clave de cliente | 30 de septiembre de 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-16: claves de cifrado del cliente <br> CUEC-17: bóveda de clave de cliente <br>  CUEC-18: rotación de clave de cliente| 30 de septiembre de 2019 |
