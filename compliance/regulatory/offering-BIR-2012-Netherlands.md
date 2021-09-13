---
title: Estándar base Informatiebeveiliging Rijksdienst (BIR 2012)
description: Los servicios en la nube de Microsoft ayudan a los organismos del sector público en los Países Bajos a cumplir con el estándar BIR 2012.
keywords: Microsoft 365, cumplimiento, ofertas
ms.localizationpriority: high
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
ms.openlocfilehash: d0f7bd0db5d71c91a163e05e582ad8c227a8aa22
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160898"
---
# <a name="baseline-informatiebeveiliging-rijksdienst-standard-bir-2012"></a>Estándar base Informatiebeveiliging Rijksdienst (BIR 2012)

## <a name="bir-2012-overview"></a>Información general del BIR 2012

Las organizaciones que operan en el sector público holandés deben demostrar el cumplimiento normativo del estándar básico Informatiebeveiliging Rijksdienst (BIR 2012). BIR 2012 proporciona un marco de trabajo estándar basado en ISO 27001 e ISO 27002. Cuando se usa Microsoft Azure u Office 365, Microsoft administra los controles de BIR 2012 para estos servicios en la Nube siguiendo el modelo de responsabilidad compartida de la informática en la nube. Por lo tanto, las organizaciones que necesitan cumplir con BIR 2012 deben determinar si los servicios de Microsoft subyacentes que usan son compatibles con BIR 2012.

El informe de cobertura de BIR ofrece instrucciones para las situaciones en las que los estándares de BIR están cubiertos por las certificaciones ISO 27001 existentes disponibles para servicios en la nube de Microsoft. En caso de controles de BIR adicionales que no estén cubiertos por la norma ISO 27001, se han hecho referencias a otras atestaciones independientes, documentación de auditoría o declaraciones contractuales.

## <a name="microsoft-and-bir-2012"></a>Microsoft y BIR 2012

Aunque Microsoft no está sujeto al cumplimiento de BIR 2012, los clientes del sector gubernamental que buscan usar los servicios en la nube pueden usar las certificaciones existentes de Microsoft para determinar su cumplimiento con este estándar. Azure y Office 365 se someten a diferentes certificaciones y atestaciones periódicas independientes, algunas de las cuales están estrechamente relacionadas con el BIR 2012.

[Descargue la guía de usuario de la nube de Microsoft: Azure y Office 365 BIR-2012](https://go.microsoft.com/fwlink/p/?linkid=2099461)

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Servicios y plataformas en la nube dentro de Microsoft

- Azure
- Intune
- Office 365

## <a name="office-365-and-bir-2012"></a>Office 365 y BIR 2012

### <a name="office-365-cloud-environments"></a>Entornos en la nube de Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Aplicabilidad y servicios dentro Office 365

Use la siguiente tabla para determinar la aplicabilidad de los servicios y la suscripción de Office 365:

| **Aplicabilidad** | **Servicios incluidos** |
|:------------------|:----------------------|
| **Comercial** | Azure Information Protection, Bookings, Exchange Online Protection, Exchange Online, Kaizala, Microsoft Analytics, Microsoft Booking, Microsoft Graph, Microsoft Teams, Microsoft To-Do para la Web, MyAnalytics, Office 365 Cloud App Security, Grupos de Office 365, Office 365 Video, Office Delve, OneDrive para la Empresa, Planner, Power Apps, Power Automate, Power BI para Office 365, PowerApps, SharePoint Online, Skype Empresarial, StaffHub, Stream, Sway, Yammer Enterprise |

## <a name="audits-reports-and-certificates"></a>Auditorías, informes y certificados

Microsoft contrató a una empresa de auditoría independiente de terceros para analizar en qué medida las certificaciones y atestaciones actuales de Azure y Office 365 (como ISO/IEC 27001 y SOC 2 Tipo 2) cubren la parte de BIR 2012 de la que Microsoft es responsable. El informe resultante proporciona una asignación de estas certificaciones y atestaciones existentes a los controles enumerados en el estándar BIR 2012. Los clientes pueden usar el informe como una herramienta para ayudar a adoptar Azure de forma compatible con BIR 2012. El informe muestra claramente qué controles BIR 2012 están cubiertos por Microsoft y qué controles deben ser implementados por los clientes. El informe "Microsoft Cloud: Azure and Office 365 BIR 2012 Baseline Coverage" se puede descargar desde la sección [Informes de auditoría del Portal de confianza de servicios - Informes de Auditoría GRC](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3).

## <a name="frequently-asked-questions"></a>Preguntas más frecuentes

**¿Está Microsoft certificado con el BIR 2012?**

El ámbito de cumplimiento del BIR se limita al sector gubernamental. Requiere que la organización implemente un sistema de administración de seguridad de la información y que aborde los riesgos con las medidas técnicas y de la organización adecuadas. Para Microsoft, como proveedor de servicios de nube, el cumplimiento del BIR no es un objetivo, ni es factible de forma técnica. Cuando un cliente implementa o usa servicios en la nube de Microsoft, es posible que estos servicios estén en el ámbito de una evaluación del BIR. Sin embargo, la organización debe agregar sus propios controles, elecciones y procesos (adicionales), que forman parte de la evaluación de BIR general. El objetivo del informe es demostrar que una entidad gubernamental puede adoptar servicios en la nube de Microsoft de un modo que sea compatible con el BIR 2012.

**¿Un cliente que use servicios en la nube de Microsoft cumple con BIR 2012?**

Demostrar el cumplimiento normativo de BIR es responsabilidad del cliente. Cuando se usa un proveedor de servicios de nube, los clientes suelen exigir garantías del proveedor y agregan su propia tecnología (adicional) y decisiones, elecciones y procesos de la organización. Este esfuerzo da como resultado una evaluación general por parte del cliente de su cumplimiento con BIR, que puede enviarse para su revisión o certificación a un auditor de terceros. El informe de cobertura de BIR ofrece información acerca de los controles BIR que se encuentran cubiertos por los servicios en la nube de Microsoft, pero no cubre el cumplimiento de un extremo a otro.

**El informe no muestra una cobertura del 100 %. ¿No es viable el cumplimiento de BIR 2012?**

Los servicios en la nube de Microsoft proporcionan muchos controles para ayudar a las organizaciones dentro del territorio holandés con sus necesidades de cumplimiento de BIR. Sin embargo, una organización debe complementar estas garantías de proveedor con sus propias opciones de implementación, controles de tecnología adicionales y procesos administrativos. El informe muestra que ya cuenta con un 91 % de cobertura directa de la lista completa de controles aplicables. Para los controles restantes, Microsoft ofrece directrices en el informe acerca de cómo se puede demostrar el cumplimiento de esos controles.

**¿El informe de cobertura de BIR es un documento jurídicamente vinculante?**

No. Es una herramienta de ayuda para el proceso de garantía del BIR interno del cliente y le ayuda a establecer confianza en que es viable el cumplimiento del BIR. El informe tiene un estado descriptivo y contiene una renuncia legal.

**¿Podemos compartir este informe?**

El informe se le proporciona a los clientes con un acuerdo de no divulgación, sobre la base de que solo se usará para informar a los clientes y que no se va a copiar o revelar por otros canales que no sean la [Plataforma de confianza de servicios](https://www.microsoft.com/TrustCenter/STP/default.aspx) de Microsoft. Los clientes pueden compartir el informe con su auditor interno o externo como parte de sus procesos de cumplimiento o garantía.

## <a name="resources"></a>Recursos

- [ISO-IEC 27001](offering-iso-27001.md)
- [Prescripción de seguridad nacional de 2013 (BVR)](https://wetten.overheid.nl/BWBR0033512/2013-06-01)
- [Prescripción sobre la seguridad de información nacional de 2007 (VIR)](https://wetten.overheid.nl/BWBR0022141/2007-07-01)
- [Seguridad de información base (BIR)](https://www.earonline.nl/index.php/BIR_2012)
- [Cumplimiento en el Centro de Confianza de Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
