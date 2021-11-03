---
title: Microsoft 365 de acceso del ingeniero de servicio
description: Información general sobre la arquitectura de control Microsoft 365 de acceso del ingeniero de servicio.
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 2700c95feb5c32765e2dc3420c67800b154b1e9d
ms.sourcegitcommit: 85b36ce8c79fb111980cc6462f2addb44a924065
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2021
ms.locfileid: "60678489"
---
# <a name="microsoft-365-service-engineer-access-control"></a>Microsoft 365 de acceso del ingeniero de servicio

Zero Standing Access (ZSA) significa que el personal del equipo de servicio de Microsoft no tiene ningún acceso con privilegios permanentes al entorno de producción de Microsoft 365 ni a los datos del cliente. Cuando un miembro del equipo de servicio de Microsoft quiere actualizar el servicio o obtener acceso a los datos del cliente por cualquier motivo, debe enviar una solicitud que justifique la necesidad y recibir la aprobación de un administrador autorizado. A escala, no es factible proporcionar y quitar manualmente el acceso según sea necesario para mantener los servicios Microsoft 365, por lo que Microsoft ha desarrollado una solución automatizada para administrar el acceso con privilegios según sea necesario.

## <a name="lockbox"></a>Caja de seguridad

Lockbox, un sistema de control de acceso que usa un modelo just-in-time (JIT) y Just-Enough-Access (JEA) para proporcionar a los ingenieros de servicio acceso con privilegios temporales a los datos y servicios de Microsoft 365 especificados. Microsoft 365 Además, todas las solicitudes y acciones se registran con fines de auditoría y son accesibles mediante la API de actividad de administración de [Office 365](/office/office-365-management-api/get-started-with-office-365-management-apis) y el Centro de seguridad [y cumplimiento](https://protection.office.com/).

Para que un ingeniero de servicio de Microsoft pueda conectarse a cualquier Microsoft 365 o obtener acceso a los datos de los clientes, debe enviar una solicitud de acceso a través de lockbox. Esta solicitud solo se puede aprobar si se cumplen ciertos criterios:

- El ingeniero de servicio cumple los [requisitos de elegibilidad para una cuenta de equipo de servicio](assurance-microsoft-365-account-management.md),
- Pertenecen al rol Cuadro de bloqueo asociado con el trabajo de la solicitud,
- El tiempo de acceso solicitado no supera el tiempo máximo permitido,
- Tienen una justificación empresarial legítima,
- El recurso solicitado al que desean tener acceso está dentro de su ámbito de trabajo y
- Reciben aprobación de administrador

Una vez que Lockbox cumple y comprueba todos los criterios, se concede acceso temporal para realizar la acción específica solicitada. Una vez transcurrido el tiempo de la solicitud, se revoca el acceso.

![Proceso de acceso a la caja de seguridad.](../media/assurance-lockbox-process.png)

Además, si un cliente licencia [](/microsoft-365/compliance/customer-lockbox-requests) y habilita la característica Caja de seguridad del cliente, cualquier intento de un ingeniero de servicio de Microsoft para obtener acceso a los datos del cliente debe ser aprobado adicionalmente por un administrador en el inquilino del cliente. La necesidad de obtener acceso a los datos de los clientes puede surgir tanto del cliente como de Microsoft. Por ejemplo, un incidente producido por un cliente puede requerir acceso a sus datos para solucionar el problema o cuando Microsoft necesita acceso a datos para aplicar una actualización específica.

![Proceso de acceso a la caja de seguridad del cliente.](../media/assurance-customer-lockbox-process.png)

Los clientes no tienen herramientas para iniciar una solicitud de caja de seguridad del cliente; deben enviar un vale a Microsoft que requiera que se levante una solicitud de caja de seguridad del cliente. Un administrador de Microsoft y un administrador autorizado en el inquilino del cliente deben aprobar una solicitud de caja de seguridad del cliente que haya creado un ingeniero de servicio de Microsoft.

### <a name="lockbox-roles"></a>Roles de caja de seguridad

Para exigir la separación de funciones y el principio de privilegio mínimo, los ingenieros de servicio deben pertenecer a un rol de caja de seguridad que corresponda a su rol en el equipo. Los roles de caja de seguridad se administran dentro de la herramienta de administración de identidades y definen los privilegios y acciones para las que se puede aprobar un miembro del equipo de servicio a través del proceso de solicitud de caja de seguridad. El personal del equipo de servicio debe solicitar ser miembro de un rol de caja de seguridad y recibir aprobación de administrador. Si se aprueba, la cuenta del equipo de servicio del empleado se coloca en un grupo de seguridad impuesto por Active Directory (AD) y Azure Active Directory (AAD).

## <a name="constrained-management-interfaces"></a>Interfaces de administración restringidas

Los ingenieros de servicio usan dos interfaces de administración para realizar tareas administrativas: Escritorio remoto desde una estación de trabajo de acceso seguro (SAW) a través de una puerta de enlace de terminal service (TSG) segura y PowerShell remoto. Dentro de estas interfaces de administración, los controles de acceso basados en la solicitud de caja de seguridad aprobada y las directivas de software aplican restricciones significativas en las aplicaciones que se ejecutan y qué comandos y cmdlets están disponibles.

## <a name="remote-desktop"></a>Escritorio remoto

Los miembros del equipo de servicio que administran su servicio con Escritorio remoto deben conectarse desde un equipo PORTÁTIL SAW, especialmente diseñado y fabricado administrado por Microsoft específicamente para este caso de uso. Microsoft se asocia con proveedores para crear SAWs, creando una cadena de suministro corta y segura. Los SAW usan sistemas operativos con protección que están configurados para limitar todas las funciones excepto lo necesario para las tareas de administración definidas. Estas limitaciones incluyen la deshabilitación de todos los puertos USB, listas estrictas de acceso a aplicaciones, eliminación del acceso de correo electrónico, limitación de la navegación por Internet y aplicación de bloqueos de protectores de pantalla de inactividad. Los sistemas de control de acceso de Microsoft examinan las máquinas SAW periódicamente para asegurarse de que cumplen con los controles de seguridad más recientes y deshabilitan automáticamente las máquinas si se determina que no son compatibles.

Los ingenieros de servicio solo pueden conectarse a un TSG a la vez y no se permiten varias sesiones. Sin embargo, los TSG permiten Microsoft 365 administradores del equipo de servicio conectarse a varios servidores, cada uno con una sola sesión simultánea, para que los administradores puedan realizar sus tareas de forma eficaz. Los administradores del equipo de servicio no tienen permisos en los propios TSG. El TSG solo se usa para aplicar la autenticación multifactor (MFA) y los requisitos de cifrado. Una vez que el administrador del equipo de servicio se conecta a un servidor específico a través de un TSG, el servidor específico aplica un límite de sesión de uno por administrador.

Las directivas de grupo de Active Directory establecen restricciones de uso, conexión y requisitos de configuración para Microsoft 365 personal. Estas directivas incluyen las siguientes características de TSG:

- Usar solo [cifrado validado FIPS 140-2](/compliance/regulatory/offering-FIPS-140-2)
- Las sesiones se desconectan después de 15 minutos de inactividad
- Las sesiones cierran sesión automáticamente después de 24 horas

Las conexiones a TSG también requieren MFA mediante una tarjeta inteligente física independiente. Los ingenieros de servicio se emiten diferentes tarjetas inteligentes para varias plataformas y plataformas de administración de secretos que garantizan el almacenamiento seguro de las credenciales. Los TSG usan directivas de grupo de Active Directory para controlar quién puede iniciar sesión en servidores remotos, el número de sesiones permitidas y la configuración de tiempo de espera de inactividad.

## <a name="remote-powershell"></a>PowerShell remoto

Además del acceso remoto mediante TSG especialmente configurados, el personal del equipo de servicio con el rol Caja de seguridad de operaciones del ingeniero de servicio puede tener acceso a determinadas funciones administrativas en servidores de producción mediante PowerShell remoto. Para usar este acceso, el usuario debe estar autorizado para el acceso de solo lectura (depuración) al entorno Microsoft 365 producción. La escalación de privilegios está habilitada de la misma manera que se habilita para los TSG mediante el proceso de caja de seguridad.

Para el acceso remoto, cada centro de datos tiene una DIRECCIÓN IP virtual con equilibrio de carga que sirve como un único punto de acceso. Los cmdlets de PowerShell remotos disponibles se basan en el nivel de privilegios identificado en la notificación de acceso obtenida durante la autenticación. Estos cmdlets proporcionan la única funcionalidad administrativa accesible para los usuarios que se conectan con este método. PowerShell remoto limita el ámbito de los comandos disponibles para el ingeniero y se basa en el nivel de acceso concedido a través del proceso de caja de seguridad. Por ejemplo, en Exchange Online, el cmdlet Get-Mailbox puede estar disponible, pero el cmdlet Set-Mailbox no lo haría.

## <a name="resources"></a>Recursos

- [Aislamiento en Microsoft 365](assurance-isolation-in-microsoft-365.md)
- [Comprobación en segundo plano de Microsoft sobre el](assurance-pre-employment-screening.md)examen previo al empleo en la nube de[Microsoft](assurance-cloud-background-check.md)
