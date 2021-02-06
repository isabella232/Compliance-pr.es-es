---
title: 'Controles de tecnología en Microsoft 365 '
description: En este artículo se proporciona información general sobre las herramientas y tecnologías usadas por Microsoft para el control de tecnología en Microsoft 365.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
f1.keywords:
- NOCSH
ms.custom:
- seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 2c02e1739f6d3b5981e4327139477a12f987ed68
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120739"
---
# <a name="technology-controls-in-microsoft-365"></a>Controles de tecnología en Microsoft 365 

Microsoft usa varias herramientas y tecnologías para controlar, administrar y auditar el acceso a los datos de los clientes en sus servicios en línea. Se aplican a Exchange Online, SharePoint Online, Caja de seguridad y Caja de seguridad del cliente, autenticación multifactor y mucho más. Yammer usa controles similares descritos en [Los controles de acceso de Yammer Enterprise](assurance-yammer-enterprise-access-controls.md).

Los ingenieros de Microsoft 365 no tienen acceso permanente a los datos de clientes de Microsoft 365. Los ingenieros deben pasar por un proceso de aprobación de Microsoft antes de tener acceso a los datos de clientes para las operaciones de servicio. Si el cliente licencia la característica Caja de seguridad del cliente para Exchange Online y SharePoint Online, el acceso a los datos de cliente requiere la aprobación del cliente. Después de su aprobación, las cuentas administrativas específicas del servicio se aprovisionan con acceso puntual para las tareas requeridas por la solicitud de servicio.

## <a name="lockbox-and-customer-lockbox"></a>Caja de seguridad y caja de seguridad del cliente

Aunque rara vez, un cliente podría solicitar ayuda a Microsoft que exponga el contenido del cliente a un ingeniero de Microsoft. Para controlar el acceso a Exchange Online, Microsoft usa un sistema de control de acceso denominado Caja de seguridad. Antes de que cualquier ingeniero de Microsoft acceda a cualquier sistema o datos de Exchange Online o SharePoint Online, debe enviar una solicitud de acceso mediante la Caja de seguridad. Todas las solicitudes de servicio para Exchange Online y SharePoint Online se controlan mediante el sistema de caja de seguridad. Tanto con la Caja de seguridad como con la Caja de seguridad del cliente, todo el acceso aprobado es rastreable para un usuario único, lo que hace que los ingenieros den cuenta de su control de los datos de clientes.

> [!NOTE]
> Exchange Online incluye todos los datos de Skype Empresarial almacenados en buzones de usuario. La cobertura de Skype Empresarial no incluye las grabaciones de difusión de reunión de Skype ni el contenido cargado a las reuniones por los usuarios. SharePoint Online incluye OneDrive para la Empresa.

La caja de seguridad procesa las solicitudes de permisos que conceden a los ingenieros la capacidad de realizar funciones operativas y administrativas dentro del servicio. Los ingenieros envían solicitudes a través de la Caja de seguridad y un administrador de Microsoft debe aprobar la solicitud antes de que el ingeniero pueda acceder a los datos de cliente. Después de la aprobación del administrador, el ingeniero tiene acceso limitado por tiempo y ámbito a los datos de clientes para trabajar en el problema del cliente.

Caja de seguridad del cliente para Microsoft 365 le ayuda a cumplir las obligaciones de cumplimiento si necesita procedimientos para la autorización explícita de acceso a datos. Este es un requisito para algunos estándares de cumplimiento, como FedRAMP y HIPAA. La Caja de seguridad del cliente lo inserta en el proceso de aprobación de la caja de seguridad y le proporciona la capacidad de controlar la autorización del acceso de Microsoft al contenido de Exchange Online o SharePoint Online para las operaciones de servicio.

En el caso poco frecuente cuando un ingeniero de servicio de Microsoft necesita tener acceso a los datos, solo se concede acceso a los datos necesarios para resolver el problema y durante un período de tiempo limitado. Si rechaza una solicitud de acceso, los ingenieros de Microsoft no tendrán acceso al contenido y no podrán completar las operaciones de servicio. Si aprueba la solicitud, los ingenieros de Microsoft han limitado el acceso just-in-time a su contenido a través de interfaces de administración supervisadas y restringidas.

Las acciones realizadas por el ingeniero de soporte técnico se registran con fines de auditoría y son accesibles a través de la API de actividad de administración de [Office 365](/office/office-365-management-api/get-started-with-office-365-management-apis) y el Centro de seguridad [y cumplimiento.](https://protection.office.com/)

>[!NOTE]
> Caja de seguridad del cliente está disponible [en Microsoft 365 E5](https://products.office.com/business/office-365-enterprise-e5-business-software) como una compra de complemento. Para obtener más información, vea Solicitudes de caja de seguridad del cliente [de Microsoft 365.](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2)

## <a name="just-in-time-access"></a>Acceso just-in-time

Microsoft usa el principio de acceso just-in-time (JIT) de Microsoft 365 para mitigar los riesgos de manipulación de credenciales y los ataques laterales. JIT quita el acceso administrativo persistente a los servicios y reemplaza los derechos por la capacidad de elevarse a esos roles a petición. La eliminación de derechos de acceso persistente de los administradores garantiza que las credenciales solo estén disponibles cuando son necesarias y reduce los riesgos de robo de credenciales.

El modelo de acceso JIT requiere que los ingenieros soliciten privilegios elevados durante un período limitado para realizar tareas administrativas. Además, los ingenieros usan cuentas temporales creadas con contraseñas complejas generadas por máquina y solo conceden los roles que les permiten realizar las tareas necesarias. Por ejemplo, el acceso administrativo concedido por Caja de seguridad está limitado por tiempo y la cantidad de tiempo concedido depende del rol solicitado. Un ingeniero especifica la duración del acceso necesario en la solicitud al sistema de caja de seguridad. El sistema de caja de seguridad rechaza las solicitudes cuando el tiempo solicitado supera el tiempo máximo permitido para la elevación. Después de la expiración, se quita el acceso administrativo y expira la cuenta temporal.

Cuando se autoriza y aprueba el acceso, los ingenieros reciben una contraseña administrativa de uso único generada por el sistema de autorización. Las contraseñas nuevas se generan cada vez que se aprueba una solicitud de acceso elevado. La contraseña se copia en una contraseña segura, es independiente de las credenciales del ingeniero para el entorno corporativo de Microsoft y solo es válida para la sesión de acceso elevado aprobada.

## <a name="constrained-management-interfaces"></a>Interfaces de administración restringidas

Los ingenieros usan dos interfaces de administración para realizar tareas administrativas: Escritorio remoto a través de puertas de enlace de Terminal Service (TSG) protegidas y PowerShell remoto. Dentro de estas interfaces de administración, las directivas de software y los controles de acceso aplican restricciones significativas sobre las aplicaciones que se ejecutan y los comandos y cmdlets disponibles.

Los servidores de Microsoft 365 restringen las sesiones simultáneas a una sesión por administrador de equipo por servicio, por servidor. Los TSG solo permiten una única sesión simultánea para los usuarios y no permiten varias sesiones. Con una sola sesión por servidor, los TSG permiten a los administradores del equipo de servicio de Microsoft 365 conectarse a varios servidores simultáneamente para que los administradores puedan realizar sus tareas de forma eficaz. Los administradores del equipo de servicio no tienen permisos en los propios TSG. El TSG solo se usa para aplicar la autenticación multifactor (MFA) y los requisitos de cifrado. Una vez que el administrador del equipo de servicio se conecta a un servidor específico a través de un TSG, el servidor específico aplica un límite de sesión de uno por administrador.

Las restricciones de uso y los requisitos de conexión y configuración para el personal de Microsoft 365 se establecen mediante directivas de grupo de Active Directory. Estas directivas incluyen las siguientes características:

- Los TSG solo usan cifrado validado [fips](https://www.microsoft.com/TrustCenter/Compliance/FIPS) 140-2.
- Las sesiones de TSG se desconectan después de 30 minutos de inactividad.
- Las sesiones de TSG cierran sesión automáticamente después de 24 horas.

Las conexiones a los TSG también requieren MFA con una tarjeta inteligente física independiente y una cuenta independiente de las credenciales corporativas de Microsoft del ingeniero. A los ingenieros se les emiten diferentes tarjetas inteligentes para diversas plataformas y plataformas de administración de secretos que garantizan el almacenamiento seguro de las credenciales. Los TSG usan directivas de grupo de Active Directory para controlar quién puede iniciar sesión en servidores remotos, el número de sesiones permitidas y la configuración de tiempo de espera de inactividad. Las directivas adicionales limitan el acceso a las aplicaciones permitidas y restringen el acceso a Internet.

Además del acceso remoto mediante TSG configurados especialmente, Exchange Online permite a los usuarios con el rol De ingeniero de servicio acceder a determinadas funciones administrativas en servidores de producción con PowerShell remoto. Para ello, el usuario debe estar autorizado para el acceso de solo lectura (depuración) al entorno de producción de Microsoft 365. La escalación de privilegios se habilita de la misma forma que se habilita para los TSG mediante el proceso de caja de seguridad.

Para el acceso remoto, cada centro de datos tiene una IP virtual de carga equilibrada que sirve como un único punto de acceso. Los cmdlets de PowerShell remoto disponibles se basan en el nivel de privilegio identificado en la notificación de acceso obtenida durante la autenticación. Estos cmdlets proporcionan la única funcionalidad administrativa a la que pueden acceder los usuarios que se conectan mediante este método. PowerShell remoto limita el ámbito de los comandos disponibles para el ingeniero y se basa en el nivel de acceso concedido a través del proceso de caja de seguridad. Por ejemplo, en Exchange Online, Get-Mailbox puede estar disponible, pero Set-Mailbox lo haría.
