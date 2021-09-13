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
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: dc53f42c6aa7ce16e1291538bfad6d63c5a1689d
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160081"
---
# <a name="encryption-and-key-management-overview"></a>Información general sobre el cifrado y la administración de claves

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>¿Qué rol desempeña el cifrado en la protección del contenido del cliente?

La mayoría de los servicios en la nube empresarial de Microsoft son multiinquilino, lo que significa que el contenido del cliente puede almacenarse en el mismo hardware físico que otros clientes. Para proteger la confidencialidad del contenido de los clientes, los servicios en línea de Microsoft cifran todos los datos en reposo y en tránsito con algunos de los protocolos de cifrado más seguros y seguros disponibles.

El cifrado no sustituye a los controles de acceso seguro. La directiva de control de acceso de Microsoft de Acceso permanente cero (ZSA) protege el contenido del cliente del acceso no autorizado por parte de los empleados de Microsoft. El cifrado complementa el control de acceso protegiendo la confidencialidad del contenido del cliente dondequiera que esté almacenado y evitando que el contenido se lea mientras está en tránsito entre los sistemas de servicios en línea de Microsoft o entre los servicios en línea de Microsoft y el cliente.

## <a name="how-do-microsoft-online-services-encrypt-data-at-rest"></a>¿Cómo cifran los servicios en línea de Microsoft los datos en reposo?

Todo el contenido de los clientes de los servicios en línea de Microsoft está protegido por una o más formas de cifrado. Los servidores de Microsoft usan BitLocker para cifrar las unidades de disco que contienen contenido del cliente en el nivel de volumen. El cifrado proporcionado por BitLocker protege el contenido del cliente si hay lapsos en otros procesos o controles (por ejemplo, control de acceso o reciclaje de hardware) que podrían provocar acceso físico no autorizado a discos que contienen contenido del cliente.

Además del cifrado a nivel de volumen, los servicios en línea de Microsoft usan cifrado de servicio en la capa de aplicación para cifrar el contenido del cliente. El cifrado de servicio proporciona características de administración y protección de derechos además de una protección de cifrado segura. También permite la separación entre los Windows operativos y los datos del cliente almacenados o procesados por dichos sistemas operativos.

## <a name="how-do-microsoft-online-services-encrypt-data-in-transit"></a>¿Cómo cifran los servicios en línea de Microsoft los datos en tránsito?

Los servicios en línea de Microsoft usan protocolos de transporte sólidos, como TLS, para evitar que las partes no autorizadas realicen escuchas a los datos de los clientes mientras se mueven a través de una red. Algunos ejemplos de datos en tránsito incluyen mensajes de correo que están en proceso de entrega, conversaciones que tienen lugar en una reunión en línea o archivos que se replican entre centros de datos.

Para los servicios en línea de Microsoft, los datos se consideran "en tránsito" siempre que el dispositivo de un usuario se comunica con un servidor de Microsoft o cuando un servidor de Microsoft se comunica con otro servidor.

## <a name="how-do-microsoft-online-services-manage-the-keys-used-for-encryption"></a>¿Cómo administran los servicios en línea de Microsoft las claves usadas para el cifrado?

El cifrado seguro es tan seguro como las claves usadas para cifrar datos. Microsoft usa sus propios certificados de seguridad para cifrar las conexiones TLS para los datos en tránsito. Para los datos en reposo, los volúmenes protegidos con BitLocker se cifran con una clave de cifrado de volumen completo, que se cifra con una clave maestra de volumen, que a su vez está enlazada al Módulo de plataforma de confianza (TPM) del servidor. BitLocker usa algoritmos compatibles con FIPS para asegurarse de que las claves de cifrado nunca se almacenan o envían a través del cable de forma clara.

El cifrado de servicio proporciona otra capa de cifrado para los datos en reposo del cliente, lo que ofrece a los clientes dos opciones para la administración de claves de cifrado: claves administradas por Microsoft o Clave de cliente. Al usar claves administradas por Microsoft, los servicios en línea de Microsoft generan automáticamente y almacenan de forma segura las claves raíz usadas para el cifrado de servicios.

Los clientes con requisitos para controlar sus propias claves de cifrado raíz pueden usar cifrado de servicio con clave de cliente. Con la clave de cliente, los clientes pueden generar sus propias claves criptográficas mediante un módulo de servicio de hardware (HSM) local o Azure Key Vault (AKV). Las claves raíz del cliente se almacenan en AKV, donde se pueden usar como raíz de una de las cadenas de claves que cifra los datos o archivos del buzón de cliente. El código de servicio en línea de Microsoft solo puede acceder indirectamente a las claves raíz del cliente para el cifrado de datos y los empleados de Microsoft no pueden acceder directamente a las claves raíz.

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y certificaciones externas. Consulte la siguiente tabla para la validación de controles relacionados con el cifrado y la administración de claves.

### <a name="azure-and-dynamics-365"></a>Azure y Dynamics 365

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Controles criptográficos <br> A.18.1.5: Controles criptográficos | 2 de diciembre de 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Controles criptográficos <br> A.18.1.5: Controles criptográficos | 2 de diciembre de 2020 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: Cifrado de PII transmitido a través de redes públicas de transmisión de datos | 2 de diciembre de 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | DS-1: Almacenamiento seguro de claves y certificados criptográficos <br> DS-2: Los datos del cliente se cifran en tránsito <br> DS-3: Comunicación interna de componentes de Azure cifrados en tránsito <br> DS-4: controles y procedimientos criptográficos | 31 de marzo de 2021 |

### <a name="office-365"></a>Office 365

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | SC-8: confidencialidad e integridad de transmisión <br> SC-13: Uso de criptografía <br> SC-28: Protección de la información en reposo <br>  | 24 de septiembre de 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Controles criptográficos <br> A.18.1.5: Controles criptográficos | 20 de abril de 2021 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: Cifrado de PII transmitido a través de redes públicas de transmisión de datos | 20 de abril de 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44: cifrado de datos en tránsito <br> CA-54: cifrado de datos en reposo <br> CA-62: Cifrado de buzones de correo de clave de cliente <br> CA-63: Eliminación de datos de clave de cliente <br> CA-64: Clave de cliente | 24 de diciembre de 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16: Claves de cifrado del cliente <br> CUEC-17: Almacén de claves de cliente <br>  CUEC-18: Giro de clave de cliente| 24 de diciembre de 2020 |
