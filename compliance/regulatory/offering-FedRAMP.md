---
title: Programa Federal de Administración de Autorizaciones y Riesgo (FedRAMP)
description: A Microsoft se le concedió el Programa federal de administración de riesgos y autorización de Estados Unidos P-ATOs y ATOs.
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
ms.openlocfilehash: 3f178689655662272fc8149259cf769ce122a18a
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482945"
---
# <a name="federal-risk-and-authorization-management-program-fedramp"></a>Programa Federal de Administración de Autorizaciones y Riesgo (FedRAMP)

## <a name="fedramp-overview"></a>Introducción a FedRAMP

El Programa federal de administración de riesgos y autorización de Estados Unidos (FedRAMP) se estableció para proporcionar un enfoque estandarizado para evaluar, supervisar y autorizar productos y servicios de informática en la nube en virtud de la Ley federal de administración de seguridad de la información (FISMA), y para acelerar la adopción de soluciones seguras en la nube por parte de las agencias federales.

La Office de administración y presupuesto ahora requiere que todas las agencias federales ejecutivas usen FedRAMP para validar la seguridad de los servicios en la nube. (Otras agencias también lo han adoptado, por lo que también es útil en otras áreas del sector público). El Instituto Nacional de Estándares y Tecnología (NIST) SP 800-53 establece los estándares obligatorios, establece categorías de seguridad de sistemas de información (confidencialidad, integridad y disponibilidad) para evaluar el posible impacto en una organización en caso de que sus sistemas de información y de información se vea comprometido. FedRAMP es el programa que certifica que un proveedor de servicios en la nube (CSP) cumple esos estándares.

Los CSP que desaconsejen vender servicios a una agencia federal pueden tomar tres rutas para demostrar el cumplimiento de FedRAMP:

- Obtenga una autoridad provisional para operar (P-ATO) de la Junta de autorización conjunta (JAB). El JAB es el principal órgano de gobierno y toma de decisiones de FedRAMP. Los representantes del Departamento de Defensa, el Departamento de Seguridad Nacional y la Administración de Servicios Generales sirven en la pizarra. La junta concede un P-ATO a los SPC que han demostrado el cumplimiento de FedRAMP.
- Recibir una autoridad para operar (ATO) de una agencia federal.
- O bien, trabaje independientemente para desarrollar un paquete proporcionado por CSP que cumpla los requisitos del programa.

Cada una de estas rutas requiere una estricta revisión técnica por parte del FedRAMP Program Management Office (PMO) y una evaluación por parte de una organización independiente de terceros que esté acreditada por el programa.

Las autorizaciones de FedRAMP se conceden en tres niveles de impacto según las directrices de NIST: bajo, medio y alto. Estos niveles clasifican el impacto que la pérdida de confidencialidad, integridad o disponibilidad podría tener en una organización: bajo (efecto limitado), medio (efecto adverso grave) y alto (efecto grave o catastrófico).

## <a name="microsoft-and-fedramp"></a>Microsoft y FedRAMP

Los servicios en la nube gubernamentales de Microsoft, incluidos Azure Government, Dynamics 365 Government y Office 365 U.S. Government cumplen los exigentes requisitos del Programa federal de administración de riesgos y autorización de Estados Unidos (FedRAMP), lo que permite a las agencias federales estadounidenses beneficiarse del ahorro de costos y la seguridad rigurosa de Microsoft Cloud.

Los servicios en la nube del gobierno de Microsoft ofrecen a los clientes del sector público una amplia variedad de servicios compatibles con FedRAMP y herramientas sólidas de guía e implementación, incluido el plan [de FedRAMP High,](https://aka.ms/fedrampblueprint)que ayuda a los clientes a implementar un conjunto básico de directivas para cualquier arquitectura implementada en Azure que debe implementar los controles FedRAMP High.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Servicios y plataformas en la nube dentro de Microsoft

- Azure y Azure Government
- [Dynamics 365 U.S. Government](https://aka.ms/d365-compliance-list)
- Intune
- Office 365 U.S. Government, Office 365 U.S. Government - High, Office 365 U.S. Government Defense
- El servicio de nube de Power BI como servicio independiente o incluido en un plan o conjunto de aplicaciones de Office 365

## <a name="azure-dynamics-365-and-fedramp"></a>Azure, Dynamics 365 y FedRAMP

Para obtener más información acerca del cumplimiento de Azure, Dynamics 365 y otros servicios en línea, consulte la oferta [de Azure FedRAMP](/azure/compliance/offerings/offering-fedramp).

## <a name="office-365-and-fedramp"></a>Office 365 y FedRAMP

- Office 365 y Office 365 gobierno de los Estados Unidos tienen un ATO del Departamento de Salud y Servicios Humanos de estados Unidos (DHHS).
- Office 365 U.S. Government Defense tiene un P-ATO de la Agencia de sistemas de información de defensa estadounidense (DISA). Cualquier cliente que desee implementar Office 365 U.S. Government Defense puede usar la DISA P-ATO para generar un ATO de agencia para documentar su aceptación.
- Office 365 (planes empresariales y empresariales) y Office 365 Gobierno de los Estados Unidos tienen un ATO de la agencia FedRAMP en el nivel de impacto moderado de la Office del Inspector General. Office 365 El Gobierno de Estados Unidos fue el primer servicio de colaboración y correo electrónico basado en la nube en obtener esta autorización.

### <a name="office-365-cloud-environments"></a>Entornos en la nube de Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Aplicabilidad y servicios dentro Office 365

Use la siguiente tabla para determinar la aplicabilidad de los servicios y la suscripción de Office 365:

| **Aplicabilidad** | **Servicios incluidos** |
|:------------------|:----------------------|
| **GCC** | Servicio de fuentes de actividad, servicios de Bing, Delve, Exchange Online, Exchange Online Protection, infraestructura, servicios inteligentes, Microsoft Teams, portal de clientes de Office 365, Office Online, servicio de Office, informes de uso de Office, OneDrive para la Empresa, tarjeta de personas, SharePoint Online, Skype Empresarial, Windows Ink |
| **GCC High** | Servicio de fuentes de actividad, servicios de Bing, Exchange Online, Exchange Online Protection, servicios inteligentes, Microsoft Teams, portal de clientes de Office 365, Office Online, infraestructura de servicio de Office, informes de uso de Office, OneDrive para la Empresa, tarjeta de personas, SharePoint Online, Skype Empresarial, Windows Ink |
| **DoD** | Servicio de fuentes de actividad, servicios de Bing, Exchange Online Protection, Exchange Online, servicios inteligentes, Microsoft Teams, portal de clientes de Office 365, Office Online, infraestructura de servicio de Office, informes de uso de Office, OneDrive para la Empresa, tarjeta de personas, SharePoint Online, Skype Empresarial, Windows Ink |

### <a name="office-365-audits-reports-and-certificates"></a>Auditorías, informes y certificados de Office 365

Microsoft debe recertificar sus servicios en la nube cada año para mantener sus P-ATOs y ATOs. Para ello, Microsoft debe supervisar y evaluar continuamente sus controles de seguridad y demostrar que la seguridad de sus servicios permanece en cumplimiento.

- [Informes de auditoría de Microsoft FedRAMP](https://aka.ms/MicrosoftFedRAMPAuditDocuments)  

### <a name="frequently-asked-questions"></a>Preguntas más frecuentes

**¿Los servicios en la nube de Microsoft cumplen con la Ley federal de administración de seguridad de la información (FISMA)?**

FISMA es la ley federal que requiere que las agencias federales estadounidenses y sus asociados adquieran sistemas de información y servicios solo de organizaciones que cumplan con los requisitos de FISMA. La mayoría de las agencias y sus proveedores que indican que cumplen con FISMA se refieren a cómo cumplen los controles identificados por el NIST en la publicación especial 800-53 rev 4. El proceso FISMA (pero no los propios estándares subyacentes) fue reemplazado por FedRAMP en 2011.

**¿A quién se aplica FedRAMP?**

'FedRAMP es obligatorio para las implementaciones en la nube de la agencia federal y los modelos de servicio en los niveles de impacto de riesgo bajo y moderado.' Cualquier agencia federal que quiera participar en un CSP puede ser necesaria para cumplir las especificaciones de FedRAMP. Además, las empresas que emplean tecnologías en la nube en productos o servicios usados por el gobierno federal pueden ser necesarias para obtener un ATO.

**¿Dónde inicia mi agencia su propio esfuerzo de cumplimiento?**

Para obtener información general sobre los pasos que deben seguir las agencias federales para navegar correctamente por FedRAMP y cumplir sus requisitos, vaya a [Obtener autorización: Autorización de la agencia](https://www.fedramp.gov/agency-authorization/).

**¿Puedo usar el cumplimiento de Microsoft en el proceso de autorización de mi agencia?**

Sí. Puede usar las certificaciones de los servicios en la nube de Microsoft como base para cualquier programa o iniciativa que requiera un ATO de una agencia gubernamental federal. Sin embargo, debe lograr sus propias autorizaciones para componentes fuera de estos servicios.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Usar el Administrador de cumplimiento de Microsoft para evaluar el riesgo

[El Administrador de cumplimiento de Microsoft](/microsoft-365/compliance/compliance-manager) es una característica en el [Centro de cumplimiento de Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) que le ayuda a entender la actitud de su organización en relación con el cumplimiento normativo y a tomar medidas para contribuir a reducir los riesgos. El Administrador de cumplimiento ofrece una plantilla premium para crear una evaluación de esta normativa. Busque la plantilla en la página **plantillas de evaluación** en el Administrador de cumplimiento. Obtenga información sobre cómo [crear evaluaciones en el Administrador de cumplimiento](/microsoft-365/compliance/compliance-manager-assessments).

### <a name="resources"></a>Recursos

- [Programa federal de administración de riesgos y autorización](https://www.fedramp.gov/)
- [Marco de evaluación de seguridad de FedRAMP](https://www.fedramp.gov/assets/resources/documents/FedRAMP_Security_Assessment_Framework.pdf)
- [Administración del cumplimiento en la nube en Microsoft](https://www.microsoft.com/trustcenter/common-controls-hub)
- [Nube de Microsoft para la Administración Pública](https://go.microsoft.com/fwlink/p/?linkid=2087246)
