---
title: Información general sobre el registro de auditoría
description: Obtenga información sobre el registro de auditoría en Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 5a851373660fbc64de8fbfbb191e7b631493bae6534f687e73917f10fa605ac7
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "54289303"
---
# <a name="audit-logging-overview"></a>Información general sobre el registro de auditoría

## <a name="how-does-microsoft-365-employ-audit-logging"></a>¿Cómo Microsoft 365 el registro de auditoría?

Microsoft 365 el registro de auditoría para detectar actividades no autorizadas en sus productos y servicios y proporcionar responsabilidades al personal de Microsoft. Los registros de auditoría capturan detalles sobre los cambios de configuración del sistema y los eventos de acceso, con detalles para identificar quién fue responsable de la actividad, cuándo y dónde se realizó la actividad y cuál fue el resultado de la actividad. El análisis de registro automatizado admite la detección casi en tiempo real de comportamiento sospechoso. Los posibles incidentes se escalan al Microsoft 365 de respuesta de seguridad para una investigación más exhaustiva.

Microsoft 365 registro de auditoría interna captura datos de registro de varios orígenes, como:

- Registros de eventos
- Registros de AppLocker
- Datos de rendimiento
- System Center datos
- Registros de detalles de llamadas
- Datos de calidad de la experiencia
- Registros del servidor web iis
- SQL Server registros
- Datos de Syslog
- Registros de auditoría de seguridad

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>¿Cómo Microsoft 365 centraliza e informa en los registros de auditoría?

Muchos tipos diferentes de datos de registro se cargan desde servidores de Microsoft 365 a una solución de supervisión de seguridad propietaria para el análisis casi en tiempo real (NRT) y un servicio de big data computing interno (Cosmos) para el almacenamiento a largo plazo. Esta transferencia de datos se produce a través de una conexión TLS validada por FIPS 140-2 en puertos y protocolos aprobados mediante una herramienta de automatización propietaria denominada Office Data Loader (ODL).

Los registros se procesan en NRT mediante métodos basados en reglas, estadísticas y aprendizaje automático para detectar indicadores de rendimiento del sistema y eventos de seguridad potenciales. Los modelos de aprendizaje automático usan datos de registro entrantes y datos de registro históricos almacenados en Cosmos para mejorar continuamente las capacidades de detección. Las detecciones relacionadas con la seguridad generan alertas, notificando a los ingenieros de llamadas de un posible incidente y desencadenando acciones de corrección automatizadas cuando corresponda. Además de la supervisión de seguridad automatizada, los equipos de servicio usan herramientas de análisis y paneles para la correlación de datos, consultas interactivas y análisis de datos. Estos informes se usan para supervisar y mejorar el rendimiento general del servicio.

Para obtener más información sobre la supervisión de seguridad y las alertas, vea la información general [sobre la supervisión de seguridad](assurance-security-monitoring.md).

![Flujo de datos de auditoría](../media/assurance-audit-data-flow.png)

## <a name="how-does-microsoft-365-protect-audit-logs"></a>¿Cómo Microsoft 365 los registros de auditoría?

Las herramientas usadas en Microsoft 365 recopilar y procesar registros de auditoría no permiten cambios permanentes o irreversibles en el contenido del registro de auditoría original ni en el orden de tiempo. El acceso Microsoft 365 los datos almacenados en Cosmos está restringido al personal autorizado. Además, Microsoft 365 la administración de registros de auditoría a un subconjunto limitado de miembros del equipo de seguridad responsables de la funcionalidad de auditoría. El equipo de seguridad no tiene acceso administrativo permanente a Cosmos. El acceso administrativo requiere la aprobación de acceso just-in-time (JIT) y todos los cambios en los mecanismos de registro para Cosmos se registran y auditan. Los registros de auditoría se conservan lo suficiente como para admitir investigaciones de incidentes y cumplir los requisitos normativos. El período exacto de retención de datos del registro de auditoría Cosmos determina los equipos de servicio; la mayoría de los datos del registro de auditoría se conservan durante 90 días o más.

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>¿Cómo Microsoft 365 la información identificable del usuario final que se puede capturar en los registros de auditoría?

Antes de cargar datos de registro, la aplicación ODL usa un servicio de depuración para quitar los campos que contienen datos de cliente, como la información del inquilino y la información identificable del usuario final, y reemplazar esos campos por un valor hash. Los registros anonimizados y hash se reescriben y, a continuación, se cargan en Cosmos. Todas las transferencias de registro se producen a través de una conexión cifrada TLS (FIPS 140-2).

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y certificaciones externas. Consulte la siguiente tabla para la validación de controles relacionados con el registro de auditoría.

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AU-2: Eventos de auditoría <br> AU-3: Contenido de registros de auditoría <br> AU-4: Capacidad de almacenamiento de auditoría <br> AU-5: Respuesta a errores de procesamiento de auditoría <br> AU-6: Revisión de auditoría, análisis e informes <br> AU-7: Reducción de auditoría y generación de informes <br> AU-8: Marcas de tiempo <br> AU-9: Protección de la información de auditoría  <br> AU-10: No repudio <br> AU-11: Retención de registros de auditoría <br> AU-12: Generación de auditoría  | 24 de septiembre de 2020 | 
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registro y supervisión | 20 de abril de 2021 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registro y supervisión | 20 de abril de 2021 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: Registro de centros de datos <br> CA-60: Registro de auditoría | 24 de diciembre de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: Registro de centros de datos <br> CA-60: Registro de auditoría | 24 de diciembre de 2020|