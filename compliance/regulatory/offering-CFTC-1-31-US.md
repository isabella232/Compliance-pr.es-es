---
title: Regla 1.31(c-d) de la Comisión de Negociación de Futuros de Materias Primas (CFTC) Estados Unidos
description: Una firma de evaluación independiente validó que Azure y Office 365 pueden ayudar a las empresas financieras a cumplir con los requisitos de retención de registros y almacenamiento inmutable de la Regla 1.31 de CFTC.
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
ms.openlocfilehash: 903f4d3db8965fdcd8c96a8d474e5180430b4966e4adc6945315f283ddbc0d3f
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292587"
---
# <a name="commodity-futures-trading-commission-cftc-rule-131c-d-united-states"></a>Regla 1.31(c-d) de la Comisión de Negociación de Futuros de Materias Primas (CFTC) Estados Unidos

## <a name="about-cftc-rule-13c-d"></a>Acerca de la regla 1.3(c-d) de CFTC

La [Comisión de Negociación](https://www.cftc.gov/) de Futuros de Materias Primas (CFTC), una agencia federal independiente de Estados Unidos, regula los mercados de futuros y opciones de materias primas y, más recientemente, el mercado de intercambios.  
  
La regla 1.31 de CFTC de larga duración define los requisitos de retención de registros establecidos por la Regla 17a-4(f) de la SEC. Además, especifica que los registros electrónicos deben mantenerse durante cinco años y que los originales se mantengan "fácilmente accesibles" durante los dos primeros años y estén disponibles para su inspección por la Comisión o el Departamento de Justicia de los Estados Unidos durante todo el período de retención.  
  
En 2017, la [CFTC](https://www.cftc.gov/sites/default/files/idc/groups/public/@lrfederalregister/documents/file/2017-11014a.pdf)revisó su regla, modificando y modernizando su reglamento de mantenimiento de registros para adoptar estándares menos prescriptivos y basados en principios que proporcionan una mayor flexibilidad en la forma en que se pueden mantener los registros. Esta revisión hace que la regla sea más neutral en cuanto a tecnología, lo que permite a las entidades reguladas elegir la tecnología más adecuada para su negocio, al tiempo que se mantienen las garantías que "garantizan la confiabilidad del proceso de registro". La regla revisada elimina el requisito de que las organizaciones mantengan los registros originales durante dos años, pero conserva el período de mantenimiento de cinco años, que armoniza las prácticas de las empresas reguladas por la CFTC y la SEC.

## <a name="microsoft-and-cftc-rule-131c-d"></a>Regla 1.31(c-d) de Microsoft y CFTC

Los clientes de servicios financieros, que representan una de las industrias más reguladas del mundo, están sujetos a disposiciones complejas como la retención de transacciones financieras y la comunicación relacionada en un estado no modificable y no modificable. Una de las más prescriptivas es la Regla 1.31 de la Comisión de Negociación de Futuros de Materias Primas (CFTC) de Estados Unidos, que estipula requisitos estrictos para las entidades reguladas que optan por conservar libros y registros en medios de almacenamiento electrónico. Los registros almacenados deben ser a prueba de manipulaciones sin capacidad para modificarlos o eliminarlos hasta después del período de retención designado. Microsoft Azure Los blobs inmutables Storage bloqueo de directivas y Microsoft Office 365 con bloqueo de conservación pueden ayudar a las instituciones financieras a cumplir los requisitos de almacenamiento de la regla 1.31(c-d) de CFTC.

### <a name="microsoft-azure"></a>Microsoft Azure

Para evaluar el cumplimiento de Azure con la regla 1.31(c-d) de CFTC, Microsoft conservó una firma de evaluación independiente especializada en administración de registros y gobierno de la información, Cohasset Associates. En el informe resultante, [CFTC 1.31 (c)–(d) Evaluación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)del cumplimiento: Microsoft Azure Storage , Cohasset validó que [Azure Immutable Blob Storage](/azure/storage/blobs/storage-blob-immutable-storage) con la opción Bloqueo de directivas, cuando se usa para retener blobs basados en tiempo en un formato no eliminable y no reescribible (WORM), cumple los requisitos basados en principios de la regla CFTC. Cada blob (registro) está protegido para que no se modifique, sobrescriba o elimine hasta que haya expirado el período de retención requerido y se hayan liberado las retenciones legales asociadas. Los proveedores de software y asociados con cargas de trabajo confidenciales ahora pueden confiar en Azure Immutable Blob Storage como una solución en la nube de tienda única para la retención de registros. Las instituciones financieras ahora pueden crear sus propias aplicaciones aprovechando estas características mientras se mantienen conformes.

### <a name="microsoft-365"></a>Microsoft 365

Para los requisitos [cftc 1.31(c)-(d),](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) Cohasset validó que Microsoft 365 incluye características de archivado que permiten a los clientes regulados, incluidos los agentes de corretaje, almacenar datos de una manera que les ayude a cumplir con los requisitos de sec para la retención de registros. Las características de retención Microsoft 365 ayudan a conservar una amplia variedad de datos, incluidos el correo electrónico, el correo de voz, los documentos compartidos, los mensajes instantáneos y los datos de terceros. En particular, el archivado en Microsoft 365 permite a los clientes establecer directivas de retención de mensajería globales o granulares para almacenar datos durante un período definido y más allá en un formato no reescribible y no eliminable.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Servicios y plataformas en la nube dentro de Microsoft

- [Azure](https://aka.ms/AzureCompliance)
- [Office 365](https://aka.ms/o365-compliance-framework)

## <a name="audits-reports-and-certificates"></a>Auditorías, informes y certificados

[Regla 1.31 de CFTC de Azure &: SEC 17a-4(f) & CFTC 1.31(c-d) Evaluación del cumplimiento de Azure Storage

[Office 365 & regla 1.31 de CFTC: archivado en Office 365, retención de datos y cumplimiento de la regla 17a-4 de la SEC

## <a name="how-to-implement"></a>Cómo se debe implementar

- [Regulación de servicios financieros:](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)mapa de cumplimiento de los principios normativos clave de Estados Unidos para la informática en la nube y los servicios en línea de Microsoft.
- [Guía de cumplimiento y evaluación de riesgos](https://aka.ms/RiskGovernanceGuide): Cree un modelo de gobierno para la evaluación de riesgos de los servicios en la nube de Microsoft y las notificaciones reglamentarias.
- [Casos de uso de servicios financieros](/azure/industry/financial/): Use visiones generales sobre los casos, tutoriales u otros recursos para compilar soluciones de Azure para servicios financieros.

## <a name="resources"></a>Recursos

- [Programa de cumplimiento de servicios financieros de Microsoft](https://aka.ms/FSCP-Print)
- [Servicios financieros y servicios empresariales en la nube de Microsoft](https://www.microsoft.com/trustcenter/cloudservices/financialservices)
- [Cumplimiento de los servicios financieros en Azure](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Microsoft Office 365 Directivas de retención](/office365/securitycompliance/retention-policies)
- [Blog de servicios financieros de Microsoft](https://techcommunity.microsoft.com/t5/Financial-Services-Blog/bg-p/FinancialServicesBlog)
- [Cumplimiento en el Centro de Confianza de Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
