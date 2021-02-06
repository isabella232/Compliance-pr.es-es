---
title: 'Comisión de intercambio y valores: cumplimiento e integridad de los sistemas de regulación (SCI)'
description: Las reglas de SCI se aplican a las entidades de SCI, que incluyen organizaciones autorre regulatorias (SRE) como intercambios de valores y opciones, agencias de intercambio registradas y sistemas de comercio alternativos (ATS).
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
ms.openlocfilehash: 049f0516598209411b0c5ca47eea39140762fd3d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50119879"
---
# <a name="securities-and-exchange-commission-regulation-systems-compliance-and-integrity-sci"></a>Comisión de intercambio y valores: Cumplimiento e integridad de los sistemas de regulación (SCI)

## <a name="about-regulation-sci"></a>Acerca del Reglamento SCI

La Us Securities and Exchange Commission (SEC) es una agencia independiente del gobierno federal de los Estados Unidos y el principal supervisor y regulador de los mercados de valores de Estados Unidos. Controla la autoridad de cumplimiento de las leyes federales de valores, propone nuevas reglas de valores y supervisa la regulación del mercado de la industria de valores.

En noviembre de 2014, la SEC adoptó regulation [systems compliance and integrity (SCI)](https://www.sec.gov/rules/final/2014/34-73639.pdf) (and Form SCI for reporting SCI events) para reforzar la infraestructura tecnológica en los mercados de valores de Estados Unidos. El reglamento está diseñado para reducir la frecuencia de interrupciones del sistema, mejorar la resistencia cuando se producen estos incidentes y aumentar la supervisión de la SEC de la tecnología del mercado de valores y la aplicación de sus normativas.

Las reglas de SCI se aplican a las entidades de SCI, que incluyen organizaciones autorre regulatorias (SRE) como intercambios de valores y opciones, agencias de intercambio registradas y sistemas de comercio alternativos (ATS). Las reglas regulan principalmente los sistemas que admiten directamente las funciones clave del mercado de valores: comercio, autorización y liquidación, enrutamiento de pedidos, datos del mercado, regulación del mercado y vigilancia del mercado.

## <a name="microsoft-and-sec-regulation-sci"></a>Microsoft y SEC Regulation SCI

La Comisión de Bolsa y Valores de Estados Unidos (SEC) adoptó el Reglamento SCI para reforzar la infraestructura tecnológica de las organizaciones financieras que operan y son compatibles con los mercados de valores de Estados Unidos. Bajo la supervisión de la SEC, sus requisitos están diseñados para garantizar que estos sistemas tengan alta disponibilidad, resistencia sólida y baja latencia (gran volumen de mensajes con poco retraso).

Para guiar a los clientes de servicios financieros de Estados Unidos que deben cumplir con este reglamento, Microsoft ha publicado la Guía de implementación de la nube de integridad y cumplimiento de sistemas de regulación de [Microsoft Azure SEC.](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers) Las instrucciones de este documento:

- Proporciona una introducción a las capacidades generales de Azure que admiten resistencia sólida, alta disponibilidad y baja latencia.
- Deja claro qué áreas de control y aspectos normativos aborda Azure. Esta asignación punto a punto de las características y servicios de Azure a los requisitos de SCI mide el cumplimiento de Azure con el marco normativo. También ayuda a los clientes a comprender dónde pueden cambiar las responsabilidades de seguridad a Azure de las que eran propietarios cuando operaban de forma local. Estas funcionalidades están en respaldo de las promesas que Microsoft realiza en los SLA de Azure.
- Especifica cada requisito de LA SCI del Reglamento que es responsabilidad del cliente y ofrece documentación y servicios de Azure para ayudarles a resolver estas responsabilidades.

En este documento se proporciona una lista de comprobación exhaustiva de las áreas críticas de CENTRARSE de regulación. Esta lista de comprobación ayuda a las organizaciones financieras a comprender cómo pueden adoptar Azure para ayudar a garantizar a sus reguladores, clientes y liderazgo que pueden cumplir con los requisitos normativos aplicables.

## <a name="microsoft-in-scope-cloud-services"></a>Servicios de la nube dentro del alcance de Microsoft

- [Azure](https://aka.ms/AzureCompliance)

## <a name="how-to-implement"></a>Cómo se debe implementar

- [Guía de implementación de SCI de regulación:](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)asigna las capacidades de Azure a la normativa y detalla la responsabilidad compartida del cumplimiento.
- [Diseño de aplicaciones de Azure confiables:](/azure/architecture/resiliency/)breve introducción a cómo crear confiabilidad en cada paso del diseño de aplicaciones de Azure.
- [Diseño de aplicaciones de alta disponibilidad:](/azure/storage/common/storage-designing-ha-apps-with-ragrs)cómo los desarrolladores pueden ayudar a garantizar que sus aplicaciones de Azure Storage están altamente disponibles.
- [Guía de cumplimiento y evaluación de riesgos](https://aka.ms/RiskGovernanceGuide): Cree un modelo de gobierno para la evaluación de riesgos de los servicios en la nube de Microsoft y las notificaciones reglamentarias.

## <a name="frequently-asked-questions"></a>Preguntas más frecuentes

**¿Qué significa la responsabilidad compartida al usar la tecnología en la nube?**

A medida que los entornos informáticos se mueven de centros de datos locales a los de la nube, la responsabilidad de la seguridad también cambia: el proveedor de servicios en la nube (CSP) y el cliente ahora comparten esa responsabilidad. Para cada aplicación y solución, la parte de esa responsabilidad corresponde al cliente y cuánto depende del CSP depende del modelo de Azure que implemente un cliente: IaaS, SaaS o PaaS. Es obligación del cliente comprender hasta qué punto son responsables de implementar los controles de seguridad requeridos. Sin embargo, Microsoft proporciona instrucciones para ayudar a los clientes a navegar por esta dinámica compleja. Para obtener más información, lea [Responsabilidades compartidas para informática en la nube.](https://gallery.technet.microsoft.com/Shared-Responsibilities-81d0ff91)

**¿Qué instituciones financieras pueden aprovechar Azure para ayudar a cumplir los requisitos de LA SCI del Reglamento?**

Las organizaciones financieras, o entidades de SCI, que están sujetas a este reglamento pueden implementar Azure. La SEC dice que su reglamento se aplica a "las organizaciones autorre regulatorias (SRE), incluidas las bolsa de valores y opciones, los organismos de intercambio registrados, FINRA y la MSRB, sistemas de comercio alternativos (ATS), que comercializan las acciones nms y no nms que superen los umbrales de volumen especificados, la eliminación de los datos del mercado consolidado (procesadores de planes) y determinadas agencias de compensación exentas".

## <a name="resources"></a>Recursos

- [Respuestas de la SEC a las preguntas más frecuentes relacionadas con el Reglamento SCI](https://www.sec.gov/divisions/marketreg/regulation-sci-faq.shtml)
- [Continuidad empresarial y recuperación ante desastres (BCDR): Regiones emparejadas de Azure](/azure/best-practices-availability-paired-regions)
- [Mapa de cumplimiento de principios normativos de informática en la nube y Microsoft Online Services](https://aka.ms/FinServ-Guide-US)
- [Programa de cumplimiento para los servicios financieros de Microsoft Cloud](https://aka.ms/FSCP-Print)
- [Cumplimiento de los servicios financieros en Azure](https://aka.ms/FinServ-Compliance-Azure)
- [Servicios financieros de Microsoft](https://aka.ms/FinServ-Compliance)
- [Microsoft y la regla 17a-4 de la SEC](offering-SEC-17a-4.md)
- [Cumplimiento en el Centro de Confianza de Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
