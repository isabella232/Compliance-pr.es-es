---
title: Controles de aislamiento de Microsoft 365
description: Obtenga información sobre los controles de aislamiento en Microsoft 365
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
ms.openlocfilehash: 312de9f1417ba6298898d47b2b7e05b5fa7034fe
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160250"
---
# <a name="microsoft-365-isolation-controls"></a>Controles de aislamiento de Microsoft 365

Microsoft trabaja continuamente para garantizar que la arquitectura multiinquilino de Microsoft 365 admite estándares de seguridad, confidencialidad, privacidad, integridad, locales, internacionales y de [disponibilidad.](https://www.microsoft.com/trust-center/compliance/compliance-overview) La escala y el ámbito de los servicios proporcionados por Microsoft dificultan y no son económicos la administración de Microsoft 365 con una interacción humana significativa. Microsoft 365 servicios se proporcionan a través de centros de datos distribuidos globalmente, cada uno de ellos altamente automatizado con pocas operaciones que requieren un toque humano o cualquier acceso al contenido del cliente. Nuestro personal admite estos servicios y centros de datos con herramientas automatizadas y acceso remoto altamente seguro.

Microsoft 365 se compone de varios servicios que proporcionan una funcionalidad empresarial importante y contribuyen a toda la experiencia Microsoft 365 negocio. Cada uno de estos servicios es independiente y está diseñado para integrarse entre sí. Microsoft 365 está diseñado con los siguientes principios:

- Arquitectura orientada al servicio: diseño y desarrollo de software en forma de servicios interoperables que proporcionan una funcionalidad empresarial bien definida.
- [Seguridad](https://www.microsoft.com/securityengineering/osa)operativa: un marco que incorpora los conocimientos adquiridos a través de diversas capacidades que son exclusivas de Microsoft, como el Ciclo de vida de desarrollo de seguridad de [Microsoft,](https://www.microsoft.com/sdl/default.aspx)el Centro de respuesta de seguridad de [Microsoft](https://www.microsoft.com/msrc)y un profundo conocimiento del panorama de amenazas de ciberseguridad.

Microsoft 365 entre sí, pero se diseñan e implementan para que se puedan implementar y operar como servicios autónomos, independientemente entre sí. Microsoft segrega las tareas y áreas de responsabilidad de Microsoft 365 para reducir las oportunidades de modificación o mal uso no autorizados o involuntarias de los activos de la organización. Microsoft 365 los equipos han definido roles como parte de un mecanismo de control de acceso completo basado en roles.

## <a name="tenant-isolation"></a>Aislamiento de espacios empresariales

Una de las principales ventajas de la informática en la nube es el concepto de una infraestructura común y compartida entre numerosos clientes simultáneamente, lo que lleva a economías de escala. Microsoft trabaja continuamente para garantizar que las arquitecturas multiinquilino de nuestros servicios en la nube admitan estándares de seguridad, confidencialidad, privacidad, integridad y disponibilidad de nivel empresarial.

Los servicios en la nube de Microsoft se diseñaron con la suposición de que todos los inquilinos son potencialmente hostiles para todos los demás inquilinos y hemos implementado medidas de seguridad para evitar que las acciones de un inquilino afecten a la seguridad o al servicio de otro inquilino o accedan al contenido de otro inquilino.

Los dos objetivos principales de mantener el aislamiento de inquilinos en un entorno multiinquilino son:

- Impedir la filtración o el acceso no autorizado al contenido del cliente entre inquilinos; y
- Impedir que las acciones de un inquilino afecten negativamente al servicio de otro inquilino

Se han implementado varias formas de protección a lo largo de Microsoft 365 para impedir que los clientes puedan poner en peligro los servicios o aplicaciones de Microsoft 365 o obtener acceso no autorizado a la información de otros inquilinos o del propio sistema Microsoft 365, incluidos:

- El aislamiento lógico del contenido del cliente dentro de cada espacio empresarial para Microsoft 365 servicios se logra Azure Active Directory autorización y control de acceso basado en roles.
- SharePoint Online proporciona mecanismos de aislamiento de datos en el nivel de almacenamiento.
- Microsoft usa una seguridad física rigurosa, un filtrado en segundo plano y una estrategia de cifrado multicapa para proteger la confidencialidad y la integridad del contenido del cliente. Todos Microsoft 365 centros de datos tienen controles de acceso biométricos, con la mayoría de las impresiones de la palma para obtener acceso físico. Además, todos los empleados de Microsoft con sede en Estados Unidos deben completar correctamente una comprobación de antecedentes estándar como parte del proceso de contratación. Para obtener más información sobre los controles usados para el acceso administrativo en Microsoft 365, vea [Microsoft 365 Account Management](assurance-microsoft-365-account-management.md).
- Microsoft 365 tecnologías del lado del servicio que cifran el contenido del cliente en reposo y en tránsito, incluido BitLocker, cifrado por archivo, Seguridad de la capa de transporte (TLS) y Seguridad de protocolo de Internet (IPsec). Para obtener detalles específicos sobre el cifrado en Microsoft 365, vea [Tecnologías de cifrado de datos en Microsoft 365](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview).

Juntos, las protecciones mencionadas anteriormente proporcionan controles de aislamiento lógico robustos que proporcionan protección contra amenazas y mitigación equivalentes a las proporcionadas por el aislamiento físico solo.

## <a name="resources"></a>Recursos

- [Aislamiento y control de acceso en Azure Active Directory](/microsoft-365/enterprise/microsoft-365-isolation-in-azure-active-directory)
- [Supervisión y prueba de límites de inquilinos](assurance-monitoring-and-testing.md)
- [Aislamiento y control de acceso en Microsoft 365](/microsoft-365/enterprise/microsoft-365-isolation-in-microsoft-365)
