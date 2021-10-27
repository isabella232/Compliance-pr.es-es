---
title: Guía de evaluación de riesgos para Microsoft Cloud
description: Obtenga información sobre la Guía de evaluación de riesgos para Microsoft Cloud
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: a7b6e345afa49d82f96d9eb9e5c804fc7cbf5ffe
ms.sourcegitcommit: 1f30616328d7deb04e41dcbd44a330ea937fe94f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/26/2021
ms.locfileid: "60584874"
---
# <a name="risk-assessment-guide-for-microsoft-cloud"></a>Guía de evaluación de riesgos para Microsoft Cloud

El objetivo de una evaluación de riesgos en la nube es garantizar que el sistema y los datos que se consideran para la migración a la nube no introduzcan ningún riesgo nuevo o no identificado en la organización. El objetivo es garantizar la confidencialidad, integridad, disponibilidad y privacidad del procesamiento de información y mantener los riesgos identificados por debajo del umbral de riesgo interno aceptado.

En un modelo de responsabilidad compartida, el proveedor de servicios en la nube (CSP) es responsable de administrar la seguridad y el cumplimiento de la *nube* como proveedor. El cliente sigue siendo responsable de administrar y configurar la seguridad y el cumplimiento en la nube de acuerdo con sus necesidades y tolerancia a riesgos.

![Modelo de responsabilidad compartida.](../media/assurance-shared-responsibility-model.png)

En esta guía, se comparten procedimientos recomendados sobre cómo evaluar eficazmente los riesgos de los proveedores y cómo usar los recursos y herramientas que Microsoft pone a disposición.

## <a name="understand-shared-responsibility-in-the-cloud"></a>Comprender la responsabilidad compartida en la nube

Las implementaciones en la nube se pueden clasificar como Infraestructura como servicio (IaaS), Plataforma como servicio (PaaS) o Software como servicio (SaaS). Según el modelo de servicio en la nube aplicable, el nivel de responsabilidad sobre los controles de seguridad de las soluciones cambia entre el CSP y el cliente. En un modelo local tradicional, el cliente es responsable de toda la pila. Al pasar a la nube, todas las responsabilidades de seguridad física se transfieren al CSP. Según el modelo de servicio en la nube de su organización, las responsabilidades adicionales se trasladan al CSP. Sin embargo, en la mayoría de los modelos de servicio, la organización sigue siendo responsable de los dispositivos usados para acceder a la nube, la conectividad de red, las cuentas e identidades y los datos. Microsoft invierte en gran medida en la creación de servicios que permiten a los clientes mantener el control de sus datos durante todo el ciclo de vida.

Microsoft Cloud funciona a una hiperescala, basándose en una combinación de DevSecOps y automatización para estandarizar los modelos operativos. El modelo operativo de Microsoft cambia la forma en que se aborda el riesgo en comparación con los modelos operativos locales tradicionales, lo que lleva a la implementación de controles diferentes y a veces desconocidos para administrar riesgos. Al realizar la evaluación de riesgos en la nube, tenga en cuenta que el objetivo de Microsoft es garantizar que se aborden todos los riesgos, pero no necesariamente implementar los mismos controles que hace su organización. Microsoft puede abordar los mismos riesgos con un conjunto de controles diferente y eso debe reflejarse en la evaluación de riesgos en la nube. Diseñar e implementar controles preventivos sólidos puede reducir gran parte del trabajo requerido por los controles de detective y correctivo.

## <a name="adopt-a-framework"></a>Adoptar un marco

Microsoft recomienda que los clientes asignen su marco de controles y riesgos internos a un marco independiente que abarje los riesgos de la nube de forma estandarizada. Si los modelos de evaluación de riesgos internos existentes no abordan los desafíos específicos que vienen con la informática en la nube, se beneficiará de estos marcos ampliamente adoptados y estandarizados. Una ventaja secundaria es que Microsoft proporciona asignaciones con estos marcos en documentación y herramientas que acelerarán las evaluaciones de riesgos. Algunos ejemplos de estos marcos son el estándar de seguridad de la información [ISO 27001,](/compliance/regulatory/offering-iso-27001) [cis benchmark](/compliance/regulatory/offering-cis-benchmark)y [nist sp 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53). Microsoft ofrece el conjunto más completo de ofertas de cumplimiento de cualquier CSP. Para obtener más información, vea [Ofertas de cumplimiento de Microsoft](/compliance/regulatory/offering-home).

Use [Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) para crear sus propias evaluaciones que evalúen el cumplimiento de las normativas regionales y del sector que se aplican a su organización. Las evaluaciones se basa en el marco de las plantillas de evaluación, que contienen los controles necesarios, las acciones de mejora y, en su caso, las acciones de Microsoft para completar la evaluación. Para las acciones de Microsoft, se proporcionan planes de implementación detallados y resultados de auditoría recientes. De esta forma, el tiempo se puede guardar al buscar, asignar e investigar cómo microsoft implementa controles específicos. Para obtener más información, consulte el artículo de Microsoft Compliance Manager.

## <a name="understand-how-microsoft-operates-to-safeguard-your-data"></a>Comprender cómo funciona Microsoft para proteger sus datos

Aunque el cliente es responsable de administrar y configurar la seguridad y el cumplimiento en la *nube,* el CSP es responsable de administrar la seguridad y el cumplimiento *de la nube.* Una forma de validar que el CSP está ateniendo eficazmente sus responsabilidades y cumpliendo sus promesas es revisar sus informes de auditoría externos, como ISO y SOC. Microsoft pone a disposición de las audiencias autenticadas informes de auditoría [externos](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)en el Portal de confianza de servicio .

Además de los informes de auditoría externos, Microsoft anima a los clientes a aprovechar los siguientes recursos para ayudar a comprender cómo funciona Microsoft en profundidad:

- [Ruta de acceso Learning](/learn/roles/auditor)a petición: la plataforma Learn de Microsoft ofrece cientos de rutas de aprendizaje y módulos en diferentes temas. Entre ellos, obtenga información sobre cómo Microsoft protege los datos de los clientes para comprender las [prácticas](/learn/paths/audit-safeguard-customer-data/) fundamentales de seguridad y privacidad de Microsoft.

- [Service Assurance on Microsoft Compliance:](/compliance/#service-assurance)los artículos sobre las prácticas de Microsoft se clasifican en 16 dominios para una revisión más sencilla. Cada dominio incluye una introducción que captura cómo Microsoft administra los riesgos asociados con cada área. Se proporcionan tablas de auditoría que contienen vínculos a los informes más recientes almacenados en el Portal de confianza de servicio, secciones relacionadas y la fecha en que se realizó el informe de auditoría para los servicios en línea de Microsoft. Si está disponible, se proporcionan vínculos a artefactos que muestran la implementación del control, como evaluaciones de vulnerabilidad de terceros e informes de comprobación del plan de continuidad empresarial. Al igual que los informes de auditoría, estos artefactos se hospedan en STP y requieren autenticación para acceder.

| **Dominio** |**Descripción** |
|:---------- |:-------------- |
| [**Arquitectura**](assurance-architecture.md) | El diseño de los servicios en línea de Microsoft y los principios de seguridad que actúan como base. |
| [**Registro de auditoría**](assurance-audit-logging.md) | Cómo Microsoft captura, procesa, almacena y protege los registros que hacen posible la supervisión de seguridad y rendimiento. |
| [**Seguridad del centro de datos**](assurance-datacenter-security.md) | Cómo Microsoft opera de forma segura los centros de datos que proporcionan los medios para operar los servicios en línea de Microsoft en todo el mundo. |
| [**Cifrado y administración de claves**](assurance-encryption.md) | La protección criptográfica de las comunicaciones de los clientes y los datos almacenados y procesados en la nube. |
| [**Gobierno**](assurance-governance.md) | Cómo Microsoft crea, distribuye, actualiza y aplica directivas de seguridad en toda la empresa para cumplir las promesas de los clientes y los requisitos de cumplimiento. |
| [**Recursos humanos**](assurance-human-resources.md) | Los procesos de filtrado y la administración segura del personal a lo largo de su tiempo en Microsoft. |
| [**Administración de acceso e identidad**](assurance-identity-and-access-management.md) | La protección de los servicios en línea de Microsoft y los datos de los clientes frente al acceso no autorizado o malintencionado. |
| [**Administración de incidencias**](assurance-incident-management.md) | Los procesos que Microsoft usa para preparar, detectar, responder y comunicar todos los incidentes de seguridad y privacidad. |
| [**Seguridad de red**](assurance-network-security.md) | Cómo Protege Microsoft sus límites de red frente a ataques externos y administra su red interna para limitar su propagación. |
| [**Privacidad**](assurance-privacy.md) | Cómo Controla y protege los datos de los clientes para conservar sus derechos de datos. |
| [**Resiliencia y continuidad**](assurance-resiliency-and-continuity.md) | Procesos y tecnologías que se usan para mantener la disponibilidad del servicio y garantizar la continuidad y recuperación del negocio. |
| [**Administración de riesgos**](assurance-risk-management.md) | Identificación, evaluación y acciones tomadas para minimizar los riesgos en toda la empresa. |
| [**Operación y desarrollo de seguridad**](assurance-security-development-and-operation.md) | Cómo Microsoft garantiza que sus servicios se diseñan, ejecutan y administran de forma segura a lo largo de su ciclo de vida. |
| [**Supervisión de seguridad**](assurance-security-monitoring.md) | Análisis central de registros para detectar y alertar al personal de cualquier actividad no autorizada o malintencionada. |
| [**Administración de suministros**](assurance-supplier-management.md) | Cómo Microsoft proyecta y administra empresas de terceros que ayudan con los servicios en línea de Microsoft. |
| [**Administración de amenazas y vulnerabilidades**](assurance-vulnerability-management.md) | Los procesos que Microsoft usa para buscar, detectar y solucionar vulnerabilidades y malware. |

## <a name="resources"></a>Recursos

- [Guía de evaluación y cumplimiento de riesgos para instituciones financieras en Microsoft Cloud](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Riesgo de concentración: perspectivas de Microsoft](https://azure.microsoft.com/mediahandler/files/resourcefiles/concentration-risk-perspectives-from-microsoft-/Concentration_Risk_Perspectives_092020.pdf)
- [Portal de confianza del servicio](https://servicetrust.microsoft.com/)
