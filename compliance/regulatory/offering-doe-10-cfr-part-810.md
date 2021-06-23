---
title: US DoE 10 CFR Part 810
description: Los clientes sujetos a los requisitos de control de exportación de us DoE 10 CFR Parte 810 pueden usar Azure Government.
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
ms.openlocfilehash: 1a16495f5cfe3e293910ebe84e6af566aea17621
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/23/2021
ms.locfileid: "53087549"
---
# <a name="us-doe-10-cfr-part-810"></a>US DoE 10 CFR Part 810

## <a name="microsoft-and-doe-10-cfr-part-810"></a>Parte 810 de CFR de Microsoft y DoE 10

Microsoft Azure El gobierno puede ayudar a dar soporte a los clientes sujetos a los requisitos de control de exportación del Departamento de Energía de Estados Unidos (DoE) 10 CFR Parte 810 a través de dos autorizaciones:

- La autorización provisional alta de FedRAMP para operar (P-ATO) emitida por la Junta de autorización conjunta (JAB)
- Las autorizaciones provisionales de nivel 4 y 5 de la Agencia de sistemas de información del Departamento de Defensa (DoD)

FedRAMP ofrece una línea base adecuada para proporcionar garantías de que Azure Government ofrece infraestructura principal y tecnologías y servicios de virtualización, como computación, almacenamiento y redes diseñados con estrictos controles NIST. Estas ayudan a cumplir los requisitos de separación de datos de clientes y a habilitar conexiones seguras a los entornos locales de los clientes.

Además, Azure Government es una nube de la comunidad gubernamental de Estados Unidos que está físicamente separada de la nube de Azure. Proporciona garantías adicionales con respecto a requisitos específicos de filtrado de antecedentes por parte del gobierno de Estados Unidos, incluidos controles específicos que restringen el acceso a la información y los sistemas a los ciudadanos estadounidenses en pruebas entre el personal de operaciones de Azure.

## <a name="microsoft-in-scope-cloud-services"></a>Servicios en la nube de Microsoft en el ámbito

- [Azure Government](https://aka.ms/AzureCompliance)
- Intune

## <a name="how-to-implement"></a>Cómo se debe implementar

- [Nerc Cip Standards & Cloud Computing:](https://aka.ms/AzureNERC)Guía para las utilidades eléctricas y las entidades registradas que implementan cargas de trabajo en Azure o Azure Government.

## <a name="about-doe-10-cfr-part-810"></a>Acerca de DoE 10 CFR Parte 810

El reglamento de control de exportación [10 CFR parte 810](https://www.govinfo.gov/content/pkg/FR-2015-02-23/pdf/2015-03479.pdf) del Departamento de Energía (DoE) de Estados Unidos rige la exportación de tecnología y asistencia no clasificados de la energía nuclear. Ayuda a garantizar que las tecnologías nucleares exportadas desde Estados Unidos solo se usarán con fines pacíficos. La parte revisada 810 (regla final) surte efecto en marzo de 2015 y es administrada por la Administración Nacional [de Seguridad Nuclear](https://www.energy.gov/nnsa/national-nuclear-security-administration). La sección 810.6 indica que se requiere una autorización específica del DoE tanto para las disposiciones de asistencia como para las transferencias de tecnologías nucleares confidenciales que están "generalmente autorizadas", así como para aquellas que requieren una autorización específica (por ejemplo, para la asistencia con tecnologías nucleares confidenciales como el enriquecimiento y la producción de agua pesada).

## <a name="frequently-asked-questions"></a>Preguntas frecuentes

**¿Se aplican los 10 reglamentos cfr parte 110 de la Comisión reguladora de la energía nuclear de Estados Unidos a Azure Government?**

No. La [Comisión de Reglamentación Nuclear](https://www.nrc.gov/) de [](https://www.nrc.gov/about-nrc/ip/export-import.html) estados Unidos (NRC) regula la exportación e importación de instalaciones nucleares y equipos y materiales relacionados en virtud de [10 CFR Parte 110](https://www.nrc.gov/reading-rm/doc-collections/cfr/part110/). El NRC no regula la tecnología y la asistencia nuclear relacionadas con estos elementos que están bajo la jurisdicción del DoE. Por lo tanto, las regulaciones de NRC 10 CFR Parte 110 no se aplicarían a Azure Government.

**¿Cómo puedo proporcionar pruebas de que estoy cumpliendo con doE 10 CFR Parte 810?**

Si su organización está implementando datos en Azure Government, puede confiar en el FedRAMP high P-ATO de Azure Government como prueba de que está administrando los datos de forma restringida adecuadamente. Sin embargo, usted es responsable de obtener la autorización doE de sus propios sistemas, incluido el uso de servicios en la nube.

**¿Cuáles son mis responsabilidades para clasificar los datos implementados en Azure Government?**

Los clientes que implementan datos en Azure Government son responsables de su propio proceso de clasificación de seguridad. Para los datos de clientes sujetos a controles de exportación doE, el sistema de clasificación se aumenta con los controles de información nuclear controlada sin clasificar (UCNI) establecidos en la sección 148 de la [Ley](https://www.epa.gov/laws-regulations/summary-atomic-energy-act)de energía atómica de estados Unidos .

## <a name="resources"></a>Recursos

- [Azure Cloud Services y controles de exportación de EE. UU.](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)
- [Microsoft y FedRAMP](offering-fedramp.md)
- [Microsoft y DoD](offering-dod-disa-l2-l4-l5.md)
- [Nube de Microsoft para la Administración Pública](https://www.microsoft.com/enterprise/government)
- [Cumplimiento normativo en el Centro de confianza de Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
