---
title: Regla 4511(c) de la Autoridad Reguladora de la Industria Financiera (FINRA) de Los Estados Unidos
description: Una empresa de evaluación independiente validó que Azure y Office 365 pueden ayudar a las empresas financieras a cumplir los requisitos de retención de registros y almacenamiento inmutable de la regla FINRA 4511.
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
ms.openlocfilehash: f4a26a88ca742178d894b5e46d0372d91babba66
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120849"
---
# <a name="financial-industry-regulatory-authority-finra-rule-4511c-united-states"></a>Regla 4511(c) de la Autoridad Reguladora de la Industria Financiera (FINRA) de Los Estados Unidos

## <a name="about-finra-rule-4511"></a>Acerca de la regla 4511 de FINRA

La Autoridad Reguladora de la Industria Financiera [(FINRA)](https://www.finra.org/#/) es el organismo independiente más grande que regula las empresas de valores con supervisión de más de 4500 empresas de corretaje en los Estados Unidos. Fue autorizado por el Gobierno de Ee. UU. "para proteger a los inversores de Estados Unidos asegurándose de que la industria de negociación opera de manera razonable y con sinceridad".

En 2011, la Comisión de Seguridad y Exchange (SEC) de los Estados Unidos aprobó la adopción de las reglas de la SEC que rigen la retención de libros y registros en medios de almacenamiento electrónico. La Regla [4511(c)](https://www.finra.org/sites/default/files/NoticeDocument/p123548.pdf) de FINRA especifica que "todos los libros y registros necesarios para realizarse en virtud de las reglas finra se conservarán en un formato y medios que cumplan con la regla 17a-4 de la SEA (Ley de intercambio de valores bursáarios)."

Además, la regla 4511(c) de FINRA requiere que las empresas conserven durante un período de al menos seis años aquellos libros y registros para los que no haya un período de retención especificado en las reglas DE FINRA o SEA aplicables. De hecho, si los libros y registros pertenecen a una cuenta, se exige que el período de retención sea de seis años después del cierre de la cuenta. De lo contrario, el período de retención es de seis años después de crear dichos libros y registros.

## <a name="microsoft-and-finra-rule-4511c"></a>Regla 4511(c) de Microsoft y FINRA

Los clientes de servicios financieros, que representan una de las industrias más reguladas del mundo, están sujetos a disposiciones complejas como la retención de transacciones financieras y las comunicaciones relacionadas en un estado no modificable y no modificable. Entre ellas se encuentra la regla 4511 de la Autoridad Reguladora de la Industria Financiera (FINRA) que estipula requisitos estrictos para las entidades reguladas que optan por conservar libros y registros en medios de almacenamiento electrónico. Los registros almacenados deben ser a prueba de manipulaciones sin la capacidad de modificarlos o eliminarlos hasta después del período de retención designado.

El almacenamiento de blobs inmutable de Microsoft Azure con bloqueo de directivas y Microsoft Office 365 con bloqueo de conservación puede ayudar a las instituciones financieras a cumplir los requisitos de almacenamiento inmutables de la regla 4511(c) de FINRA.

## <a name="microsoft-azure"></a>Microsoft Azure

Para evaluar el cumplimiento de Azure con la regla 4511(c) de FINRA, Microsoft retuvo una empresa de evaluación independiente especializada en la administración de registros y el gobierno de la información, Cohasset Associates. El informe resultante, [SEC 17a-4(f) & CFTC 1.31 (c-d) Compliance Assessment: Microsoft Azure Storage](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports), abarca el cumplimiento de Azure con la regla 4511(c) de FINRA, que aplaza los requisitos de formato y medios de la regla 17a-4(f) de la SEC.

Cohasset validó que [Azure Immutable Blob Storage](/azure/storage/blobs/storage-blob-immutable-storage) con la opción de bloqueo de directivas, cuando se usa para conservar blobs basados en tiempo en un formato que no se puede borrar y no se puede reescribir (WORM), cumple los requisitos de almacenamiento de FINRA relevantes. Cada blob (registro) está protegido para que no se modifique, sobrescriba o elimine hasta que haya expirado el período de retención requerido y se hayan liberado las retenciones legales asociadas.

Los proveedores de software y asociados con cargas de trabajo confidenciales ahora pueden confiar en Azure Immutable Blob Storage como una solución en la nube de una sola tienda para la retención de registros y el almacenamiento inmutable. Las instituciones financieras ahora pueden crear sus propias aplicaciones aprovechando estas características mientras permanecen conformes.

## <a name="microsoft-365"></a>Microsoft 365

Para los requisitos de la regla [4511(c) de FINRA,](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) Cohasset validó que Microsoft 365 incluye características de archivado que permiten a los clientes regulados, incluidos los agentes de bolsa, almacenar datos de manera que les ayude a cumplir con los requisitos de la SEC para la retención de registros. Las características de retención de Microsoft 365 ayudan a conservar una amplia gama de datos, como correo electrónico, correo de voz, documentos compartidos, mensajes instantáneos y datos de terceros. En particular, el archivado en Microsoft 365 permite a los clientes establecer directivas de retención de mensajería globales o granulares para almacenar datos durante un período definido y posteriores en un formato que no se puede reescribir y que no se puede borrar.

## <a name="microsoft-in-scope-cloud-services"></a>Servicios de la nube dentro del alcance de Microsoft

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="audits-reports-and-certificates"></a>Auditorías, informes y certificados

### <a name="azure--finra-rule-4511c"></a>Regla 4511(c) de Azure & FINRA

[SEC 17a-4(f) & evaluación de cumplimiento cftc 1.31 (c-d) de Azure Storage](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)

### <a name="office-365--finra-rule-4511c"></a>Office 365 & finra regla 4511(c)

[Archivado en Office 365, retención de datos y cumplimiento de la regla SEC 17a-4](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)

## <a name="how-to-implement"></a>Cómo se debe implementar

- **Regulación de servicios financieros:** mapa de cumplimiento de los principios normativos clave de Estados Unidos para informática en la nube y servicios en línea de Microsoft. [Más información](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- **Guía de cumplimiento y evaluación de riesgos**: Cree un modelo de gobierno para la evaluación de riesgos de los servicios en la nube de Microsoft y las notificaciones reglamentarias. [Más información](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)
- **Casos de uso financiero**: información general de casos de uso, tutoriales y otros recursos para crear soluciones de Azure para servicios financieros. [Más información](/azure/industry/financial/)

## <a name="resources"></a>Recursos

- [Programa de cumplimiento de servicios financieros de Microsoft](https://download.microsoft.com/download/6/4/7/64707E3E-6D3E-45D0-8207-A0EA3201B4A6/Microsoft%20Cloud%20-%20Financial%20Services%20Compliance%20Program%20\(Print\).pdf)
- [Servicios financieros y servicios empresariales en la nube de Microsoft](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Cumplimiento de los servicios financieros en Azure](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Herramienta de evaluación de riesgos en la nube para servicios financieros de Azure](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint?command=Download&downloadType=Document&downloadId=079a1973-711a-428f-9312-9ddd290cff7b&docTab=c726d5c0-2d1e-11e8-a485-57140ec19669_PaaS)
- [Microsoft Office de retención de 365](/office365/securitycompliance/retention-policies)
- [Blog de servicios financieros de Microsoft](https://techcommunity.microsoft.com/t5/Financial-Services-Blog/bg-p/FinancialServicesBlog)
- [Cumplimiento en el Centro de Confianza de Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
