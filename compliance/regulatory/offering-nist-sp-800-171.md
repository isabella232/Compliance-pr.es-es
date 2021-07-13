---
title: NIST SP 800-171
description: Los servicios en la nube de Microsoft cumplen con las directrices de NIST SP 800-171 para proteger la información controlada sin clasificar (CUI) en sistemas de información no profesionales.
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
ms.openlocfilehash: 19b312d1b9f31683d775049010d390710554df01
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385670"
---
# <a name="nist-sp-800-171"></a>NIST SP 800-171

## <a name="about-nist-sp-800-171"></a>Acerca de NIST SP 800-171

El Instituto Nacional de Estándares y Tecnología de Estados Unidos (NIST) promueve y mantiene estándares de medida y directrices para ayudar a proteger los sistemas de información e información de las agencias federales. En respuesta a la orden ejecutiva 13556 sobre la administración de información controlada sin clasificar (CUI), publicó [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final), *Protecting Controlled Unclassified Information In Nonfederal Information Systems and Organizations*. CUI se define como información, tanto digital como física, creada por un gobierno (o una entidad en su nombre) que, aunque no está clasificada, sigue siendo confidencial y requiere protección.

NIST SP 800-171 se publicó originalmente en junio de 2015 y se ha actualizado varias veces desde entonces en respuesta a las ciberamenazas en evolución. Proporciona directrices sobre cómo se debe acceder, transmitir y almacenar la CUI de forma segura en organizaciones y sistemas de información no profesionales; sus requisitos se encuadrán en cuatro categorías principales:

- Controles y procesos para administrar y proteger
- Supervisión y administración de sistemas de IT
- Procedimientos y procedimientos claros para los usuarios finales
- Implementación de medidas de seguridad tecnológicas y físicas

## <a name="microsoft-and-nist-sp-800-171"></a>Microsoft y NIST SP 800-171

Las organizaciones de evaluación de terceros acreditadas, Kratos Secureinfo y Coalfire, se asociaron con Microsoft para dar fe de que sus servicios en la nube dentro del ámbito cumplen los criterios de NIST SP 800-171, *Protecting Controlled Unclassified Information (CUI) in Nonfederal Information Systems and Organizations*, cuando procesan CUI. La implementación de Microsoft de los requisitos [de FedRAMP](offering-fedramp.md) ayuda a garantizar que los servicios en la nube de ámbito de Microsoft cumplan o superen los requisitos de NIST SP 800-171 mediante los sistemas y prácticas ya establecidos.

Los requisitos de NIST SP 800-171 son un subconjunto de NIST SP 800-53, el estándar que usa FedRAMP. El Apéndice D de NIST SP 800-171 proporciona una asignación directa de sus requisitos de seguridad cui a los controles de seguridad relevantes de NIST SP 800-53, para los que los servicios en la nube del ámbito ya se han evaluado y autorizado en el marco del programa FedRAMP.

Cualquier entidad que procese o almacena CUI del gobierno de Estados Unidos: instituciones de investigación, empresas de consultoría, contratistas de fabricación, debe cumplir con los estrictos requisitos de NIST SP 800-171. Esta atestación significa que los servicios en la nube de Microsoft en el ámbito pueden dar cabida a clientes que buscan implementar cargas de trabajo de CUI con la garantía de que Microsoft está en plena conformidad. Por ejemplo, todos los contratistas doD que procesan, almacenan o transmiten "información de defensa cubierta" con servicios en la nube de Microsoft en el ámbito de sus sistemas de información cumplen las cláusulas DFARS del Departamento de Defensa de Estados Unidos que requieren el cumplimiento de los requisitos de seguridad de NIST SP 800-171.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plataformas en la nube de ámbito de Microsoft & servicios

- Azure Commercial, Azure Government
- Dynamics 365 U.S. Government
- Intune
- Office 365 Estados Unidos Government Community Cloud (GCC), Office 365 GCC High y DoD

## <a name="azure-dynamics-365-and-nist-sp-800-171"></a>Azure, Dynamics 365 y NIST SP 800-171

Para obtener más información acerca del cumplimiento de Azure, Dynamics 365 y otros servicios en línea, vea la oferta de [Azure NIST SP 800-171](/azure/compliance/offerings/offering-nist-800-171).

## <a name="office-365-and-nist-sp-800-171"></a>Office 365 y NIST SP 800-171

### <a name="office-365-cloud-environments"></a>Office 365 entornos de nube

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 aplicabilidad y servicios en el ámbito

Use la tabla siguiente para determinar la aplicabilidad de los servicios Office 365 y suscripción:

| **Aplicabilidad** | **Servicios en el ámbito** |
|:------------------|:----------------------|
| **GCC** | Servicio de fuente de actividades, servicios de Bing, Delve, Exchange Online, servicios inteligentes, Microsoft Teams, portal de clientes de Office 365, Office Online, infraestructura de servicio de Office, informes de uso de Office, OneDrive para la Empresa, tarjeta de personas, SharePoint Online, Skype Empresarial, Windows Ink |
| **GCC High** | Servicio de fuente de actividad, servicios de Bing, Exchange Online, servicios inteligentes, Microsoft Teams, portal de clientes de Office 365, Office Online, infraestructura de servicio de Office, informes de uso de Office, OneDrive para la Empresa, tarjeta de personas, 
SharePoint Online, Skype Empresarial, Windows Ink |
| **DoD** | Servicio de fuente de actividades, servicios de Bing, Exchange Online, servicios inteligentes, portal de clientes de Office 365, Office Online, infraestructura de servicio de Office, informes de uso de Office, OneDrive para la Empresa, tarjeta de personas, Microsoft Teams, SharePoint Online, Skype Empresarial, Windows Ink |

### <a name="frequently-asked-questions"></a>Preguntas más frecuentes

**¿Puedo usar el cumplimiento de Microsoft con NIST SP 800-171 para mi organización?**

Sí. Los clientes de Microsoft pueden usar los controles auditados descritos en los informes de organizaciones de evaluación de terceros independientes (3PAO) sobre los estándares FedRAMP como parte de sus propios esfuerzos de análisis y calificación de riesgos de FedRAMP y NIST. Estos informes atestiguan la eficacia de los controles que Microsoft ha implementado en sus servicios en la nube en el ámbito. Los clientes son responsables de garantizar que sus cargas de trabajo cui cumplan con las directrices de NIST SP 800-171.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Usar el Administrador de cumplimiento de Microsoft para evaluar el riesgo

[El Administrador de cumplimiento de Microsoft](/microsoft-365/compliance/compliance-manager) es una característica en el [Centro de cumplimiento de Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) que le ayuda a entender la actitud de su organización en relación con el cumplimiento normativo y a tomar medidas para contribuir a reducir los riesgos. El Administrador de cumplimiento ofrece una plantilla premium para crear una evaluación de esta normativa. Busque la plantilla en la página **plantillas de evaluación** en el Administrador de cumplimiento. Obtenga información sobre cómo [crear evaluaciones en el Administrador de cumplimiento](/microsoft-365/compliance/compliance-manager-assessments).

### <a name="resources"></a>Recursos

- [La certificación de Microsoft DoD cumple los requisitos de NIST 800-171](offering-DoD-DISA-L2-L4-L5.md)
- [El cumplimiento de NIST 800-171 comienza con la documentación sobre ciberseguridad](https://www.nist800171.com/)
- [Autorizaciones fedRAMP de Microsoft Cloud Services](https://marketplace.fedramp.gov/index.html?status=Compliant&sort=productName#/products)
- [NIST 800-171 3.3 Audit and Accountability with Office 365 GCC High](https://info.summit7systems.com/blog/nist-3.3-audit-and-accountability-with-office-365)
- [Microsoft y nist Cybersecurity Framework](offering-nist-csf.md)
- [Nube de Microsoft para la Administración Pública](https://www.microsoft.com/enterprise/government)
- [Cumplimiento normativo en el Centro de confianza de Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
