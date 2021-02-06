---
title: Normativa de administración de exportaciones de Ee. UU. (EAR)
description: Los servicios en la nube de Microsoft ayudan a los clientes sujetos al Reglamento de Administración de Exportaciones de Estados Unidos (EAR) a cumplir sus requisitos de cumplimiento y administrar los riesgos de control de exportación.
keywords: Microsoft 365, cumplimiento, ofertas
localization_priority: None
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: fbc8166770a3ad2539264bbf76319116a2c306a9
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120009"
---
# <a name="us-export-administration-regulations-ear"></a>Normativa de administración de exportaciones de Ee. UU. (EAR)

## <a name="about-the-ear"></a>Acerca de la EAR

El Departamento de Comercio de los Estados Unidos aplica el Reglamento de Administración de Exportaciones (EAR) a través de la [Oficina de Industria y Seguridad (BIS).](https://www.bis.doc.gov/) La EAR rige e impone controles a la exportación y reex exportación de la mayoría de los productos comerciales, software y tecnología, incluidos los elementos de "doble uso" que se pueden usar con fines comerciales y civiles y ciertos elementos de defensa.

La guía de BIS contiene que, cuando los datos o software se cargan en la nube o se transfieren entre nodos de usuario, el cliente, no el proveedor de la nube, es el "exportador" que tiene la responsabilidad de garantizar que las transferencias, el almacenamiento y el acceso a los datos o software cumplan con la EAR.

De acuerdo con  [el BIS,](https://www.bis.doc.gov/index.php/documents/regulation-docs/412-part-734-scope-of-the-export-administration-regulations/file)la exportación hace referencia a la transferencia de tecnología protegida o datos técnicos a un destino externo o su lanzamiento a una persona externa en los Estados Unidos (también denominada exportación considerada *).* La EAR rige ampliamente:

- Exportaciones de Los Estados Unidos.
- Volver a exportar o volver a exportar elementos de origen estadounidense y determinados elementos de origen externo con más de una parte *de minimis* de contenido de origen estadounidense.
- Transferencias o divulgaciones a personas de otros países.

Los elementos sujetos a la EAR se pueden encontrar en la lista de control comercial (CCL), donde cada elemento tiene asignado un número de clasificación de control de exportación [(ECCN)](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn)único. Los elementos que no aparecen en el CCL se designan como EAR99 y la mayoría de los productos comerciales EAR99 no requerirán una licencia para exportarse. Sin embargo, según el destino, el usuario final o el uso final del elemento, incluso un elemento EAR99 puede requerir una licencia de exportación de BIS.

La regla [final,](https://www.federalregister.gov/documents/2016/06/03/2016-12734/revisions-to-definitions-in-the-export-administration-regulations)publicada en junio de 2016, aclaró que los requisitos de licencia de la EAR tampoco se aplicarían a la transmisión y almacenamiento de datos técnicos y software sin clasificar si se cifraban de un extremo a otro mediante módulos criptográficos validados por FIPS 140-2 y no se almacenaban intencionadamente en un país impuesto por el gobierno ni en la Federación de Rusia.

## <a name="microsoft-and-the-ear"></a>Microsoft y la EAR

Las tecnologías, productos y servicios de Microsoft están sujetos al Reglamento de Administración de Exportaciones de Estados Unidos (EAR). Aunque no hay ninguna certificación de cumplimiento para la EAR, Microsoft Azure, Microsoft Azure Government y Microsoft Office 365 Government (entornos GCCHigh y DoD) ofrecen características y herramientas importantes para ayudar a los clientes elegibles sujetos a la EAR a administrar los riesgos de control de exportación y cumplir sus requisitos de cumplimiento.

El Departamento de Comercio de Estados Unidos, que aplica la EAR, ha tomado la posición de que los clientes, no los proveedores de servicios en la nube como Microsoft, se consideran exportadores de sus propios datos de cliente. Aunque la mayoría de los datos de los clientes no se considera "tecnología" o "datos técnicos" sujetos a los controles de exportación de EAR, los servicios en la nube de Microsoft en el ámbito están estructurados para ayudar a los clientes a administrar y mitigar significativamente los posibles riesgos de control de exportación a los que se enfrentan. Microsoft generalmente, pero no exclusivamente, recomienda el uso de sus servicios en la nube de administración pública para los clientes elegibles. Con una planeación adecuada, los clientes pueden usar las siguientes herramientas y sus propios procedimientos internos para ayudar a garantizar el cumplimiento total de los controles de exportación de Estados Unidos.

- **Controles en la ubicación de datos**. Los clientes tienen visibilidad sobre dónde se almacenan sus datos y acceso a herramientas sólidas para restringir su almacenamiento. Por lo tanto, pueden asegurarse de que sus datos se almacenan en los Estados Unidos y minimizar la transferencia de tecnología controlada o datos técnicos fuera de los Estados Unidos. Además, los datos de los clientes no se almacenan en una ubicación no conforme, de acuerdo con las prohibiciones de ear sobre dónde se "almacenan intencionalmente" los datos: ningún centro de datos de Azure se encuentra en ninguno de los 25 países del Grupo D:5 ni en la Federación de Rusia.
- **Cifrado de un extremo a otro.** Al aprovechar el puerto seguro de cifrado de un extremo a otro para las ubicaciones de almacenamiento físico especificadas en la EAR, los servicios en la nube de Microsoft en el ámbito proporcionan características de cifrado que pueden ayudar a proteger contra los riesgos de control de exportación. También ofrecen a los clientes una [amplia](https://aka.ms/Azure-Encryption-Overview) gama de opciones para cifrar datos en tránsito y en reposo, y la flexibilidad de elegir entre las opciones de cifrado.
- **Herramientas y protocolos para evitar la exportación no autorizada.** El uso del cifrado también ayuda a proteger contra una posible exportación (o se considera una reex exportación) en la EAR, ya que aunque una persona que no sea estadounidense tenga acceso a datos cifrados, no se revela nada si no puede leer o comprender los datos mientras está cifrado; por lo tanto, no hay ninguna "liberación" de datos controlados.

## <a name="microsoft-in-scope-cloud-services"></a>Servicios de la nube dentro del alcance de Microsoft

- [Azure y Azure Government](https://aka.ms/AzureCompliance)
- [Office 365 Administración General (GCC-High y DoD)](https://aka.ms/Office-365-Export-Controls)
- Intune

## <a name="how-to-implement"></a>Cómo se debe implementar

Información general sobre los controles de exportación de Estados Unidos y las instrucciones para los clientes que evalúan sus obligaciones en virtud de la EAR.

- [Azure](https://aka.ms/Azure-Export-Controls)
- [Office 365](https://aka.ms/Office-365-Export-Controls)

## <a name="frequently-asked-questions"></a>Preguntas más frecuentes

**¿Qué debo hacer para cumplir con los controles de exportación al usar los servicios en la nube de Microsoft?**

En la EAR, cuando los datos se cargan en un servidor en la nube como la nube de Microsoft, el cliente propietario de los datos , no el proveedor de servicios en la nube, se considera el exportador. Por este motivo, el propietario de los datos (es decir, el cliente de Microsoft) debe evaluar detenidamente cómo su uso de la nube de Microsoft puede implicar a los controles de exportación de Estados Unidos y determinar si alguno de los datos que quiere usar o almacenar puede estar sujeto a los controles EAR y, si es así, qué controles se aplican. Obtenga más información sobre cómo [los servicios](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers) en la nube de [Azure y Office 365](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE1s5kI) pueden ayudar a los clientes a garantizar su cumplimiento total con los controles de exportación de Estados Unidos.

**¿Las tecnologías, productos y servicios de Microsoft están sujetos a la EAR?**

La mayoría de las tecnologías, productos y servicios de Microsoft:

- No están sujetos a la EAR y, por lo tanto, no están en la lista de control comercial y no tienen ECCN;
- O bien, son elegibles para el mercado masivo ear99 o 5D992 para la autoclasificación por Parte de Microsoft y se pueden exportar a países sin embargo sin una licencia como no se requiere licencia (NLR).

Dicho esto, a algunos productos de Microsoft se les ha asignado un ECCN que puede requerir o no una licencia. Consulte a la EAR o a los asesores legales para determinar el tipo de licencia adecuado y los países elegibles para fines de exportación.

**¿Cuál es la diferencia entre la EAR y el Reglamento internacional de tráfico de armas (ITAR)?**

Los principales controles de exportación de Estados Unidos con la aplicación más amplia son la EAR, administrada por el Departamento de Comercio de estados Unidos. La EAR se aplica a los elementos de doble uso que tienen aplicaciones comerciales y civiles, y a los elementos con aplicaciones puramente comerciales.

Los Estados Unidos también tienen normativas de control de exportación independientes y más especializadas, como el ITAR, que rigen los elementos y la tecnología más confidenciales. Administrados por el Departamento de Estado de Los Estados Unidos, imponen controles sobre la exportación, importación temporal, reexa exportación y transferencia de muchos elementos de inteligencia, defensa e inteligencia (también conocidos como "artículos de defensa"), incluidos los datos técnicos relacionados.

## <a name="resources"></a>Recursos

- [Exportación de productos de Microsoft: Información general](https://www.microsoft.com/exporting/overview.aspx)
- [Exportación de productos de Microsoft: preguntas más frecuentes](https://www.microsoft.com/exporting/faq.aspx)
- [Exportación de productos de Microsoft: búsqueda de productos](https://www.microsoft.com/exporting/exporting-information.aspx)
- [Restricciones de exportación en criptografía](/windows/uwp/security/export-restrictions-on-cryptography)
- [Microsoft y FIPS 140-2](offering-fips-140-2.md)
- [Microsoft e ITAR](offering-itar.md)
- [Cumplimiento en el Centro de Confianza de Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
