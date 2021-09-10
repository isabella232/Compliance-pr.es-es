---
title: Regla 17a-4(f) de la Comisión de Valores Exchange (SEC) Estados Unidos
description: Una firma de evaluación independiente validó que Azure y Office 365 pueden ayudar a las empresas financieras a cumplir con los requisitos de retención de registros y almacenamiento inmutable de la regla 17a-4(f) de la SEC.
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
ms.openlocfilehash: 50c44b6801e15af02bf4bfa4f4d46758b7a6c7a8
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2021
ms.locfileid: "58948430"
---
# <a name="securities-and-exchange-commission-sec-rule-17a-4f-united-states"></a>Regla 17a-4(f) de la Comisión de Valores Exchange (SEC) Estados Unidos

## <a name="about-sec-rule-17a-4f"></a>Acerca de la regla 17a-4(f) de la SEC

La Comisión de valores y Exchange de Estados Unidos [(SEC)](https://www.sec.gov/) es una agencia independiente del gobierno federal de los Estados Unidos y el supervisor y regulador principal de los mercados de valores de Estados Unidos. Se encarga de la autoridad de cumplimiento de las leyes federales de valores, propone nuevas reglas de valores y supervisa la regulación del mercado de la industria de valores.

La SEC define requisitos rigurosos y explícitos para las entidades reguladas que optan por conservar libros y registros en medios de almacenamiento electrónico. Estableció [17 CFR 240.17a-3](https://www.govinfo.gov/app/details/CFR-2012-title17-vol3/CFR-2012-title17-vol3-sec240-17a-3) y [17 CFR 240.17a-4](https://www.ecfr.gov/cgi-bin/text-idx?mc=true&node=pt17.4.240&rgn=div5#se17.4.240_117a_64) para regular la conservación de registros, incluidos los períodos de retención, para los agentes de bolsa de valores. Más adelante, la [SEC](https://www.sec.gov/rules/interp/34-47806.htm) modificó 17 cfr 240.17a-4 párrafo (f), emitiendo dos versiones interpretativas expresamente para permitir que los libros y registros se conservarán en medios de almacenamiento electrónico siempre que se cumplen determinadas condiciones.

Un sistema de almacenamiento electrónico cumple esas condiciones si impide la alteración o eliminación de registros durante el período de retención requerido. Los períodos de retención varían de tres a seis años en función de los tipos de registro, con la accesibilidad inmediata de los dos primeros años. Además, una de las versiones interpretativas requiere que el sistema de almacenamiento sea capaz de retener registros más allá del período de retención establecido por la SEC para cumplir con citaciones, retención legal u otros requisitos de este tipo.

## <a name="microsoft-and-sec-rule-17a-4f"></a>Regla 17a-4(f) de Microsoft y sec

Los clientes de servicios financieros, que representan una de las industrias más reguladas del mundo, están sujetos a disposiciones complejas como la retención de transacciones financieras y la comunicación relacionada en un estado no modificable y no modificable. Entre las más prescriptivas se encuentra la Regla 17a-4(f) de la Comisión de Seguridad y Exchange de Estados Unidos (SEC), que estipula requisitos estrictos para las entidades reguladas que optan por conservar libros y registros en medios de almacenamiento electrónico. Los registros almacenados deben ser a prueba de manipulaciones sin capacidad para modificarlos o eliminarlos hasta después del período de retención designado.

Microsoft Azure Los blobs inmutables Storage bloqueo de directivas y Microsoft Office 365 con bloqueo de conservación pueden ayudar a las instituciones financieras a cumplir los requisitos de almacenamiento inmutables de la regla 17a-4(f) de la SEC.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Servicios y plataformas en la nube dentro de Microsoft

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="independent-assessments"></a>Evaluaciones independientes

Para evaluar el cumplimiento de Azure y Office 365 con la regla 17a-4(f) de la SEC, Microsoft conservó una firma de evaluación independiente especializada en administración de registros y gobierno de la información, Cohasset Associates.

### <a name="azure"></a>Azure

[El almacenamiento inmutable para Azure Blob Storage](/azure/storage/blobs/storage-blob-immutable-storage) permite a los usuarios almacenar registros críticos para la empresa en un estado de escritura una vez leídos muchos (WORM). Este estado hace que los datos no se pueden borrar y no se pueden modifican para un intervalo especificado por el usuario. Durante el intervalo de retención, los blobs se pueden crear y leer, pero no se pueden modificar ni eliminar. Estas características del almacenamiento inmutable de Azure pueden ayudar a los clientes a cumplir sus requisitos de retención de registros.

Microsoft retuvo una firma de evaluación independiente de terceros que se especializa en la administración de registros y el gobierno de la información para evaluar el almacenamiento inmutable para el cumplimiento del almacenamiento de blobs de Azure con los requisitos de la Regla 17a-4(f) de la SEC. El informe *[resultante Cohasset Assessment: Microsoft Azure WORM Storage](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)* está disponible para los clientes.

El evaluador opina que Azure Storage con la característica de almacenamiento inmutable  para *blobs* de Azure y la opción de directiva basada en tiempo bloqueada conserva blobs (registros) basados en tiempo en un formato no modificable y no modificable y cumple los requisitos de almacenamiento pertinentes de la Regla 17a-4(f), la Regla [FINRA 4511(c)](offering-FINRA-4511.md)y los requisitos basados en principios de la Regla [1.31(c)-(d)](offering-cftc-1-31-us.md)de CFTC .

A petición, Microsoft también proporcionará una carta de *90* días necesaria para cumplir los requisitos sec 17a-4(f)(2) para que los clientes notifiquen a su autoridad examinadora designada al menos 90 días antes de usar medios de almacenamiento electrónico. Como se indica en el reglamento, "el miembro, agente o distribuidor debe proporcionar su propia representación o una del proveedor de medios de almacenamiento u otro tercero con la experiencia adecuada para que el medio de almacenamiento seleccionado cumpla las condiciones establecidas en este párrafo (f)(2)." Para obtener la Certificación de *Microsoft* de Storage Media Services electrónico para la regla 17a-4 [](https://azure.microsoft.com/support/create-ticket/) de la SEC, los clientes con un plan de soporte técnico de [Azure](https://azure.microsoft.com/support/plans/) pueden crear un vale de soporte técnico en Azure Portal y solicitar la carta de atestación para la regla 17a-4 de la SEC. En este documento, Microsoft proporciona garantías relevantes para los requisitos de la SEC 17a-4(f)(2).

### <a name="office-365"></a>Office 365

Para los requisitos de [sec 17a-4(f),](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) Cohasset validó que Microsoft 365 incluye características de archivado que permiten a los clientes regulados, incluidos los agentes de corretaje, almacenar datos de una manera que les ayude a cumplir con los requisitos de la SEC para la retención de registros. Las características de retención Microsoft 365 ayudan a conservar una amplia variedad de datos, incluidos el correo electrónico, el correo de voz, los documentos compartidos, los mensajes instantáneos y los datos de terceros. En particular, el archivado en Microsoft 365 permite a los clientes establecer directivas de retención de mensajería globales o granulares para almacenar datos durante un período definido y más allá en un formato no reescribible y no eliminable.

## <a name="audits-reports-and-certificates"></a>Auditorías, informes y certificados

### <a name="azure--sec-rule-17"></a>Regla 17 & SEC de Azure

- [SEC 17a-4(f) & CFTC 1.31 (c-d) Evaluación del cumplimiento de Azure Storage](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)

Microsoft *Attestation of Electronic Storage Media Services* for SEC Rule 17a-4 can be requested by creating a support [ticket](https://azure.microsoft.com/support/create-ticket/) with [Azure support](https://azure.microsoft.com/support/plans/). En esta carta de atestación, Microsoft proporciona garantías para ayudar a los clientes a cumplir con los requisitos sec 17a-4(f)(2).

### <a name="office-365--sec-rule-17"></a>Office 365 & regla 17 de la SEC

- [Evaluación del cumplimiento sec 17a-4(f): Centro de cumplimiento de Microsoft Security & con SharePoint, OneDrive, Teams, Exchange y Skype Empresarial](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=2dc92867-5f83-49d8-ad04-9e7295c9e40e&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="how-to-implement"></a>Cómo se debe implementar

### <a name="financial-services-regulation"></a>Regulación de servicios financieros

Mapa de cumplimiento de los principios normativos clave de Estados Unidos para la informática en la nube y los servicios en línea de Microsoft. [Más información](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)

### <a name="risk-assessment--compliance-guide"></a>Guía de cumplimiento & de evaluación de riesgos

Cree un modelo de gobierno para la evaluación de riesgos de los servicios en la nube de Microsoft y la notificación de reguladores. [Más información](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

### <a name="financial-use-cases"></a>Casos de uso financiero

Use información general sobre casos, tutoriales y otros recursos para crear soluciones de Azure para servicios financieros. [Más información](/azure/industry/financial/)

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Usar el Administrador de cumplimiento de Microsoft para evaluar el riesgo

[El Administrador de cumplimiento de Microsoft](/microsoft-365/compliance/compliance-manager) es una característica en el [Centro de cumplimiento de Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) que le ayuda a entender la actitud de su organización en relación con el cumplimiento normativo y a tomar medidas para contribuir a reducir los riesgos. El Administrador de cumplimiento ofrece una plantilla premium para crear una evaluación de esta normativa. Busque la plantilla en la página **plantillas de evaluación** en el Administrador de cumplimiento. Obtenga información sobre cómo [crear evaluaciones en el Administrador de cumplimiento](/microsoft-365/compliance/compliance-manager-assessments).

## <a name="resources"></a>Recursos

- [Documentación de cumplimiento de Azure](/azure/compliance/)
- [Azure habilita un mundo de cumplimiento](https://azure.microsoft.com/resources/azure-enables-a-world-of-compliance/)
- [Regla](https://www.sec.gov/) [17a-4](https://www.sec.gov/rules/final/34-38245.txt) Exchange de valores y valores (SEC)
- [Recursos de servicios financieros de Microsoft Cloud](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Programa de cumplimiento de servicios financieros de Microsoft Cloud](https://aka.ms/FSCP-Print)
- [Mapa de cumplimiento de los principios normativos de informática en la nube y los servicios en línea de Microsoft](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- [Guía de evaluación y cumplimiento de riesgos para instituciones financieras en Microsoft Cloud](https://azure.microsoft.com/resources/risk-assessment-and-compliance-guide-for-financial-institutions-in-the-microsoft-cloud-/)
- [Casos de uso del sector de servicios financieros](/azure/industry/financial/)
- [Archivado en Microsoft Office 365, retención de datos y regla 17a-4](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)
