---
title: Información general sobre el cifrado y la administración de claves
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
hideEdit: true
ms.openlocfilehash: 5e46fdb5ddc3b1b80df0bcadf9054b9353a0dc8e
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088649"
---
# <a name="encryption-and-key-management-overview"></a>Información general sobre el cifrado y la administración de claves

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>¿Qué rol desempeña el cifrado en la protección del contenido del cliente?

La mayoría de los servicios en la nube empresarial de Microsoft son multitenant, lo que significa que el contenido del cliente puede almacenarse en el mismo hardware físico que el de otros clientes. Para proteger la confidencialidad del contenido del cliente, Microsoft 365 cifra todos los datos en reposo y en tránsito con algunos de los protocolos de cifrado más seguros y seguros disponibles.

El cifrado no sustituye a los controles de acceso seguro. Microsoft 365 de control de acceso de Zero Standing Access (ZSA) protege el contenido del cliente del acceso no autorizado por parte de los empleados de Microsoft. El cifrado complementa el control de acceso protegiendo la confidencialidad del contenido del cliente dondequiera que esté almacenado y evitando que el contenido se lea mientras está en tránsito entre sistemas Microsoft 365 o entre Microsoft 365 y el cliente.

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>¿Cómo Microsoft 365 los datos en reposo?

Todo el contenido de Microsoft 365 está protegido por una o más formas de cifrado. Los servidores de Microsoft usan BitLocker para cifrar las unidades de disco que contienen contenido del cliente en el nivel de volumen. El cifrado proporcionado por BitLocker protege el contenido del cliente en caso de fallos en otros procesos o controles (por ejemplo, control de acceso o reciclaje de hardware) que podrían provocar un acceso físico no autorizado a discos que contienen contenido del cliente.

Exchange Online, Microsoft Teams, SharePoint Online y OneDrive para la Empresa también usan cifrado de servicio en la capa de aplicación para cifrar el contenido del cliente. El cifrado de servicio proporciona características de administración y protección de derechos además de una protección de cifrado segura. También permite la separación entre los Windows operativos y los datos del cliente almacenados o procesados por dichos sistemas operativos.

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>¿Cómo Microsoft 365 cifra los datos en tránsito?

Microsoft 365 productos y servicios usan protocolos de transporte seguros, como TLS, para evitar que las partes no autorizadas realicen escuchas a datos de clientes mientras se mueve por una red. Algunos ejemplos de datos en tránsito incluyen mensajes de correo que están en proceso de entrega, conversaciones que tienen lugar en una reunión en línea o archivos que se replican entre centros de datos.

En Microsoft 365, los datos se consideran "en tránsito" cada vez que el dispositivo de un usuario se comunica con un servidor microsoft o un servidor de Microsoft se está comunicando con otro servidor. Exchange Online, SharePoint Online, Microsoft Teams y Office Online usan TLS para garantizar que los datos permanecen confidenciales mientras están en tránsito.

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>¿Cómo Microsoft 365 las claves usadas para el cifrado?

El cifrado seguro es tan seguro como las claves usadas para cifrar datos. Microsoft usa sus propios certificados de seguridad para cifrar las conexiones TLS para los datos en tránsito. Para los datos en reposo, los volúmenes protegidos con BitLocker se cifran con una clave de cifrado de volumen completo, que se cifra con una clave maestra de volumen, que a su vez está enlazada al Módulo de plataforma de confianza (TPM) del servidor. BitLocker usa algoritmos compatibles con FIPS para asegurarse de que las claves de cifrado nunca se almacenan o envían a través del cable de forma clara.

Service Encryption proporciona una capa adicional de cifrado para los datos en reposo de clientes en Exchange Online, Microsoft Teams, SharePoint Online y OneDrive para la Empresa. Cifrado de servicio ofrece a los clientes dos opciones para la administración de claves de cifrado: claves administradas por Microsoft o Clave de cliente. Al usar claves administradas por Microsoft, Microsoft 365 genera automáticamente y almacena de forma segura las claves raíz usadas para el cifrado de servicios.

Los clientes con requisitos para controlar sus propias claves de cifrado raíz pueden aprovechar el cifrado de servicio con clave de cliente. Con la clave de cliente, los clientes pueden generar sus propias claves criptográficas mediante un módulo de servicio de hardware (HSM) local o Azure Key Vault (AKV). Las claves raíz del cliente se almacenan en AKV, donde se pueden usar como raíz de una de las cadenas de claves que cifra los datos o archivos del buzón de cliente. Los empleados de Microsoft no pueden acceder directamente a las claves raíz del cliente Microsoft 365 código de servicio para el cifrado de datos.

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y certificaciones externas. Consulte la siguiente tabla para la validación de controles relacionados con el cifrado y la administración de claves.

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8: confidencialidad e integridad de transmisión <br> SC-13: Uso de criptografía <br> SC-28: Protección de la información en reposo <br>  | 24 de septiembre de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Controles criptográficos <br> A.18.1.5: Controles criptográficos | 20 de abril de 2021 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Controles criptográficos <br> A.18.1.5: Controles criptográficos | 20 de abril de 2021 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: Cifrado de PII transmitido a través de redes públicas de transmisión de datos | 20 de abril de 2021 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44: cifrado de datos en tránsito <br> CA-54: cifrado de datos en reposo <br> CA-62: Cifrado de buzones de correo de clave de cliente <br> CA-63: Eliminación de datos de clave de cliente <br> CA-64: Clave de cliente | 24 de diciembre de 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16: Claves de cifrado del cliente <br> CUEC-17: Almacén de claves de cliente <br>  CUEC-18: Giro de clave de cliente| 24 de diciembre de 2020 |
