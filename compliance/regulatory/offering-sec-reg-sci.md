---
title: 'Securities and Exchange Commission : Regulation Systems Compliance and Integrity (SCI)'
description: Las reglas de SCI se aplican a las entidades de SCI, que incluyen organizaciones autorreguladas (SROS) como intercambios de acciones y opciones, agencias de compensación registradas y sistemas de comercio alternativos (ATS).
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
ms.openlocfilehash: 06537749b60f40ab87211aa6efa65e8e88ed691b
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/23/2021
ms.locfileid: "53087539"
---
# <a name="securities-and-exchange-commission-regulation-systems-compliance-and-integrity-sci"></a>Securities and Exchange Commission: Regulation Systems Compliance and Integrity (SCI)

## <a name="about-regulation-sci"></a>Acerca de la LIC de regulación

La Comisión de valores y Exchange de Estados Unidos (SEC) es una agencia independiente del gobierno federal de los Estados Unidos y el principal supervisor y regulador de los mercados de valores de Estados Unidos. Se encarga de la autoridad de cumplimiento de las leyes federales de valores, propone nuevas reglas de valores y supervisa la regulación del mercado de la industria de valores.

En noviembre de 2014, la SEC adoptó regulation [systems compliance and integrity (SCI)](https://www.sec.gov/rules/final/2014/34-73639.pdf) (y Form SCI for reporting SCI events) para reforzar la infraestructura tecnológica en los mercados de valores de Estados Unidos. La regulación está diseñada para reducir la frecuencia de las interrupciones del sistema, mejorar la resistencia cuando se producen estos incidentes y aumentar la supervisión de la SEC de la tecnología del mercado de valores y la aplicación de sus reglamentos.

Las reglas de SCI se aplican a las entidades de SCI, que incluyen organizaciones autorreguladas (SROS) como intercambios de acciones y opciones, agencias de compensación registradas y sistemas de comercio alternativos (ATS). Las reglas regulan principalmente los sistemas que admiten directamente las funciones clave del mercado de valores: negociación, liquidación y liquidación, enrutamiento de pedidos, datos de mercado, regulación del mercado y vigilancia del mercado.

## <a name="microsoft-and-sec-regulation-sci"></a>Sci de regulación de Microsoft y sec

La Comisión de Valores y Exchange de Estados Unidos (SEC) adoptó el Reglamento SCI para reforzar la infraestructura tecnológica de las organizaciones financieras que operan y admiten los mercados de valores de Estados Unidos. Bajo supervisión de la SEC, sus requisitos están diseñados para garantizar que estos sistemas tienen alta disponibilidad, resistencia fuerte y baja latencia (alto volumen de mensajes con poco retraso).

Para ayudar a guiar a los clientes de servicios financieros de Estados Unidos que deben cumplir con esta reglamentación, Microsoft ha publicado la Microsoft Azure guía de implementación de la nube de integridad y cumplimiento de sistemas [de regulación de la SEC.](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers) Las instrucciones de este documento:

- Proporciona información general sobre las capacidades generales de Azure que admiten resistencia fuerte, alta disponibilidad y baja latencia.
- Aclara qué áreas de control y aspectos normativos aborda Azure. Esta asignación punto a punto de las características y servicios de Azure a los requisitos de SCI mide el cumplimiento de Azure con el marco normativo. También ayuda a los clientes a comprender dónde pueden cambiar las responsabilidades de seguridad a Azure que tenían totalmente propiedad cuando operaban localmente. Estas funcionalidades están a la vez que las promesas que Microsoft hace en los SLA de Azure.
- Especifica cada requisito de SCI de regulación que es responsabilidad del cliente abordar y ofrece documentación y servicios de Azure para ayudarles a resolver estas responsabilidades.

En este documento se proporciona una lista de comprobación exhaustiva de las áreas críticas de foco de LIC de regulación. Esta lista de comprobación ayuda a las organizaciones financieras a comprender cómo pueden adoptar Azure para ayudar a garantizar a sus reguladores, clientes y liderazgo que pueden cumplir con los requisitos normativos aplicables.

## <a name="microsoft-in-scope-cloud-services"></a>Servicios de la nube dentro del alcance de Microsoft

- [Azure](https://aka.ms/AzureCompliance)

## <a name="how-to-implement"></a>Cómo se debe implementar

- [Guía de implementación de](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)SCI de regulación: Mapas capacidades de Azure con respecto al reglamento y se detalla la responsabilidad compartida del cumplimiento.
- [Diseño de aplicaciones de Azure confiables:](/azure/architecture/resiliency/)una breve introducción a cómo crear confiabilidad en cada paso del diseño de aplicaciones de Azure.
- [Diseño de aplicaciones de alta disponibilidad:](/azure/storage/common/storage-designing-ha-apps-with-ragrs)cómo los desarrolladores pueden ayudar a garantizar que sus Azure Storage están altamente disponibles.
- [Guía de cumplimiento y evaluación de riesgos](https://aka.ms/RiskGovernanceGuide): Cree un modelo de gobierno para la evaluación de riesgos de los servicios en la nube de Microsoft y las notificaciones reglamentarias.

## <a name="frequently-asked-questions"></a>Preguntas frecuentes

**¿Qué significa la responsabilidad compartida al usar la tecnología en la nube?**

A medida que los entornos informáticos se mueven de centros de datos locales a los de la nube, la responsabilidad de la seguridad también cambia: el proveedor de servicios en la nube (CSP) y el cliente ahora comparten esa responsabilidad. Para cada aplicación y solución, la cantidad de esa responsabilidad depende del cliente y la cantidad del CSP depende del modelo de Azure que implemente un cliente: IaaS, SaaS o PaaS. Es deber del cliente comprender hasta qué punto son responsables de implementar los controles de seguridad necesarios. Sin embargo, Microsoft proporciona instrucciones para ayudar a los clientes a navegar por esta dinámica compleja. Para obtener más información, [lea Responsabilidades compartidas para Cloud Computing](https://gallery.technet.microsoft.com/Shared-Responsibilities-81d0ff91).

**¿Qué instituciones financieras pueden aprovechar Azure para ayudar a cumplir los requisitos de LIC de regulación?**

Las organizaciones financieras o entidades sci que están sujetas a esta normativa pueden implementar Azure. La SEC dice que su reglamento se aplica a "organizaciones autorreguladoras (SROS), incluidas las bolsa de valores y opciones, las agencias de compensación registradas, FINRA y el MSRB, sistemas de negociación alternativos (ATS), que comercializan valores NMS y no NMS que superen los umbrales de volumen especificados, disensors de datos de mercado consolidados (procesadores de planes) y ciertas agencias de compensación exentas".

## <a name="resources"></a>Recursos

- [Respuestas de la SEC a preguntas más frecuentes relativas a la LIC de regulación](https://www.sec.gov/divisions/marketreg/regulation-sci-faq.shtml)
- [Continuidad empresarial y recuperación ante desastres (BCDR): Regiones emparejadas de Azure](/azure/best-practices-availability-paired-regions)
- [Mapa de cumplimiento de principios normativos y normativas de informática en la nube Microsoft Online Services](https://aka.ms/FinServ-Guide-US)
- [Programa de cumplimiento para los servicios financieros de Microsoft Cloud](https://aka.ms/FSCP-Print)
- [Programa de cumplimiento de servicios financieros en Azure](https://aka.ms/FinServ-Compliance-Azure)
- [Servicios financieros de Microsoft](https://aka.ms/FinServ-Compliance)
- [Regla 17a-4 de Microsoft y sec](offering-SEC-17a-4.md)
- [Cumplimiento en el centro de confianza de Microsoft ](https://www.microsoft.com/trust-center/compliance/compliance-overview)
