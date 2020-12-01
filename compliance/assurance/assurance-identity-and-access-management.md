---
title: Información general de administración de identidades y acceso
description: Obtenga información sobre la administración de acceso e identidades en Microsoft 365
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
ms.openlocfilehash: b62219faa5bc55ef4bef9557d953caf1a2f95fc7
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507833"
---
# <a name="identity-and-access-management-overview"></a>Información general de administración de identidades y acceso

## <a name="how-does-microsoft-365-protect-production-systems-from-unauthorized-or-malicious-access"></a>¿Cómo protege Microsoft 365 los sistemas de producción de acceso malintencionado o no autorizado?

Microsoft 365 está diseñado para permitir a los ingenieros de Microsoft operar el servicio sin acceder al contenido del cliente. De forma predeterminada, los ingenieros de Microsoft 365 tienen un acceso de cero (ZSA) a contenido de clientes y sin privilegios de acceso al entorno de producción. Microsoft 365 usa un modelo Just-in-Time (JIT) y de acceso único (JEA) para proporcionar a los ingenieros de equipo de servicio acceso temporal a los entornos de producción cuando dicho acceso es necesario para admitir Microsoft 365. El modelo de acceso JIT reemplaza el acceso administrativo tradicional y persistente con un proceso para que los ingenieros soliciten la elevación temporal en roles privilegiados cuando sea necesario.

Los ingenieros asignados a un equipo de servicio para admitir servicios de producción solicitan la elegibilidad de una cuenta de equipo de servicio a través de la herramienta de administración de identidades (IDM). La solicitud de elegibilidad desencadena una serie de comprobaciones de personal para asegurarse de que el ingeniero ha superado todos los requisitos de detección en la nube, ha completado la formación necesaria y ha recibido la aprobación de administración adecuada antes de crear la cuenta. Solo después de cumplir todos los requisitos de elegibilidad puede crear una cuenta de equipo de servicio para el entorno solicitado.

Las cuentas de equipo de servicio no conceden ningún privilegio de administrador o acceso al contenido del cliente. Cuando un ingeniero requiere acceso adicional para admitir el servicio de Microsoft 365, solicitan un acceso elevado temporal a los recursos que necesitan con una herramienta de administración de acceso denominada Lockbox. Lockbox restringe el acceso elevado a los privilegios mínimos, los recursos y el tiempo necesarios para completar la tarea asignada. Si un revisor autorizado aprueba la solicitud de acceso JIT, al ingeniero se le concede una cuenta temporal con los privilegios necesarios para completar su trabajo asignado. Esta cuenta temporal requiere la autenticación multifactor y se elimina automáticamente después de que expire el período aprobado.

## <a name="how-does-microsoft-365-handle-remote-access-to-production-systems"></a>¿Cómo maneja Microsoft 365 el acceso remoto a los sistemas de producción?

Los componentes del sistema Microsoft 365 se alojan en centros de los centros de recursos separados geográficamente de los equipos de operaciones. El personal del centro de recursos no tiene acceso lógico a los sistemas Microsoft 365. Como resultado, el personal del equipo de servicio de 365 de Microsoft administra el entorno a través de acceso remoto. El personal del equipo de servicio que requiere acceso remoto a soporte técnico de Microsoft 365 solo se le concede acceso remoto tras la aprobación de un administrador autorizado. Todos los accesos remotos usan TLS compatible con FIPS 140-2 para conexiones remotas seguras.

Microsoft 365 usa estaciones de trabajo de administración seguras (Sierras) para el acceso remoto del equipo de servicio para ayudar a proteger los entornos de Microsoft 365 de la intromisión. Estas estaciones de trabajo están diseñadas específicamente para evitar la pérdida intencionada o no de datos de producción, como el bloqueo de puertos USB y la limitación del software disponible en la sierra a lo que se necesita para admitir el entorno. Se realiza un seguimiento y supervisión de los Sierras para detectar y evitar un riesgo malintencionado o accidental de los datos de los clientes por parte de los ingenieros de Microsoft.

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>¿Cómo agregan las protecciones del cliente protección adicional para el contenido del cliente?

Los clientes pueden agregar un nivel de control de acceso adicional a su contenido mediante la habilitación de caja de caja de clientes. Cuando una solicitud de elevación de Lockbox implica el acceso al contenido del cliente, la caja de caja del cliente requiere la aprobación del cliente como paso final en el flujo de trabajo de aprobación. Esto proporciona a las organizaciones la opción de aprobar o denegar estas solicitudes y proporciona control de acceso directo al cliente. Si el cliente rechaza una solicitud de caja de caja del cliente, se deniega el acceso al contenido solicitado. Si el cliente no rechaza ni aprueba la solicitud en un período determinado, la solicitud expirará automáticamente sin que Microsoft obtenga acceso al contenido del cliente. Si el cliente aprueba la solicitud, el acceso temporal de Microsoft al contenido del cliente se registrará, auditará y revocará automáticamente una vez que expire el tiempo asignado para completar la operación de solución de problemas.

## <a name="related-external-regulations--certifications"></a>Certificaciones & de las reglamentaciones externas relacionadas

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y las certificaciones externas. Consulte la tabla siguiente para validar los controles relacionados con el control de acceso y la identidad.

| **Auditorías externas** | **Section** | **Fecha del informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: administración de cuentas <br> AC-3: aplicación de acceso <br> AC-5: separación de tareas <br> AC-6: privilegio mínimo <br> AC-17: acceso remoto | 24 de septiembre de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 9.1: requisitos empresariales del control de acceso <br> A. 9.2: administración de acceso de usuario <br> A. 9.3: responsabilidades del usuario <br> A. 9.4: control de acceso de aplicaciones y sistema <br> A. 15.1: seguridad de la información en relaciones de proveedores | 22 de febrero de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 9.2: administración de acceso de usuario <br> A. 9.4: control de acceso de aplicaciones y sistema <br> A. 15.1: seguridad de la información en relaciones de proveedores | 22 de febrero de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-33: modificación de cuentas <br> CA-34: autenticación de usuario <br> CA-35: acceso privilegiado <br> CA-36: acceso remoto <br> CA-57: aprobación del cliente de Microsoft Management Approval <br> CA-58: solicitudes de servicio del Lockbox del cliente <br> CA-59: notificaciones de Lockbox del cliente <br> CA-61: revisión y aprobación de JIT | 30 de septiembre de 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-32: Directiva de cuenta compartida <br> CA-33: modificación de cuentas <br> CA-34: autenticación de usuario <br> CA-35: acceso privilegiado <br> CA-36: acceso remoto <br> CA-53: supervisión de terceros <br> CA-56: aprobación del cliente de caja de caja de clientes <br> CA-57: aprobación del cliente de Microsoft Management Approval <br> CA-58: solicitudes de servicio del Lockbox del cliente <br> CA-59: notificaciones de Lockbox del cliente <br> CA-61: revisión y aprobación de JIT | 30 de septiembre de 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-15: solicitudes de caja de caja de cliente | 30 de septiembre de 2019 |