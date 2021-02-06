---
title: Controles de acceso administrativo en Microsoft 365
description: En este artículo se proporciona información general sobre los controles de acceso administrativo y la categorización de datos en Microsoft 365.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: d3d6cd30fbe682de979d5c04943c57cedc86552f
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120719"
---
# <a name="administrative-access-controls-in-microsoft-365"></a>Controles de acceso administrativo en Microsoft 365 

Microsoft ha invertido mucho en sistemas y controles que automatizan la mayoría de las operaciones de Microsoft 365, a la vez que limita intencionadamente el acceso al contenido de los clientes por parte de Microsoft. Los humanos rigen el servicio y el software opera el servicio. Esta estructura permite a Microsoft administrar Microsoft 365 a escala y administrar los riesgos de las amenazas internas para el contenido del cliente.

De forma predeterminada, los ingenieros de Microsoft tienen cero privilegios administrativos permanentes y ningún acceso permanente al contenido de los clientes en Microsoft 365. Un ingeniero de Microsoft puede tener acceso limitado, auditado y protegido al contenido de un cliente durante un período de tiempo limitado. El acceso es solo cuando es necesario para las operaciones de servicio y solo cuando lo aprueba un miembro de la administración superior de Microsoft. Para los clientes con licencia de caja de seguridad del cliente, el cliente proporciona la aprobación de acceso a su contenido hospedado en Microsoft 365.

Microsoft proporciona servicios en línea con varias formas de entrega en la nube:

- **Nubes públicas:** Incluye versiones multiinquilino de Microsoft 365, Azure y otros servicios hospedados en Norteamérica, América del Sur, Europa, Asia, Australia, etc.
- **Nubes nacionales:** Incluye todas las nubes soberanas y operadas por terceros fuera de los Estados Unidos (excepto las que se han indicado anteriormente), como Microsoft 365 en China (operado por 21Vianet) y Microsoft 365 en Alemania (operado por Microsoft, pero bajo un modelo en el que un administrador de datos alemán, Deutsche Telekom, controla y supervisa el acceso de Microsoft a los datos de clientes y sistemas que contienen datos de clientes).
- **Nubes de administración pública:** Incluye los servicios de Microsoft 365 y Azure que están disponibles para los clientes gubernamentales de Estados Unidos.

Para este artículo, los servicios de Microsoft 365 incluyen:

- [Exchange Online](/Exchange/exchange-online)
- [Exchange Online Protection](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [SharePoint Online](/sharepoint/sharepoint-online)
- [OneDrive para la Empresa](/OneDrive/onedrive)
- [Skype Empresarial](/SkypeForBusiness/skype-for-business-online)
- [Microsoft Teams](/MicrosoftTeams/Teams-overview)
- [Yammer](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a>Controles de acceso de Microsoft 365

Con fines de control de acceso, Microsoft clasifica los datos de Microsoft 365 como datos de clientes u otros tipos de datos.

### <a name="customer-data"></a>Datos de cliente

Los datos de cliente son todos los datos proporcionados por un cliente o en su nombre al usar los servicios de Microsoft 365. Estos datos son contenido del cliente creado o cargado directamente por usuarios de Microsoft 365, incluidos:

- Mensajes de correo electrónico
- Contenido de SharePoint Online
- Mensajes instantáneos
- Elementos de calendario
- Documentos
- Contactos
- Información identificable del usuario final (EUII) (datos que son exclusivos de un usuario o que se pueden vincular a un usuario individual pero que no incluyen contenido del cliente)

### <a name="other-types-of-data"></a>Otros tipos de datos

Otros tipos de datos son:

- **Datos de la cuenta:** Incluye datos administrativos (información proporcionada por los administradores al registrarse o comprar servicios) y datos de pago (información sobre instrumentos de pago, como los detalles de la tarjeta de crédito).
- **Información de identificación organizativa:** Incluye datos usados para identificar un inquilino, datos de uso y no vinculables a un usuario individual o incluidos en el contenido del cliente.
- **Metadatos del sistema:** Incluye registros de servicio que contienen opciones de configuración, estado del sistema, direcciones IP de Microsoft e información técnica sobre suscripciones e inquilinos.

Microsoft ha establecido mecanismos de control de acceso para garantizar que nadie tiene acceso no aprobado a los datos de clientes ni a los datos de control de acceso. Los datos de control de acceso administran el acceso a otros tipos de datos o funciones dentro del entorno, incluido el acceso al contenido del cliente o EUII, las contraseñas de Microsoft, los certificados de seguridad y otros datos relacionados con la autenticación. Los mecanismos de control de acceso también protegen contra el acceso físico, lógico o remoto no aprobado al entorno de producción de Microsoft 365.

Hay tres categorías de controles de acceso usados por Microsoft para el funcionamiento de Microsoft 365:

- Controles de aislamiento
- Controles de personal
- Controles de tecnología

Cuando se combinan, estos controles ayudan a evitar y detectar acciones malintencionadas en Microsoft 365. Además de los controles de aislamiento, personal y tecnología usados por Microsoft, hay una cuarta categoría de controles: los controles implementados por los clientes.

Microsoft 365 le permite administrar los datos de la misma forma que los datos se administran en entornos locales. La persona que se suscribe a una organización para Microsoft 365 se convierte automáticamente en administrador global. El administrador global tiene acceso a todas las características de los portales de administración y puede:

- Crear o editar usuarios
- Asignar roles de administrador a otros usuarios
- Restablecer contraseñas de usuario
- Administrar licencias de usuario
- Administrar dominios
- Aprobar solicitudes de caja de seguridad del cliente

Se recomienda que cada organización configure al menos dos cuentas de administrador. Para las grandes organizaciones empresariales, se recomiendan cuentas de administrador especializadas que atienden diferentes funciones.

Para obtener información acerca de la asignación de roles y permisos de administrador, vea [Asignar roles de administrador](/microsoft-365/admin/add-users/assign-admin-roles) y Acerca de los roles de [administrador.](/microsoft-365/admin/add-users/about-admin-roles)

## <a name="related-links"></a>Vínculos relacionados

- [Aislamiento en Microsoft 365](assurance-isolation-in-microsoft-365.md)
- [Filtrado previo al empleo de Microsoft](assurance-pre-employment-screening.md)
- [Comprobación de antecedentes en la nube de Microsoft](assurance-cloud-background-check.md)
- [Auditoría y supervisión de controles de acceso](assurance-monitoring-and-auditing-access-controls.md)
- [Controles de acceso de Yammer Enterprise](assurance-yammer-enterprise-access-controls.md)
