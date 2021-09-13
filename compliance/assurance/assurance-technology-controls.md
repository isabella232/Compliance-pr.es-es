---
title: Controles de tecnología en Microsoft 365
description: En este artículo se proporciona información general sobre las herramientas y tecnologías usadas por Microsoft para el control de tecnología en Microsoft 365.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom:
- seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 06d8f500a96c84bf961dc47f6b8d259e0fffe02d
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160714"
---
# <a name="technology-controls-in-microsoft-365"></a>Controles de tecnología en Microsoft 365 

Microsoft usa varias herramientas y tecnologías para controlar, administrar y auditar el acceso a los datos de los clientes en sus servicios en línea. Se aplican a Exchange Online, SharePoint Online, Lockbox y Customer Lockbox, autenticación multifactor y mucho más. Yammer controles similares descritos en [Yammer Enterprise controles de acceso](assurance-yammer-enterprise-access-controls.md).

Microsoft 365 ingenieros no tienen acceso permanente a Microsoft 365 datos de clientes. Los ingenieros deben pasar por un proceso de aprobación de Microsoft antes de tener acceso a los datos del cliente para las operaciones de servicio. Si el cliente licencia la característica Caja de seguridad del cliente para Exchange Online y SharePoint Online, el acceso a los datos del cliente requiere la aprobación del cliente. Una vez aprobadas, las cuentas administrativas específicas del servicio se aprovisionan con acceso justo a tiempo para las tareas requeridas por la solicitud de servicio.

## <a name="lockbox-and-customer-lockbox"></a>Caja de seguridad y caja de seguridad de cliente

Aunque es poco frecuente, un cliente podría solicitar ayuda a Microsoft que exponga el contenido del cliente a un ingeniero de Microsoft. Para controlar el acceso a Exchange Online, Microsoft usa un sistema de control de acceso denominado Caja de seguridad. Antes de que cualquier ingeniero de Microsoft acceda a cualquier Exchange Online o SharePoint o datos en línea, deben enviar una solicitud de acceso mediante Lockbox. Todas las solicitudes de servicio para Exchange Online y SharePoint Online se controlan mediante el sistema de caja de seguridad. Tanto con la caja de seguridad como con la caja de seguridad del cliente, todo el acceso aprobado se puede rastrear a un usuario único, lo que hace que los ingenieros resciten su tratamiento de los datos del cliente.

> [!NOTE]
> Exchange Online incluye todos los Skype Empresarial almacenados en buzones de usuario. Skype Empresarial cobertura no incluye Skype de difusión de reuniones o contenido cargado en reuniones por los usuarios. SharePoint Online incluye OneDrive para la Empresa.

Lockbox procesa solicitudes de permisos que conceden a los ingenieros la capacidad de realizar funciones operativas y administrativas dentro del servicio. Los ingenieros envían solicitudes a través de Lockbox y un administrador de Microsoft debe aprobar la solicitud antes de que el ingeniero pueda acceder a los datos del cliente. Después de la aprobación del administrador, el ingeniero tiene acceso limitado por tiempo y ámbito limitado a los datos del cliente para trabajar en el problema del cliente.

Caja de seguridad del cliente para Microsoft 365 ayuda a cumplir las obligaciones de cumplimiento si necesita procedimientos para la autorización explícita de acceso a datos. Este es un requisito para algunos estándares de cumplimiento, como FedRAMP e HIPAA. Caja de seguridad del cliente lo inserta en el proceso de aprobación de la caja de seguridad y le proporciona la capacidad de controlar la autorización del acceso de Microsoft a su contenido de Exchange Online o SharePoint Online para operaciones de servicio.

En el caso poco frecuente cuando un ingeniero de servicio de Microsoft necesita acceso a los datos, solo se concede acceso a los datos necesarios para resolver el problema y durante un período de tiempo limitado. Si rechaza una solicitud de acceso, los ingenieros de Microsoft no tendrán acceso al contenido y no podrán completar las operaciones de servicio. Si aprueba la solicitud, los ingenieros de Microsoft tienen acceso "Just-In-Time" a su contenido a través de interfaces de administración supervisadas y restringidas.

Las acciones realizadas por el ingeniero de soporte técnico se registran con fines de auditoría y son accesibles a través de la API de actividad de administración de [Office 365](/office/office-365-management-api/get-started-with-office-365-management-apis) y el Centro de [seguridad y cumplimiento](https://protection.office.com/).

>[!NOTE]
> Caja de seguridad del cliente está [disponible Microsoft 365 E5](https://products.office.com/business/office-365-enterprise-e5-business-software) como una compra de complemento. Para obtener más información, vea Microsoft 365 Solicitudes de caja [de seguridad del cliente](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2).

## <a name="just-in-time-access"></a>Acceso cuando es necesario

Microsoft usa el principio de acceso just-in-time (JIT) para Microsoft 365 para mitigar los riesgos de manipulación de credenciales y los ataques laterales. JIT quita el acceso administrativo persistente a los servicios y reemplaza los derechos con la capacidad de elevarlos a esos roles a petición. La eliminación de derechos de acceso persistente de los administradores garantiza que las credenciales estén disponibles solo cuando sean necesarias y reduce los riesgos de robo de credenciales.

El modelo de acceso JIT requiere que los ingenieros soliciten privilegios elevados durante un período limitado para realizar tareas administrativas. Además, los ingenieros usan cuentas temporales creadas con contraseñas complejas generadas por máquina y solo conceden los roles que les permiten realizar las tareas necesarias. Por ejemplo, el acceso administrativo concedido por Lockbox está limitado por tiempo y la cantidad de tiempo que se concede depende del rol solicitado. Un ingeniero especifica la duración del acceso de tiempo necesario en la solicitud al sistema de caja de seguridad. El sistema de caja de seguridad rechaza las solicitudes cuando el tiempo solicitado supera el tiempo máximo permitido para la elevación. Después de expirar, se quita el acceso administrativo y expira la cuenta temporal.

Cuando se autoriza y aprueba el acceso, los ingenieros reciben una contraseña administrativa de uso único generada por el sistema de autorización. Cada vez que se aprueba una solicitud de acceso elevado, se generan nuevas contraseñas. La contraseña se copia en una contraseña segura, es independiente de las credenciales del ingeniero para el entorno corporativo de Microsoft y solo es buena para la sesión de acceso elevado aprobada.

## <a name="constrained-management-interfaces"></a>Interfaces de administración restringidas

Los ingenieros usan dos interfaces de administración para realizar tareas administrativas: Escritorio remoto a través de puertas de enlace de terminal service (TSG) protegidas y PowerShell remoto. Dentro de estas interfaces de administración, las directivas de software y los controles de acceso aplican restricciones significativas sobre qué aplicaciones se ejecutan y qué comandos y cmdlets están disponibles.

Microsoft 365 servidores restringen las sesiones simultáneas a una sesión por administrador de equipo por servicio, por servidor. Los TSG solo permiten una sola sesión simultánea para los usuarios y no permiten varias sesiones. Con una sola sesión por servidor, los TSG permiten Microsoft 365 administradores del equipo de servicio conectarse a varios servidores simultáneamente para que los administradores puedan realizar eficazmente sus tareas. Los administradores del equipo de servicio no tienen permisos en los propios TSG. El TSG solo se usa para aplicar la autenticación multifactor (MFA) y los requisitos de cifrado. Una vez que el administrador del equipo de servicio se conecta a un servidor específico a través de un TSG, el servidor específico aplica un límite de sesión de uno por administrador.

Las directivas de grupo de Active Directory establecen restricciones de uso y requisitos de conexión y configuración para Microsoft 365 personal. Estas directivas incluyen las siguientes características:

- Los TSG solo usan cifrado validado [fips](https://www.microsoft.com/TrustCenter/Compliance/FIPS) 140-2.
- Las sesiones de TSG se desconectan después de 30 minutos de inactividad.
- Las sesiones de TSG cierran sesión automáticamente después de 24 horas.

Las conexiones a TSG también requieren MFA mediante una tarjeta inteligente física independiente y una cuenta independiente de las credenciales corporativas de Microsoft del ingeniero. Los ingenieros se emiten diferentes tarjetas inteligentes para diversas plataformas y plataformas de administración de secretos que garantizan el almacenamiento seguro de las credenciales. Los TSG usan directivas de grupo de Active Directory para controlar quién puede iniciar sesión en servidores remotos, el número de sesiones permitidas y la configuración de tiempo de espera de inactividad. Las directivas adicionales limitan el acceso a las aplicaciones permitidas y restringen el acceso a Internet.

Además del acceso remoto mediante TSG especialmente configurados, Exchange Online permite a los usuarios con el rol Operaciones de ingeniero de servicio tener acceso a determinadas funciones administrativas en servidores de producción mediante PowerShell remoto. Para ello, el usuario debe estar autorizado para el acceso de solo lectura (depuración) al entorno Microsoft 365 producción. La escalación de privilegios está habilitada de la misma manera que se habilita para los TSG mediante el proceso de caja de seguridad.

Para el acceso remoto, cada centro de datos tiene una DIRECCIÓN IP virtual con equilibrio de carga que sirve como un único punto de acceso. Los cmdlets de PowerShell remotos disponibles se basan en el nivel de privilegios identificado en la notificación de acceso obtenida durante la autenticación. Estos cmdlets proporcionan la única funcionalidad administrativa accesible para los usuarios que se conectan con este método. PowerShell remoto limita el ámbito de los comandos disponibles para el ingeniero y se basa en el nivel de acceso concedido a través del proceso de caja de seguridad. Por ejemplo, en Exchange Online, Get-Mailbox puede estar disponible, pero Set-Mailbox no lo haría.
