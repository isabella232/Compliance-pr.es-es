---
title: Us Export Administration Regulations (EAR)
description: Los servicios en la nube de Microsoft ayudan a los clientes sujetos a los Reglamentos de administración de exportación (EAR) estadounidenses a cumplir sus requisitos de cumplimiento y a administrar el riesgo de control de exportación.
keywords: Cumplimiento y ofertas de Microsoft 365
ms.localizationpriority: medium
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
ms.openlocfilehash: 859067495b6811b2264ab3a379f305d428771bce
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2021
ms.locfileid: "58948245"
---
# <a name="us-export-administration-regulations-ear"></a>Us Export Administration Regulations (EAR)

## <a name="about-the-ear"></a>Acerca del EAR

El Departamento de Comercio de Estados Unidos aplica el Reglamento de administración de exportación (EAR) a través de la Oficina de [Industria y Seguridad (BIS).](https://www.bis.doc.gov/) La EAR gobierna e impone controles sobre la exportación y reexa exportación de la mayoría de los productos comerciales, software y tecnología, incluidos los elementos de "doble uso" que se pueden usar con fines comerciales y militares y determinados elementos de defensa.

La guía de BIS contiene que, cuando los datos o el software se cargan en la nube o se transfieren entre nodos de usuario, el cliente, no el proveedor de nube, es el "exportador" que tiene la responsabilidad de garantizar que las transferencias, el almacenamiento y el acceso a los datos o software cumplan con el EAR.

[Según el BIS,](https://www.bis.doc.gov/index.php/documents/regulation-docs/412-part-734-scope-of-the-export-administration-regulations/file)la exportación hace referencia a la transferencia de tecnología protegida o datos técnicos a un destino extranjero o su liberación a una persona extranjera en los Estados Unidos (también denominada exportación considerada *).*  La EAR rige ampliamente:

- Exportaciones de Los Estados Unidos.
- Vuelve a exportar o retransferir elementos de origen estadounidense y determinados elementos de origen extranjero con más de una parte *de minimis* de contenido de origen estadounidense.
- Transferencias o divulgaciones a personas de otros países.

Los elementos sujetos al EAR se pueden encontrar en la Lista de controles de comercio (CCL), donde a cada elemento se le asigna un número de clasificación de control de exportación [(ECCN)](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn)único. Los elementos que no aparecen en el CCL se designan como EAR99 y la mayoría de los productos comerciales de EAR99 no requerirán una licencia para exportarse. Sin embargo, según el destino, el usuario final o el uso final del elemento, incluso un elemento EAR99 puede requerir una licencia de exportación de BIS.

La regla [final,](https://www.federalregister.gov/documents/2016/06/03/2016-12734/revisions-to-definitions-in-the-export-administration-regulations)publicada en junio de 2016, aclaró que los requisitos de licencias EAR tampoco se aplicarían a la transmisión y almacenamiento de datos técnicos y software no clasificados si estaban cifrados de extremo a extremo mediante módulos criptográficos validados por FIPS 140-2 y no se almacenaban intencionadamente en un país con embargo militar ni en la Federación de Rusia.

## <a name="microsoft-and-the-ear"></a>Microsoft y ear

Las tecnologías, productos y servicios de Microsoft están sujetos al Reglamento de administración de exportación (EAR) de Estados Unidos. Aunque no hay ninguna certificación de cumplimiento para ear, Microsoft Azure, Microsoft Azure Government y Microsoft Office 365 Government (entornos GCCHigh y DoD) ofrecen características y herramientas importantes para ayudar a los clientes elegibles sujetos a la EAR a administrar los riesgos de control de exportación y cumplir sus requisitos de cumplimiento.

El Departamento de Comercio de Estados Unidos, que aplica el EAR, ha tomado la posición de que los clientes, no los proveedores de servicios en la nube como Microsoft, se consideran exportadores de sus propios datos de clientes. Aunque la mayoría de los datos de clientes no se considera "tecnología" o "datos técnicos" sujetos a los controles de exportación de EAR, los servicios en la nube de Microsoft en el ámbito se estructuran para ayudar a los clientes a administrar y mitigar significativamente los posibles riesgos de control de exportación a los que se enfrentan. Microsoft generalmente, pero no exclusivamente, recomienda el uso de sus servicios en la nube gubernamentales para clientes elegibles. Con la planeación adecuada, los clientes pueden usar las siguientes herramientas y sus propios procedimientos internos para ayudar a garantizar el cumplimiento total de los controles de exportación de Estados Unidos.

- **Controles en la ubicación de datos**. Los clientes tienen visibilidad de dónde se almacenan sus datos y acceso a herramientas sólidas para restringir su almacenamiento. Por lo tanto, pueden asegurarse de que sus datos se almacenan en los Estados Unidos y minimizar la transferencia de tecnología controlada o datos técnicos fuera de los Estados Unidos. Además, los datos de los clientes no se almacenan en una ubicación no conforme, de acuerdo con las prohibiciones de EAR en las que los datos se almacenan "intencionadamente": ningún centro de datos de Azure se encuentra en ninguno de los 25 países del grupo D:5 ni en la Federación de Rusia.
- **Cifrado de extremo a extremo**. Al aprovechar el puerto seguro de cifrado de extremo a extremo para las ubicaciones de almacenamiento físico especificadas en el EAR, los servicios en la nube de Microsoft en el ámbito ofrecen características de cifrado que pueden ayudar a proteger contra riesgos de control de exportación. También ofrecen a los clientes una [amplia](https://aka.ms/Azure-Encryption-Overview) variedad de opciones para cifrar datos en tránsito y en reposo, y la flexibilidad para elegir entre las opciones de cifrado.
- **Herramientas y protocolos para evitar la exportación no autorizada.** El uso del cifrado también ayuda a proteger contra una posible exportación (o se considera una reex exportación) en el EAR, ya que incluso si una persona que no es estadounidense tiene acceso a datos cifrados, no se revela nada si no puede leer o comprender los datos mientras está cifrado; por lo tanto, no hay "liberación" de datos controlados.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Servicios y plataformas en la nube dentro de Microsoft

- [Azure y Azure Government](https://aka.ms/AzureCompliance)
- [Office 365 Administración Pública (GCC-High y DoD)](https://aka.ms/Office-365-Export-Controls)
- Intune

## <a name="how-to-implement"></a>Cómo se debe implementar

Información general sobre los controles y las directrices de exportación de Estados Unidos para los clientes que evalúan sus obligaciones en virtud del EAR.

- [Azure](https://aka.ms/Azure-Export-Controls)
- [Office 365](https://aka.ms/Office-365-Export-Controls)

## <a name="frequently-asked-questions"></a>Preguntas más frecuentes

**¿Qué debo hacer para cumplir con los controles de exportación al usar los servicios en la nube de Microsoft?**

En ear, cuando los datos se cargan en un servidor en la nube como la nube de Microsoft, el cliente propietario de los datos , no el proveedor de servicios en la nube, se considera el exportador. Por este motivo, el propietario de los datos (es decir, el cliente de Microsoft) debe evaluar detenidamente cómo su uso de la nube de Microsoft puede implicar a los controles de exportación de Estados Unidos y determinar si alguno de los datos que desea usar o almacenar puede estar sujeto a controles EAR y, si es así, qué controles se aplican. Obtenga más información sobre cómo [azure](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers) [y Office 365](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE1s5kI) servicios en la nube pueden ayudar a los clientes a garantizar el cumplimiento total de los controles de exportación de Estados Unidos.

**¿Las tecnologías, productos y servicios de Microsoft están sujetos al EAR?**

La mayoría de las tecnologías, productos y servicios de Microsoft:

- No están sujetos al EAR y, por lo tanto, no están en la lista de control de comercio y no tienen ECCN;
- O bien son aptos para el mercado masivo de EAR99 o 5D992 para la autoclasificación de Microsoft y pueden exportarse a países sin embargo sin una licencia como Sin licencia requerida (NLR).

Dicho esto, a algunos productos de Microsoft se les ha asignado un ECCN que puede requerir o no una licencia. Consulte al EAR o al asesor legal para determinar el tipo de licencia adecuado y los países elegibles para fines de exportación.

**¿Cuál es la diferencia entre el EAR y el Reglamento de tráfico internacional de armas (ITAR)?**

Los principales controles de exportación de Estados Unidos con la aplicación más amplia son la EAR, administrada por el Departamento de Comercio de Estados Unidos. El EAR se aplica a los elementos de doble uso que tienen aplicaciones comerciales y militares, y a los elementos con aplicaciones puramente comerciales.

Los Estados Unidos también tienen reglamentos de control de exportación independientes y más especializados, como el ITAR, que rige los elementos y la tecnología más confidenciales. Administrados por el Departamento de Estado de Estados Unidos, imponen controles sobre la exportación, importación temporal, reexa exportación y transferencia de muchos elementos de inteligencia, defensa y militares (también conocidos como "artículos de defensa"), incluidos los datos técnicos relacionados.

## <a name="resources"></a>Resources

- [Exportación de productos de Microsoft: Información general](https://www.microsoft.com/exporting/overview.aspx)
- [Exportación de productos de Microsoft: Preguntas más frecuentes](https://www.microsoft.com/exporting/faq.aspx)
- [Exportación de productos de Microsoft: búsqueda de productos](https://www.microsoft.com/exporting/exporting-information.aspx)
- [Restricciones de exportación en criptografía](/windows/uwp/security/export-restrictions-on-cryptography)
- [Microsoft y FIPS 140-2](offering-fips-140-2.md)
- [Microsoft y ITAR](offering-itar.md)
- [Cumplimiento en el Centro de Confianza de Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
