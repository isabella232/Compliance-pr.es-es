---
title: Código de prácticas para los controles de la seguridad de la información ISO/IEC 27017:2015
description: Los servicios en la nube de Microsoft han implementado este código de prácticas para los controles de seguridad de la información.
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
ms.openlocfilehash: b17c7629918bdf4386ad24d28c6cb6687728603c
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160626"
---
# <a name="isoiec-270172015-code-of-practice-for-information-security-controls"></a>Código de prácticas para los controles de la seguridad de la información ISO/IEC 27017:2015

## <a name="iso-iec-27017-overview"></a>Introducción a la norma ISO-IEC 27017

El código de prácticas ISO/IEC 27017:2015 está diseñado para que las organizaciones lo usen como referencia para seleccionar controles de seguridad de la información de servicios en la nube al implementar un sistema de administración de seguridad de la información de informática en la nube basado en la norma ISO/IEC 27002:2013. Los proveedores de servicios en la nube también pueden usar este documento como guía para implementar controles de protección comúnmente aceptados.

Este estándar internacional proporciona instrucciones adicionales para las implementaciones específicas para la nube basadas en la norma ISO/IEC 27002, así como controles adicionales para abordar los riesgos y las amenazas de seguridad de la información específicos de la nube que hacen referencia a las cláusulas 5-18 de la norma ISO/IEC 27002:2013 sobre controles, instrucciones de implementación y otra información. En concreto, en este estándar se proporcionan instrucciones sobre 37 controles de la norma ISO/IEC 27002, además de siete nuevos controles que no se encuentran en la ISO/IEC 27002. Estos nuevos controles abordan las siguientes áreas de importancia:

- Roles y responsabilidades compartidos en un entorno informático en la nube
- Eliminación y devolución de los activos de los clientes del servicio en la nube una vez que finaliza el contrato
- Protección y separación del entorno virtual de un cliente de entornos de otros clientes
- Requisitos de refuerzo de las máquinas virtuales para satisfacer las necesidades de la empresa
- Procedimientos para las operaciones administrativas de un entorno informático en la nube
- Permitir a los clientes supervisar las actividades pertinentes en un entorno informático en la nube
- Alineación de la administración de seguridad de las redes virtuales y físicas

## <a name="microsoft-and-isoiec-27017"></a>Microsoft y la norma ISO/IEC 27017

La ISO/IEC 27017 es única en cuanto a que proporciona instrucciones tanto para los proveedores de servicios en la nube como para los clientes de servicios en la nube. También proporciona a los clientes de servicios en la nube información práctica sobre lo que deben esperar de los proveedores de servicios en la nube. Los clientes pueden beneficiarse directamente de la ISO/IEC 27017, ya que les permitirá comprender las responsabilidades compartidas en la nube.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Servicios y plataformas en la nube dentro del ámbito de Microsoft

- [Azure, Azure Government y Azure Alemania](https://aka.ms/AzureCompliance)
- Microsoft Cloud App Security
- [Dynamics 365, Dynamics 365 y Dynamics 365 Germany](https://aka.ms/d365-compliance-list)
- Intune
- Microsoft Defender para punto de conexión
- Microsoft Graph
- Bot de Microsoft Healthcare
- [Escritorio administrado por Microsoft](/microsoft-365/managed-desktop/intro/compliance)
- Office 365, Office 365 Administración Pública para Estados Unidos, Office 365 Departamento de Defensa de la Administración Pública para Estados Unidos y Office 365 Alemania
- El servicio de nube de Power Automate (anteriormente conocido como Microsoft Flow) como un servicio independiente o incluido en un plan o un conjunto de aplicaciones de Office 365 o Dynamics 365
- El servicio de nube de PowerApps como servicio independiente o incluido en un plan o conjunto de aplicaciones de Office 365 o Dynamics 365
- El servicio de nube de Power BI como servicio independiente o incluido en un plan o conjunto de aplicaciones de Office 365
- Power BI incrustado
- Windows 365

## <a name="azure-dynamics-365-and-iso-270172015"></a>Azure, Dynamics 365 y SOC 27017:2015

Para obtener más información acerca del cumplimiento de Azure, Dynamics 365 y otros servicios en línea, consulte la [oferta ISO 27017 de Azure](/azure/compliance/offerings/offering-iso-27017).

## <a name="office-365-and-iso-270172015"></a>Office 365 e ISO 27017:2015

### <a name="office-365-cloud-environments"></a>Entornos en la nube de Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Aplicabilidad y servicios dentro Office 365

Use la siguiente tabla para determinar la aplicabilidad de los servicios y la suscripción de Office 365:

| **Aplicabilidad** | **Servicios incluidos** |
|:------------------|:----------------------|
| **Comercial** | Access Online, Azure Active Directory, Servicio de comunicaciones de Azure, Administrador de cumplimiento, Caja de seguridad del cliente, Delve, Exchange Online, Exchange Online Protection, Forms, Griffin, Identity Manager, Caja de seguridad (Torus), Microsoft Defender para Office 365, Microsoft Teams, MyAnalytics, complemento de Cumplimiento avanzado de Office 365, Portal de clientes de Office 365, Microservicios de Office 365 (incluidos, entre otros, Kaizala, ObjectStore, Sway, servicio de documentos de PowerPoint Online, Servicio de anotación de consultas, School Data Sync, Siphon, Speech, StaffHub, programa de la aplicación eXtensible), Centro de seguridad y cumplimiento de Office 365, Office Online, Office Pro Plus, Infraestructura de servicios de Office, OneDrive para la Empresa, Planner, PowerApps, Power Automate, Power BI, Project Online, Cifrado de servicio con clave de cliente, SharePoint Online, Skype Empresarial, Stream |
| **GCC** | Azure Active Directory, Servicio de comunicaciones de Azure, Administrador de cumplimiento, Delve, Exchange Online, Forms, Microsoft Defender para Office 365, Microsoft Teams, MyAnalytics, complemento de Cumplimiento avanzado de Office 365, Centro de seguridad y cumplimiento de Office 365, Office Online, Office Pro Plus, OneDrive para la Empresa, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype Empresarial, Stream |
| **GCC High** | Azure Active Directory, Servicio de comunicaciones de Azure, Exchange Online, Forms, Microsoft Defender para Office 365, Microsoft Teams, complemento de Cumplimiento avanzado de Office 365, Centro de seguridad y cumplimiento de Office 365, Office Online, Office Pro Plus, OneDrive para la Empresa, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype Empresarial |
| **DoD** | Azure Active Directory, Servicio de comunicaciones de Azure, Exchange Online, Forms, Microsoft Defender para Office 365, Microsoft Teams, complemento de Cumplimiento avanzado de Office 365, Centro de seguridad y cumplimiento de Office 365, Office Online, Office Pro Plus, OneDrive para la Empresa, Planner, Power BI, SharePoint Online, Skype Empresarial |

### <a name="office-365-audits-reports-and-certificates"></a>Auditorías, informes y certificados de Office 365

Los servicios en la nube de Microsoft se auditan una vez al año para certificar que cumplen el código de prácticas de la norma ISO/IEC 27017:2015 como parte del proceso de certificación de la ISO/IEC 27001:2013.

- [Office 365: Informe de evaluación de auditoría de las ISO 27001, 27018 y 27017](https://aka.ms/o365isoreport)

### <a name="frequently-asked-questions"></a>Preguntas más frecuentes

**¿A quién se aplica la norma?**

Este código de prácticas proporciona controles e instrucciones de implementación tanto para los clientes de servicios en la nube como para los proveedores de servicios en la nube. Está estructurado en un formato similar al de la norma ISO 27002:2013.

**¿Dónde puedo ver la información de cumplimiento normativo de Microsoft para la norma ISO/IEC 27017:2015?**

Puede descargar el [certificado ISO/IEC 27017:2015](https://aka.ms/azureiso27017) para Azure, Intune y Power BI.

**¿Puedo usar el cumplimiento de la norma ISO/IEC 27017 de los servicios Microsoft en el proceso de certificación de mi organización?**

Sí. Si su empresa desea obtener una certificación para las implementaciones desarrolladas en cualquiera de los servicios empresariales en la nube incluidos en el ámbito de Microsoft, puede usar las certificaciones correspondientes de Microsoft en la evaluación de cumplimiento. Sin embargo, usted tiene la responsabilidad de contratar un asesor para evaluar la implementación para el cumplimiento normativo y los controles y procesos de su propia organización.

**¿Cómo puedo obtener copias de los informes de auditoría aplicables?**

En el [Portal de confianza de servicios](https://aka.ms/stphelp) encontrará informes de auditoría independientes de terceros y otros documentos relacionados. Puede usar el portal para descargar y revisar esa documentación para obtener ayuda con sus propios requisitos normativos.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Usar el Administrador de cumplimiento de Microsoft para evaluar el riesgo

[El Administrador de cumplimiento de Microsoft](/microsoft-365/compliance/compliance-manager) es una característica en el [Centro de cumplimiento de Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) que le ayuda a entender la actitud de su organización en relación con el cumplimiento normativo y a tomar medidas para contribuir a reducir los riesgos. El Administrador de cumplimiento ofrece una plantilla premium para crear una evaluación de esta normativa. Busque la plantilla en la página **plantillas de evaluación** en el Administrador de cumplimiento. Obtenga información sobre cómo [crear evaluaciones en el Administrador de cumplimiento](/microsoft-365/compliance/compliance-manager-assessments).

### <a name="resources"></a>Recursos

- [Código de prácticas de la norma ISO/IEC 27017:2015](https://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=43757)
- [Términos de Microsoft Online Services](https://aka.ms/Online-Services-Terms)
- [Cumplimiento en el Centro de Confianza de Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
