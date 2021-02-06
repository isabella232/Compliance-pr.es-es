---
title: Regla 17a-4(f) de la Comisión de Bolsa y Valores (SEC) de Estados Unidos
description: Una empresa de evaluación independiente validó que Azure y Office 365 pueden ayudar a las empresas financieras a cumplir con la regla 17a-4(f) de la SEC que registra los requisitos de retención y almacenamiento inmutable.
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
ms.openlocfilehash: f877bbec76cc0d760f2f908975b3818b88551829
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121209"
---
# <a name="securities-and-exchange-commission-sec-rule-17a-4f-united-states"></a>Regla 17a-4(f) de la Comisión de Bolsa y Valores (SEC) de Estados Unidos

## <a name="about-sec-rule-17a-4f"></a>Acerca de la regla 17a-4(f) de la SEC

La [Us Securities and Exchange Commission (SEC)](https://www.sec.gov/) es una agencia independiente del gobierno federal de los Estados Unidos y el principal supervisor y regulador de los mercados de valores de Estados Unidos. Controla la autoridad de cumplimiento de las leyes federales de valores, propone nuevas reglas de valores y supervisa la regulación del mercado de la industria de valores.

La SEC define requisitos estrictos y explícitos para las entidades reguladas que optan por conservar libros y registros en medios de almacenamiento electrónico. Estableció [17 CFR 240.17a-3](https://www.govinfo.gov/app/details/CFR-2012-title17-vol3/CFR-2012-title17-vol3-sec240-17a-3) y [17 CFR 240.17a-4](https://www.ecfr.gov/cgi-bin/text-idx?mc=true&node=pt17.4.240&rgn=div5#se17.4.240_117a_64) para regular la contabilidad de registros, incluidos los períodos de retención, para agentes de bolsa de valores. Posteriormente, la [SEC](https://www.sec.gov/rules/interp/34-47806.htm) modificó 17 CFR 240.17a-4 párrafo (f), emitiendo dos versiones interpretativas expresamente para permitir que los libros y registros se conserven en medios de almacenamiento electrónico siempre que se cumplen ciertas condiciones.

Un sistema de almacenamiento electrónico cumple estas condiciones si impide la alteración o eliminación de registros durante el período de retención requerido. Los períodos de retención varían de tres a seis años en función de los tipos de registro, con la accesibilidad inmediata que se exige para los dos primeros años. Además, una de las versiones interpretativas requiere que el sistema de almacenamiento pueda conservar registros más allá del período de retención establecido por la SEC para cumplir con las citaciones, la suspensión legal u otros requisitos.

## <a name="microsoft-and-sec-rule-17a-4f"></a>Regla 17a-4(f) de Microsoft y la SEC

Los clientes de servicios financieros, que representan una de las industrias más reguladas del mundo, están sujetos a disposiciones complejas como la retención de transacciones financieras y las comunicaciones relacionadas en un estado no modificable y no modificable. Entre los más prescriptivos se encuentra la regla 17a-4(f) de la Comisión de Seguridad y Exchange (SEC) de Estados Unidos que estipula requisitos estrictos para las entidades reguladas que optan por conservar libros y registros en medios de almacenamiento electrónico. Los registros almacenados deben ser a prueba de manipulaciones sin la capacidad de modificarlos o eliminarlos hasta después del período de retención designado.

Microsoft Azure Immutable Blob Storage con bloqueo de directivas y Microsoft Office 365 con bloqueo de conservación pueden ayudar a las instituciones financieras a cumplir los requisitos de almacenamiento inmutables de la regla 17a-4(f) de la SEC.

Para evaluar el cumplimiento de Azure y Office 365 con la regla 17a-4(f) de la SEC, Microsoft retuvo una empresa de evaluación independiente especializada en la administración de registros y el gobierno de la información, Cohasset Associates. En el informe resultante para:

- **Azure**: SEC [17a-4(f)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)Evaluación de cumplimiento: Microsoft Azure Storage , Cohasset validó que [Azure Immutable Blob Storage](/azure/storage/blobs/storage-blob-immutable-storage) con la opción bloqueo de directiva, cuando se usa para conservar blobs basados en tiempo en un formato que no se puede borrar ni reescribir (WORM), cumple los requisitos de almacenamiento inmutable de la regla SEC. Cada blob (registro) está protegido para que no se modifique, sobrescriba o elimine hasta que haya expirado el período de retención requerido y se hayan liberado las retenciones legales asociadas. Los proveedores de software y asociados con cargas de trabajo confidenciales ahora pueden confiar en Azure Immutable Blob Storage como una solución en la nube de onestop-shop para la retención de registros y el almacenamiento inmutable. Las instituciones financieras ahora pueden crear sus propias aplicaciones aprovechando estas características mientras permanecen conformes.
- **Microsoft 365:** para los requisitos de la [SEC 17a-4(f),](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) Cohasset validó que Microsoft 365 incluye características de archivado que permiten a los clientes regulados, incluidos los agentes de bolsa, almacenar datos de manera que les ayude a cumplir con los requisitos de la SEC para la retención de registros. Las características de retención de Microsoft 365 ayudan a conservar una amplia gama de datos, incluidos el correo electrónico, el correo de voz, los documentos compartidos, los mensajes instantáneos y los datos de terceros. En particular, el archivado en Microsoft 365 permite a los clientes establecer directivas de retención de mensajería globales o granulares para almacenar datos durante un período definido y posteriores en un formato que no se puede reescribir y que no se puede borrar.

## <a name="microsoft-in-scope-cloud-services"></a>Servicios de la nube dentro del alcance de Microsoft

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="audits-reports-and-certificates"></a>Auditorías, informes y certificados

### <a name="azure--sec-rule-17"></a>Regla 17 & SEC de Azure

[SEC 17a-4(f) & evaluación de cumplimiento cftc 1.31 (c-d) de Azure Storage](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)

### <a name="office-365--sec-rule-17"></a>Regla 17 de & sec de Office 365

[Evaluación de cumplimiento sec 17a-4(f): Centro de seguridad de Microsoft & cumplimiento con SharePoint, OneDrive, Teams, Exchange y Skype Empresarial](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=9fa8349d-a0c9-47d9-93ad-472aa0fa44ec&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

## <a name="how-to-implement"></a>Cómo se debe implementar

### <a name="financial-services-regulation"></a>Regulación de servicios financieros

Mapa de cumplimiento de los principios normativos clave de Estados Unidos para informática en la nube y servicios en línea de Microsoft. [Más información](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)

### <a name="risk-assessment--compliance-guide"></a>Guía de cumplimiento & evaluación de riesgos

Crear un modelo de gobierno para la evaluación de riesgos de los servicios en la nube de Microsoft y la notificación regulatoria. [Más información](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

### <a name="financial-use-cases"></a>Casos de uso financiero

Use información general sobre casos, tutoriales y otros recursos para crear soluciones de Azure para servicios financieros. [Más información](/azure/industry/financial/)

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Usar el Administrador de cumplimiento de Microsoft para evaluar el riesgo

[El Administrador de cumplimiento de Microsoft](/microsoft-365/compliance/compliance-manager) es una característica en el [Centro de cumplimiento de Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) que le ayuda a entender la actitud de su organización en relación con el cumplimiento normativo y a tomar medidas para contribuir a reducir los riesgos. El Administrador de cumplimiento ofrece una plantilla premium para crear una evaluación de esta normativa. Busque la plantilla en la página **plantillas de evaluación** en el Administrador de cumplimiento. Obtenga información sobre cómo [crear evaluaciones en el Administrador de cumplimiento](/microsoft-365/compliance/compliance-manager-assessments).

## <a name="resources"></a>Recursos

- [Archivado en Microsoft Office 365, retención de datos y regla 17a-4](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)
- [Cumplimiento de los Servicios Financieros de Microsoft](https://download.microsoft.com/download/6/4/7/64707E3E-6D3E-45D0-8207-A0EA3201B4A6/Microsoft%20Cloud%20-%20Financial%20Services%20Compliance%20Program%20\(Print\).pdf)
- [Servicios financieros y servicios financieros del Programa de cumplimiento empresarial de Microsoft](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Cumplimiento de los servicios financieros en Azure](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Herramienta de evaluación de riesgos en la nube para servicios financieros de Azure](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint?command=Download&downloadType=Document&downloadId=079a1973-711a-428f-9312-9ddd290cff7b&docTab=c726d5c0-2d1e-11e8-a485-57140ec19669_PaaS)
- [Microsoft Office de retención de 365](/office365/securitycompliance/retention-policies)
- [Comunidad de servicios financieros de Microsoft](https://techcommunity.microsoft.com/t5/financial-services/ct-p/FinancialServices)
- [Cumplimiento en el Centro de Confianza de Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
