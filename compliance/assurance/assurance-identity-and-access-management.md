---
title: Información general sobre la administración de acceso e identidad
description: Información sobre la administración de identidades y acceso en Microsoft 365
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
ms.openlocfilehash: d431a7f04b156b003f5f4e213aef9bb9792874fe
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497165"
---
# <a name="identity-and-access-management-overview"></a>Información general sobre la administración de acceso e identidad

## <a name="how-does-microsoft-365-protect-production-systems-from-unauthorized-or-malicious-access"></a>¿Cómo protege Microsoft 365 los sistemas de producción del acceso no autorizado o malintencionado?

Microsoft 365 está diseñado para permitir a los ingenieros de Microsoft operar el servicio sin tener acceso al contenido del cliente. De forma predeterminada, los ingenieros de Microsoft 365 tienen acceso permanente cero (ZSA) al contenido del cliente y ningún acceso con privilegios al entorno de producción. Microsoft 365 usa un modelo Just-In-Time (JIT), Just-Enough-Access (JEA) para proporcionar a los ingenieros de equipo de servicio acceso con privilegios temporales a entornos de producción cuando dicho acceso es necesario para admitir Microsoft 365. El modelo de acceso JIT reemplaza el acceso administrativo persistente tradicional por un proceso para que los ingenieros soliciten la elevación temporal a roles con privilegios cuando sea necesario.

Los ingenieros asignados a un equipo de servicio para admitir la solicitud de servicios de producción solicitan la elegibilidad para una cuenta de equipo de servicio a través de la Herramienta de administración de identidades (IDM). La solicitud de elegibilidad desencadena una serie de comprobaciones de personal para asegurarse de que el ingeniero ha pasado todos los requisitos de filtrado en la nube, completado el entrenamiento necesario y recibido la aprobación de administración adecuada antes de la creación de cuentas. Solo después de cumplir todos los requisitos de elegibilidad, se puede crear una cuenta de equipo de servicio para el entorno solicitado.

Las cuentas de equipo de servicio no conceden privilegios de administrador permanente ni acceso al contenido del cliente. Cuando un ingeniero requiere acceso adicional para admitir su servicio de Microsoft 365, solicita acceso elevado temporal a los recursos que requieren mediante una herramienta de administración de acceso denominada Lockbox. Lockbox restringe el acceso elevado a los privilegios, recursos y tiempo mínimos necesarios para completar la tarea asignada. Si un revisor autorizado aprueba la solicitud de acceso JIT, al ingeniero se le concede una cuenta temporal con solo los privilegios necesarios para completar su trabajo asignado. Esta cuenta temporal requiere autenticación multifactor y se elimina automáticamente después de que expire el período aprobado.

## <a name="how-does-microsoft-365-handle-remote-access-to-production-systems"></a>¿Cómo administra Microsoft 365 el acceso remoto a los sistemas de producción?

Los componentes del sistema de Microsoft 365 se encuentran en centros de datos separados geográficamente de los equipos de operaciones. El personal del centro de datos no tiene acceso lógico a los sistemas de Microsoft 365. Como resultado, el personal del equipo de servicio de Microsoft 365 administra el entorno a través del acceso remoto. El personal del equipo de servicio que requiere acceso remoto para admitir Microsoft 365 solo tiene acceso remoto después de la aprobación de un administrador autorizado. Todo el acceso remoto usa TLS compatible con FIPS 140-2 para conexiones remotas seguras.

Microsoft 365 usa estaciones de trabajo de administración seguras (SAWs) para el acceso remoto del equipo de servicio para ayudar a proteger los entornos de Microsoft 365 de un riesgo. Estas estaciones de trabajo están diseñadas específicamente para evitar la pérdida intencionada o involuntaria de datos de producción, incluido el bloqueo de puertos USB y la limitación del software disponible en saw a lo necesario para admitir el entorno. Los ingenieros de Microsoft rastrean y supervisan estrechamente los SAW para detectar y evitar un riesgo malintencionado o involuntario de los datos de los clientes.

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>¿Cómo agrega la caja de seguridad del cliente protección adicional para el contenido del cliente?

Los clientes pueden agregar un nivel adicional de control de acceso a su contenido habilitando la caja de seguridad del cliente. Cuando una solicitud de elevación de caja de seguridad implica el acceso al contenido del cliente, la caja de seguridad del cliente requiere la aprobación del cliente como paso final en el flujo de trabajo de aprobación. Esto ofrece a las organizaciones la opción de aprobar o denegar estas solicitudes y proporciona control de acceso directo al cliente. Si el cliente rechaza una solicitud de caja de seguridad del cliente, se denegará el acceso al contenido solicitado. Si el cliente no rechaza o aprueba la solicitud en un período determinado, la solicitud expirará automáticamente sin que Microsoft obtenga acceso al contenido del cliente. Si el cliente aprueba la solicitud, el acceso temporal de Microsoft al contenido del cliente se registrará, auditará y revocará automáticamente después de que expire el tiempo asignado para completar la operación de solución de problemas.

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y certificaciones externas. Consulte la siguiente tabla para la validación de los controles relacionados con la identidad y el control de acceso.

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: Administración de cuentas <br> AC-3: Aplicación de acceso <br> AC-5: Separación de funciones <br> AC-6: privilegios mínimos <br> AC-17: Acceso remoto | 24 de septiembre de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: Requisitos empresariales del control de acceso <br> A.9.2: Administración de acceso de usuarios <br> A.9.3: Responsabilidades del usuario <br> A.9.4: Control de acceso de sistema y aplicación <br> A.15.1: Seguridad de la información en las relaciones con proveedores | 22 de febrero de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.2: Administración de acceso de usuarios <br> A.9.4: Control de acceso de sistema y aplicación <br> A.15.1: Seguridad de la información en las relaciones con proveedores | 22 de febrero de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-33: Modificación de la cuenta <br> CA-34: Autenticación de usuario <br> CA-35: acceso con privilegios <br> CA-36: Acceso remoto <br> CA-57: Aprobación de la administración de Microsoft del cuadro de bloqueo de clientes <br> CA-58: Solicitudes de servicio de caja de seguridad del cliente <br> CA-59: Notificaciones de caja de seguridad del cliente <br> CA-61: Revisión y aprobación de JIT | 24 de diciembre de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-32: Directiva de cuenta compartida <br> CA-33: Modificación de la cuenta <br> CA-34: Autenticación de usuario <br> CA-35: acceso con privilegios <br> CA-36: Acceso remoto <br> CA-53: Supervisión de terceros <br> CA-56: aprobación del cliente de caja de seguridad del cliente <br> CA-57: Aprobación de la administración de Microsoft del cuadro de bloqueo de clientes <br> CA-58: Solicitudes de servicio de caja de seguridad del cliente <br> CA-59: Notificaciones de caja de seguridad del cliente <br> CA-61: Revisión y aprobación de JIT | 24 de diciembre de 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-15: Solicitudes de caja de seguridad del cliente | 24 de diciembre de 2020 |