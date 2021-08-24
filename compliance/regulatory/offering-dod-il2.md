---
title: Nivel de impacto del Departamento de Defensa (DoD) 2 (IL2)
description: Obtenga información sobre cómo Microsoft cumple los estándares de Nivel de impacto 2 (IL2) del Departamento de Defensa (DoD).
keywords: Microsoft 365, cumplimiento, ofertas
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
ms.openlocfilehash: c57183a53c563fffa2bb3eb1cedb2fca23db26f4
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482453"
---
# <a name="department-of-defense-dod-impact-level-2-il2"></a>Nivel de impacto del Departamento de Defensa (DoD) 2 (IL2)

## <a name="dod-il2-overview"></a>Introducción a DoD IL2

La Agencia de sistemas de información de defensa (DISA) es una agencia del Departamento de Defensa de estados Unidos (DoD) que es responsable del desarrollo y mantenimiento de la Guía de requisitos de seguridad de DoD Cloud Computing [(SRG).](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html) El SRG define los requisitos de seguridad de línea base usados por DoD para evaluar la posición de seguridad de un proveedor de servicios en la nube (CSP), lo que admite la decisión de conceder una autorización provisional doD (PA) que permite a un CSP hospedar las misiones DoD. Incorpora, reemplaza y anula el modelo de seguridad en la nube (CSM) publicado anteriormente y se asigna al Marco de administración de riesgos de DoD (RMF).

DISA guía a las agencias y departamentos del Departamento de Desarrollo en la planeación y autorización del uso de un CSP. También evalúa las ofertas de CSP para el cumplimiento del SRG, un proceso de autorización por el que los CSP pueden proporcionar documentación que delinee su cumplimiento con los estándares de DoD. Emite autorizaciones provisionales de DoD (PAs) cuando corresponda, por lo que las agencias DoD y las organizaciones de soporte técnico pueden usar servicios en la nube sin tener que pasar por un proceso de aprobación completo por su cuenta, lo que ahorra tiempo y esfuerzo.

El 15 de diciembre de [2014,](https://www.esi.mil/contentview.aspx?id=585) el memorándum doD CIO sobre las instrucciones actualizadas sobre la adquisición y el uso de servicios informáticos en la nube comerciales indica que "FedRAMP servirá como línea base de seguridad mínima para todos los servicios en la nube de DoD".  El SRG usa la línea base fedramp moderada en todos los niveles de impacto de la información (IL) y considera la línea base alta en algunos.

La sección [5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) doD de SRG de los controles de seguridad *de FedRAMP* indica que la información de IL2 puede hospedarse en un CSP que tenga como mínimo un PA moderado de FedRAMP y un PA de nivel 2 doD, sujeto al cumplimiento de los requisitos de seguridad del personal descritos en la sección 5.6.2. Sin embargo, este enfoque no ayuda al CSP a cumplir otros requisitos de seguridad e integración según lo requiera el propietario de la misión. De acuerdo con la sección [5.2.2.1 de la sección 5.2.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) de los requisitos de ubicación y separación de SRG, DoD IL2 PA está adecuadamente cubierto por un FedRAMP Moderate PA de modo que los requisitos no se evaluarán adicionalmente para un PA IL2.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Servicios y plataformas en la nube dentro de Microsoft

- Azure
- Dynamics 365
- Microsoft Cloud App Security
- Microsoft Defender para punto de conexión
- Microsoft Graph
- Microsoft Intune
- Microsoft Stream
- Office 365 U.S. Government, Office 365 U.S. Government - High
- Power Apps
- Power Automate
- Power BI

## <a name="azure-dynamics-365-and-dod-il2"></a>Azure, Dynamics 365 y DoD IL2

Para obtener más información acerca del cumplimiento de Azure, Dynamics 365 y otros servicios en línea, vea la oferta [de Azure DoD IL2](/azure/compliance/offerings/offering-dod-il2).

## <a name="office-365-and-dod-il2"></a>Office 365 y DoD IL2

### <a name="office-365-cloud-environments"></a>Entornos en la nube de Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Aplicabilidad y servicios dentro Office 365

Use la siguiente tabla para determinar la aplicabilidad de los servicios y la suscripción de Office 365:

| **Aplicabilidad** | **Servicios incluidos** |
|:------------------|:----------------------|
| **GCC** | Servicio de fuente de actividades, servicios de Bing, Delve, Exchange Online Protection, Exchange Online, servicios inteligentes, Microsoft Teams, portal de clientes de Office 365, Office Online, infraestructura de servicio de Office, informes de uso de Office, OneDrive para la Empresa, tarjeta de personas, SharePoint Online, Skype Empresarial, Windows Ink |
| **GCC High** | Servicio de fuente de actividades, servicios de Bing, Delve, Exchange Online Protection, Exchange Online, servicios inteligentes, Microsoft Teams, portal de clientes de Office 365, Office Online, infraestructura de servicio de Office, informes de uso de Office, OneDrive para la Empresa, tarjeta de personas, SharePoint Online, Skype Empresarial, Windows Ink |

### <a name="resources"></a>Recursos

- [Soluciones gubernamentales de Microsoft](https://www.microsoft.com/enterprise/government)
- [Guía de requisitos de seguridad de DoD Cloud Computing](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [Documentos de FedRAMP](https://www.fedramp.gov/documents/)
- Marco de administración de riesgos de [NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) para organizaciones y sistemas de *información:* un enfoque Life-Cycle de seguridad y privacidad
- Controles de seguridad y privacidad de [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) *para organizaciones y sistemas de información*
- [DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) for DoD Information Technology (TI)*
