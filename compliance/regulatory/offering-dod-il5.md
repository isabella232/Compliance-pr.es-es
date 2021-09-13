---
title: Nivel de impacto del Departamento de Defensa (DoD) 5 (IL5)
description: Obtenga información sobre cómo Microsoft cumple los estándares de Nivel de impacto 5 (IL5) del Departamento de Defensa (DoD).
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
ms.openlocfilehash: c0c987dc5fbe2bee60508f0fab7dbdb8dce97857
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "59161041"
---
# <a name="department-of-defense-dod-impact-level-5-il5"></a>Nivel de impacto del Departamento de Defensa (DoD) 5 (IL5)

## <a name="dod-il5-overview"></a>Introducción a DoD IL5

La Agencia de sistemas de información de defensa (DISA) es una agencia del Departamento de Defensa de estados Unidos (DoD) que es responsable del desarrollo y mantenimiento de la Guía de requisitos de seguridad de DoD Cloud Computing [(SRG).](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html) El SRG define los requisitos de seguridad de línea base usados por DoD para evaluar la posición de seguridad de un proveedor de servicios en la nube (CSP), lo que admite la decisión de conceder una autorización provisional doD (PA) que permite a un CSP hospedar las misiones DoD. Incorpora, reemplaza y anula el modelo de seguridad en la nube (CSM) publicado anteriormente y se asigna al Marco de administración de riesgos de DoD (RMF).

DISA guía a las agencias y departamentos del Departamento de Desarrollo en la planeación y autorización del uso de un CSP. También evalúa las ofertas de CSP para el cumplimiento del SRG, un proceso de autorización por el que los CSP pueden proporcionar documentación que delinee su cumplimiento con los estándares de DoD. Emite autorizaciones provisionales de DoD (PAs) cuando corresponda, por lo que las agencias DoD y las organizaciones de soporte técnico pueden usar servicios en la nube sin tener que pasar por un proceso de aprobación completo por su cuenta, lo que ahorra tiempo y esfuerzo.

De acuerdo [con la Sección 3.2](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#3.2InformationImpactLevels) de SRG Niveles de *impacto* de la información, la información de IL5 abarca:

- Información sin clasificar controlada (CUI) que requiere un nivel de protección mayor que el que proporciona IL4
    - El [Registro CUI](https://www.archives.gov/cui) proporciona categorías específicas de información que está bajo protección por parte de la rama ejecutiva, por ejemplo, se incluyen más de 20 agrupaciones de categorías en la lista de categorías [cui](https://www.archives.gov/cui/registry/category-list).
    - [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final) Protecting *Controlled Unclassified Information in Nonfederal Systems and Organizations* está destinado a ser usado por las agencias federales en contratos u otros acuerdos establecidos con organizaciones no federales.

- Sistemas de seguridad nacionales (NSS)
    - [Nist SP 800-59](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf) *Guideline for Identifying an Information System as a National Security System* proporciona definiciones de NSS.
    - [CNSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf) *Security Categorization and Control Selection for National Security Systems* proporciona instrucciones sobre los estándares de seguridad que las agencias federales deben aplicar para clasificar la información de seguridad nacional.

El 15 de diciembre de [2014,](https://www.esi.mil/contentview.aspx?id=585) el memorándum doD CIO sobre las instrucciones actualizadas sobre la adquisición y el uso de servicios informáticos en la nube comerciales indica que "FedRAMP servirá como línea base de seguridad mínima para todos los servicios en la nube de DoD".  El SRG usa la línea base fedramp moderada en todos los niveles de impacto de la información (IL) y considera la línea base alta en algunos.

SRG Sección [5.1.1 Uso](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) doD de los controles de seguridad *de FedRAMP* indica que un FEDRAMP High PA, complementado con controles DoD FedRAMP+ y mejoras de control (C/CEs) y requisitos en el SRG, se usan para evaluar los CSP para la concesión de un DOD PA en IL5. Independientemente de cuál sea la línea base C/CE que se utilice como base para un Pa alto de FedRAMP, las consideraciones adicionales y/o los requisitos tendrán que evaluarse y aprobarse antes de que se pueda conceder un DOD PA en IL5. En concreto, la sección [5.1.2](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) del SRG *FedRAMP+* indica en la tabla 2 que se necesitan 10 C/CEs adicionales más allá de la línea base de FedRAMP High para un DOD IL5 PA.

Además, de acuerdo con la sección [5.2.2.3 de SRG,](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) los siguientes requisitos (entre otros) deben estar establecidos para un PA de nivel 5:

- La separación virtual/lógica entre doD y inquilinos o misiones del Gobierno federal es suficiente. Es necesaria la separación virtual/lógica entre los sistemas de inquilino y misión.
- Se requiere la separación física de los inquilinos que no son doD o que no son del Gobierno federal (es decir, inquilinos públicos, de gobierno local o estatal).
- El CSP restringe el acceso potencial a los DoD y la información de la comunidad a los empleados de CSP que son ciudadanos estadounidenses.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Servicios y plataformas en la nube dentro del ámbito de Microsoft

- Azure
- Servicio al cliente de Dynamics 365
- Microsoft Defender para punto de conexión (anteriormente Protección contra amenazas avanzada de Microsoft Defender)
- Microsoft Graph
- Microsoft Stream
- Office 365 U.S. Government Defense
- Power Automate (anteriormente Microsoft Flow)
- Power BI

## <a name="azure-dynamics-365-and-dod-il5"></a>Azure, Dynamics 365 y DoD IL5

Para obtener más información acerca del cumplimiento de Azure, Dynamics 365 y otros servicios en línea, vea la oferta [de Azure DoD IL5](/azure/compliance/offerings/offering-dod-il5).

## <a name="office-365-and-dod-il5"></a>Office 365 y DoD IL5

### <a name="office-365-cloud-environments"></a>Entornos en la nube de Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Aplicabilidad y servicios dentro Office 365

Use la siguiente tabla para determinar la aplicabilidad de los servicios y la suscripción de Office 365:

| **Aplicabilidad** | **Servicios incluidos** |
|:------------------|:----------------------|
| **DoD** | Servicio de fuentes de actividad, servicios de Bing, Exchange Online, Exchange Online Protection, servicios inteligentes, Microsoft Teams, portal de clientes de Office 365, Office Online, infraestructura de servicio de Office, informes de uso de Office, OneDrive para la Empresa, tarjeta de personas, SharePoint Online, Skype Empresarial, Windows Ink |

### <a name="attestation-documents"></a>Documentos de atestación

Los clientes gubernamentales de Estados Unidos pueden solicitar Office 365 fedRAMP de defensa pública de estados unidos directamente desde el Mercado [de FedRAMP](https://marketplace.fedramp.gov/#!/products?sort=productName&productNameSearch=azure) mediante el envío de un formulario de solicitud de acceso a paquetes. Debe tener una dirección de correo electrónico .gov o .mil para tener acceso a un paquete de seguridad de FedRAMP directamente desde FedRAMP.

Seleccione la documentación de FedRAMP y DoD, incluidos el Plan de seguridad del sistema (SSP), los informes de supervisión continua, plan de acción e hitos (POA M), etc., está disponible para los clientes bajo NDA y la autorización de acceso pendiente de la sección Informes de auditoría del Portal de confianza de servicio \& [- Informes de FedRAMP.](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3) Póngase en contacto con el representante de su cuenta microsoft para obtener ayuda.

### <a name="resources"></a>Recursos

- [Soluciones gubernamentales de Microsoft](https://www.microsoft.com/enterprise/government)
- [Guía de requisitos de seguridad de DoD Cloud Computing](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [Documentos de FedRAMP](https://www.fedramp.gov/documents/)
- [DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) for DoD Information Technology (TI)*
- Marco de administración de riesgos de [NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) para organizaciones y sistemas de *información:* un enfoque Life-Cycle de seguridad y privacidad
- Controles de seguridad y privacidad de [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) *para organizaciones y sistemas de información*
- [Nist SP 800-59](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf) *Guideline for Identifying an Information System as a National Security System*
- Selección de categorización y control de seguridad de [CNSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf) *para sistemas de seguridad nacionales*
- [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final) Protección de información controlada no *reclasificada en organizaciones* y sistemas nofederales
- Registro controlado sin clasificar (CUI) [y](https://www.archives.gov/cui) lista de [categorías](https://www.archives.gov/cui/registry/category-list)CUI .
