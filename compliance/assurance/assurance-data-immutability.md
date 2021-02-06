---
title: Inmutabilidad de datos en Microsoft 365
description: Obtenga información sobre cómo Microsoft 365 conserva los datos de forma detectable para abordar el cumplimiento normativo, los requisitos de gobierno interno y los riesgos de litigio.
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
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: da465b850a9216dd64f8e4d9e6450c6a17f7b26d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120669"
---
# <a name="data-immutability-in-microsoft-365"></a>Inmutabilidad de datos en Microsoft 365

El cumplimiento normativo, los requisitos de gobierno interno o los riesgos de litigio requieren que las organizaciones conserven el correo electrónico y los datos asociados de forma detectable. Todos los datos del sistema deben ser detectables y ninguno de ellos se puede destruir ni modificar. El término estándar del sector para esto es "inmutabilidad".

Los métodos tradicionales para la inmutabilidad normalmente funcionaban moviendo mensajes de correo electrónico a una ubicación de almacenamiento independiente de solo lectura. Aunque estos sistemas sirven para conservar los elementos de buzón para su detección, a menudo afectan a la experiencia del usuario al quitar elementos conservados del flujo de trabajo diario habitual. Para los profesionales de TI, este enfoque de inmutabilidad requiere la implementación y el mantenimiento continuo de una infraestructura de almacenamiento y servidor independiente. La detección se realiza con herramientas externas al sistema de correo e incluye costos de implementación y mantenimiento asociados.

A través de las características de directiva de conservación y retención local del archivado en Microsoft 365 y sus servicios, puede conservar y conservar muchas clases de datos entrantes, internos y salientes. Incluye lo siguiente:

- Comunicaciones de correo electrónico entrantes y salientes
- Libros y registros contenidos en formularios de correo electrónico o documentos en línea compartidos
- Convocatorias de reunión
- Faxes
- Mensajes instantáneos
- Documentos compartidos durante reuniones en línea
- Correos de voz

Además, Microsoft ha desarrollado características de [](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) complemento para permitir el archivado de datos de otros orígenes a través de la integración con soluciones de administración y captura de datos de terceros. Después de importar datos de terceros, puede aplicar características de cumplimiento de Microsoft 365 a los datos, incluidos:

- [Retención por juicio](/microsoft-365/compliance/create-a-litigation-hold)
- [Exhibición de documentos electrónicos local y retención](/microsoft-365/compliance/manage-legal-investigations)
- [Búsqueda de cumplimiento](/microsoft-365/compliance/search-for-content)
- [Archivado local](/microsoft-365/compliance/enable-archive-mailboxes)
- [Auditoría de buzones](/microsoft-365/compliance/enable-mailbox-auditing)
- [Directivas de retención](/microsoft-365/compliance/retention-policies)

Por ejemplo, cuando un buzón se coloca en retención por juicio, se conservan los datos de terceros. Puede buscar datos de terceros con In-Place eDiscovery o búsqueda de cumplimiento. O bien, puede aplicar directivas de archivado y retención a datos de terceros como puede hacer con los datos de Microsoft. El archivado de datos de terceros en Microsoft 365 ayuda a su organización a cumplir con las directivas gubernamentales y reglamentarias.

El archivado en Microsoft 365 proporciona almacenamiento conforme a la regla 17a-4 de la Comisión de Bolsa y Valores (SEC). Microsoft 365 conserva los archivos permanentes de todos los datos recopilados en un formato que no se puede reescribir y que no se puede borrar mediante directivas de retención locales y directivas de conservación, incluido el bloqueo de conservación.

En particular:

- Todos los registros almacenados con las directivas de retención mencionadas anteriormente se conservan en un área de almacenamiento dedicada fuera del ámbito del usuario normal. Solo los usuarios autorizados pueden acceder a estos registros y buscarlos, pero no pueden modificarlos ni borrarlos.
- Los metadatos de cada elemento incluyen una marca de tiempo usada en el cálculo de la duración de retención. Las marcas de tiempo se aplican cuando se recibe o crea un nuevo elemento y no se pueden modificar ni quitar de los metadatos.
- El archivado en Microsoft 365 permite a los usuarios combinar diferentes directivas de retención y retener acciones para crear directivas de retención pormenorizados. Estas directivas definen el tipo o la ubicación de los elementos conservados y la duración de la conservación.
- La característica bloqueo de conservación permite a los usuarios elegir si la directiva es restrictiva. Una directiva restrictiva prohíbe a cualquier usuario tener la capacidad de quitar, deshabilitar o realizar cambios en la directiva de retención. Esto significa que una vez habilitado el bloqueo de conservación, no se puede deshabilitar y no existirá ningún mecanismo bajo el cual los datos de los administradores existentes recopilados por las directivas de retención locales se puedan sobrescribir, modificar, borrar o eliminar durante el período de conservación. Además, es posible que el período de retención establecido por el bloqueo de conservación no se acorte ni disminuya. Sin embargo, puede ser más largo, en el caso de un requisito legal para continuar con la retención de los datos almacenados, como se indicó anteriormente. El bloqueo de conservación garantiza que nadie, ni siquiera los administradores o aquellos con acceso de control determinado, puedan cambiar la configuración o sobrescribir o borrar los datos almacenados, lo que hace que el archivado en Microsoft 365 se ajuste a las instrucciones establecidas en la versión 2003 de la regla 17a-4 de la SEC.

Para comprender cómo Microsoft 365 le ayuda a cumplir las obligaciones reglamentarias, específicamente en relación con los requisitos de la regla 17a-4, consulte las [whitepaper](https://www.microsoft.com/microsoft-365/blog/wp-content/uploads/2015/11/Microsoft-EOA-White-Paper.pdf) que cubren Archivado de Exchange Online, SharePoint Online, OneDrive para la Empresa y Skype Empresarial. Las whitepaper también proporcionan un análisis detallado de las características y funcionalidades de archivado de Microsoft 365 con cada uno de los requisitos de la regla 17a-4 de la SEC y demuestra a los clientes regulados cómo el archivado de Microsoft 365 puede permitirles cumplir estos requisitos.
