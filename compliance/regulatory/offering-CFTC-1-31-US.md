---
title: Regla 1.31(c-d) de la Comisión de Comercio de Futuros de Mercancías (CFTC) de Estados Unidos
description: Una empresa de evaluación independiente validó que Azure y Office 365 pueden ayudar a las empresas financieras a cumplir con los requisitos de retención de registros y almacenamiento inmutable de la regla CFTC 1.31.
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
ms.openlocfilehash: 474cd04d98dc91668e48d1999f4fbd91d81523ec
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121759"
---
# <a name="commodity-futures-trading-commission-cftc-rule-131c-d-united-states"></a>Regla 1.31(c-d) de la Comisión de Comercio de Futuros de Mercancías (CFTC) de Estados Unidos

## <a name="about-cftc-rule-13c-d"></a>Acerca de la regla 1.3(c-d) de CFTC

La Comisión de Comercio de Futuros de [Mercancías](https://www.cftc.gov/) (CFTC), una agencia federal independiente de Estados Unidos, regula los mercados de opciones y futuros de productos y, más recientemente, el mercado de intercambios.  
  
La regla 1.31 de cftc de larga duración define los requisitos de retención de registros establecidos por la regla 17a-4(f) de la SEC. Además, especifica que los registros electrónicos deben mantenerse durante cinco años y que los originales se mantengan "fácilmente accesibles" durante los dos primeros años y que estén disponibles para su inspección por parte de la Comisión o el Departamento de Investigación de los Estados Unidos durante todo el período de retención.  
  
En 2017, la [CFTC](https://www.cftc.gov/sites/default/files/idc/groups/public/@lrfederalregister/documents/file/2017-11014a.pdf)revisó su regla, modificando y modernizando su reglamento de mantenimiento de registros para adoptar estándares menos prescriptivos y basados en principios que proporcionan mayor flexibilidad en el mantenimiento de los registros. Esta revisión hace que la regla sea más neutral en cuanto a tecnología, lo que permite a las entidades reguladas elegir la tecnología más adecuada para su negocio, a la vez que se mantienen las medidas de seguridad que "garantizan la confiabilidad del proceso de mantenimiento de registros". La regla revisada elimina el requisito de que las organizaciones conserven los registros originales durante dos años, pero conserva el período de mantenimiento de cinco años, que armonice las prácticas para las empresas reguladas por la CFTC y la SEC.

## <a name="microsoft-and-cftc-rule-131c-d"></a>Regla 1.31(c-d) de Microsoft y CFTC

Los clientes de servicios financieros, que representan una de las industrias más reguladas del mundo, están sujetos a disposiciones complejas como la retención de transacciones financieras y las comunicaciones relacionadas en un estado no modificable y no modificable. Uno de los más prescriptivos es la regla 1.31 de la Comisión de Comercio de Futuros de Mercancías (CFTC) de Estados Unidos que estipula requisitos estrictos para las entidades reguladas que optan por conservar libros y registros en medios de almacenamiento electrónico. Los registros almacenados deben ser a prueba de manipulaciones sin la capacidad de modificarlos o eliminarlos hasta después del período de retención designado. El almacenamiento de blobs inmutable de Microsoft Azure con bloqueo de directivas y Microsoft Office 365 con bloqueo de conservación puede ayudar a las instituciones financieras a cumplir los requisitos de almacenamiento de la regla 1.31(c-d) de CFTC.

### <a name="microsoft-azure"></a>Microsoft Azure

Para evaluar el cumplimiento de Azure con la regla 1.31(c-d) de CFTC, Microsoft retuvo una empresa de evaluación independiente especializada en la administración de registros y el gobierno de la información, Cohasset Associates. En el informe resultante, [CFTC 1.31 (c)–(d)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)Evaluación de cumplimiento: Microsoft Azure Storage , Cohasset validó que [Azure Immutable Blob Storage](/azure/storage/blobs/storage-blob-immutable-storage) con la opción bloqueo de directiva, cuando se usa para conservar blobs basados en tiempo en un formato que no se puede borrar ni reescribir (WORM), cumple los requisitos basados en principios de la regla CFTC. Cada blob (registro) está protegido para que no se modifique, sobrescriba o elimine hasta que haya expirado el período de retención requerido y se hayan liberado las retenciones legales asociadas. Los proveedores de software y asociados con cargas de trabajo confidenciales ahora pueden confiar en Azure Immutable Blob Storage como una solución en la nube de un solo uso para la retención de registros. Las instituciones financieras ahora pueden crear sus propias aplicaciones aprovechando estas características mientras permanecen conformes.

### <a name="microsoft-365"></a>Microsoft 365

Para los requisitos de [CFTC 1.31(c)-(d),](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) Cohasset validó que Microsoft 365 incluye características de archivado que permiten a los clientes regulados, incluidos los agentes de bolsa, almacenar datos de manera que les ayude a cumplir con los requisitos de la SEC para la retención de registros. Las características de retención de Microsoft 365 ayudan a conservar una amplia gama de datos, como correo electrónico, correo de voz, documentos compartidos, mensajes instantáneos y datos de terceros. En particular, el archivado en Microsoft 365 permite a los clientes establecer directivas de retención de mensajería globales o granulares para almacenar datos durante un período definido y posteriores en un formato que no se puede reescribir y que no se puede borrar.

## <a name="microsoft-in-scope-cloud-services"></a>Servicios de la nube dentro del alcance de Microsoft

- [Azure](https://aka.ms/AzureCompliance)
- [Office 365](https://aka.ms/o365-compliance-framework)

## <a name="audits-reports-and-certificates"></a>Auditorías, informes y certificados

[Regla 1.31 de CFTC de Azure &: SEC 17a-4(f) & CFTC 1.31(c-d) Evaluación del cumplimiento de Azure Storage

[Office 365 & regla 1.31 de CFTC: archivado en Office 365, retención de datos y cumplimiento de la regla 17a-4 de la SEC

## <a name="how-to-implement"></a>Cómo se debe implementar

- [Regulación de servicios financieros:](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)mapa de cumplimiento de los principios normativos clave de Estados Unidos para informática en la nube y servicios en línea de Microsoft.
- [Guía de cumplimiento y evaluación de riesgos](https://aka.ms/RiskGovernanceGuide): Cree un modelo de gobierno para la evaluación de riesgos de los servicios en la nube de Microsoft y las notificaciones reglamentarias.
- [Casos de uso financiero](/azure/industry/financial/): información general de casos de uso, tutoriales y otros recursos para crear soluciones de Azure para servicios financieros.

## <a name="resources"></a>Recursos

- [Programa de cumplimiento de servicios financieros de Microsoft](https://aka.ms/FSCP-Print)
- [Servicios financieros y servicios empresariales en la nube de Microsoft](https://www.microsoft.com/trustcenter/cloudservices/financialservices)
- [Cumplimiento de los servicios financieros en Azure](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Microsoft Office de retención de 365](/office365/securitycompliance/retention-policies)
- [Blog de servicios financieros de Microsoft](https://techcommunity.microsoft.com/t5/Financial-Services-Blog/bg-p/FinancialServicesBlog)
- [Cumplimiento en el Centro de Confianza de Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
