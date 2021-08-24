---
title: Administración de cuentas en Microsoft 365
description: Obtenga información sobre la administración de cuentas en Microsoft 365
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
ms.openlocfilehash: d525edfb9854df156f5b7b8571199b7a0102a0bf
ms.sourcegitcommit: 61357661caf64eeb9143046b4dd66c83e1439ee3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2021
ms.locfileid: "58473027"
---
# <a name="account-management-in-microsoft-365"></a>Administración de cuentas en Microsoft 365

Microsoft ha invertido en gran medida en sistemas y controles que automatizan la mayoría de las operaciones Microsoft 365, al tiempo que limita intencionadamente la necesidad de acceso directo a los servidores y los datos del cliente por parte del personal de servicio. Los humanos rigen el servicio y el software opera el servicio. Esta estructura permite a Microsoft administrar Microsoft 365 escala y minimiza los riesgos de las amenazas internas y externas. Microsoft se acerca al control de acceso con la suposición de que todos son una amenaza potencial para Microsoft 365 servicios y datos de clientes. Por este motivo, el principio de acceso permanente cero (ZSA) da las bases para toda la estructura de control de acceso usada por Microsoft 365.

De forma predeterminada, el personal de Microsoft no tiene acceso con privilegios permanentes a Microsoft 365 entorno o datos de clientes de una organización. Solo a través de un sistema sólido de comprobaciones y aprobaciones, el personal del equipo de servicio puede obtener acceso con privilegios con una acción y un ámbito de tiempo limitados. A través de este sistema, Microsoft puede reducir significativamente el potencial de Microsoft 365 personal de servicio y atacantes de obtener acceso no autorizado o causar daños malintencionados o accidentales a servicios Microsoft y clientes.

## <a name="account-types"></a>Tipos de cuenta

Microsoft 365 todas las misiones organizativas y funciones empresariales mediante tres categorías de cuentas: cuentas de equipo de servicio, cuentas de servicio y cuentas de cliente. La administración de estas cuentas es una responsabilidad compartida entre Microsoft y los clientes. Microsoft administra las cuentas de servicio y de equipo de servicio, que se usan para operar y admitir productos y servicios de Microsoft. Las cuentas de cliente son administradas por el cliente y les permiten adaptar el acceso a las cuentas para cumplir con sus requisitos de control de acceso interno.

![Responsabilidad compartida de las cuentas](../media/assurance-shared-responsibility-for-accounts.png)

## <a name="microsoft-managed-accounts"></a>Cuentas administradas por Microsoft

**Las cuentas de equipo** de servicio las usa Microsoft 365 personal del equipo de servicio que desarrolla y mantiene Microsoft 365 servicios. Estas cuentas no tienen acceso con privilegios permanentes a los servicios Microsoft 365, sino que se pueden usar para solicitar acceso con privilegios temporales y limitados para realizar una función de trabajo especificada. No todas las cuentas de equipo de servicio pueden realizar las mismas acciones, la separación de tareas se aplica mediante el control de acceso basado en roles (RBAC). Los roles garantizan que los miembros del equipo de servicio y sus cuentas solo tienen el acceso mínimo necesario para realizar tareas de trabajo específicas. Además, las cuentas de equipo de servicio no pueden pertenecer a varios roles donde pueden actuar como aprobadores de sus propias acciones.

**Las cuentas** de servicio las usan Microsoft 365 para autenticarse al comunicarse con otros servicios a través de procesos automatizados. Al igual que a las cuentas de equipo de servicio solo se les proporciona el acceso mínimo necesario para realizar las tareas de trabajo del personal específico, a las cuentas de servicio solo se les concede el acceso mínimo necesario para su propósito. Además, hay varios tipos de cuentas de servicio diseñadas para satisfacer una necesidad específica. Un Microsoft 365 puede tener varias cuentas de servicio, cada una con un rol diferente para realizar.

## <a name="customer-managed-accounts"></a>Cuentas administradas por el cliente

**Las cuentas de** cliente se usan para acceder Microsoft 365 servicio y son las únicas cuentas de las que cada cliente es responsable. El deber del cliente es crear y administrar las cuentas de su organización para mantener un entorno seguro. La administración de cuentas de cliente se realiza Azure Active Directory (AAD) o federada con Active Directory (AD) local. Cada cliente tiene un conjunto único de requisitos de control de acceso que deben cumplir y las cuentas de cliente conceden a cada cliente la capacidad de satisfacer sus necesidades individuales. Las cuentas de cliente no pueden acceder a ningún dato fuera de su organización de clientes.

## <a name="service-team-account-management"></a>Administración de cuentas de equipo de servicio

Microsoft 365 cuentas de equipo de servicio a lo largo de su ciclo de vida mediante un sistema de administración de cuentas denominado Identity Management (IDM). IDM usa una combinación de procesos de verificación automatizados y aprobación de administrador para aplicar los requisitos de seguridad relacionados con el acceso a cuentas de equipo de servicio.

Los miembros del equipo de servicio no obtienen automáticamente una cuenta de equipo de servicio, primero deben cumplir los requisitos de elegibilidad y obtener la aprobación de un administrador autorizado. Para poder optar a una cuenta de equipo de servicio, el [](assurance-cloud-background-check.md)personal del equipo de servicio debe pasar primero por el examen de personal previo al [empleo,](assurance-pre-employment-screening.md)una comprobación de antecedentes en la nube y completar toda la formación estándar y necesaria basada en roles. Una vez que se han cumplido todos los requisitos de elegibilidad, se puede realizar una solicitud para una cuenta de equipo de servicio y debe ser aprobada por un administrador autorizado.

![Proceso de selección de personal](../media/assurance-personnel-screening-process.png)

IDM también es responsable de realizar un seguimiento de la revisión periódica y la formación necesarias para mantener una cuenta de equipo de servicio. La comprobación en segundo plano de la nube de Microsoft debe completarse cada dos años y todo el material de aprendizaje debe revisarse anualmente. Si alguno de estos requisitos no se cumple en la fecha de expiración, su elegibilidad se revoca y la cuenta del equipo de servicio se deshabilita automáticamente.

Además, la elegibilidad de la cuenta del equipo de servicio se actualiza automáticamente mediante transferencia [y terminación de personal.](assurance-employee-transfer-termination.md) Los cambios realizados en el Sistema de información de recursos humanos (HRIS) desencadenan que IDM tome medidas, lo que varía en función de la situación. El personal que se transfiere a otro equipo de servicio tendrá una fecha de expiración establecida para sus elegibilidades y una solicitud para mantener los requisitos debe ser enviada por el miembro del equipo de servicio y aprobada por su nuevo administrador. El personal terminado tiene automáticamente todas las elegibilidades revocadas y su cuenta de equipo de servicio está deshabilitada en su último día. Se puede realizar una solicitud urgente de revocación de cuenta para las terminaciones involuntarias.

De forma predeterminada, las cuentas de equipo de servicio tienen acceso de lectura limitado a los metadatos generales del sistema que se usan para la solución de problemas periódica. Además, las cuentas del equipo de servicio de línea base no pueden solicitar acceso con privilegios a Microsoft 365 datos de clientes. Se debe realizar otra solicitud para que la cuenta del equipo de servicio se agregó a un rol que permite al miembro del equipo de servicio solicitar privilegios elevados para realizar tareas y operaciones específicas.
