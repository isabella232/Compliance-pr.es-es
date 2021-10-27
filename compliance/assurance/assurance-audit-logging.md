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
ms.openlocfilehash: a676f86e8f90370a3501ead041220f4c2b3d128a
ms.sourcegitcommit: 1f30616328d7deb04e41dcbd44a330ea937fe94f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/26/2021
ms.locfileid: "60582663"
---
# <a name="audit-logging-overview"></a>Información general sobre el registro de auditoría

## <a name="how-do-microsoft-online-services-employ-audit-logging"></a>¿Cómo emplean los servicios en línea de Microsoft el registro de auditoría?

Los servicios en línea de Microsoft emplean el registro de auditoría para detectar actividades no autorizadas y proporcionar responsabilidades al personal de Microsoft. Los registros de auditoría capturan detalles sobre los cambios de configuración del sistema y los eventos de acceso, con detalles para identificar quién fue responsable de la actividad, cuándo y dónde se realizó la actividad y cuál fue el resultado de la actividad. El análisis de registro automatizado admite la detección casi en tiempo real de comportamiento sospechoso. Los posibles incidentes se escalan al equipo de respuesta de seguridad de Microsoft adecuado para una investigación más exhaustiva.

El registro de auditoría interna de Servicios en línea de Microsoft captura datos de registro de varios orígenes, como:

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

## <a name="how-do-microsoft-online-services-centralize-and-report-on-audit-logs"></a>¿Cómo centralizan los servicios en línea de Microsoft e informan sobre los registros de auditoría?

Muchos tipos diferentes de datos de registro se cargan desde servidores microsoft a una solución de supervisión de seguridad propietaria para análisis casi en tiempo real (NRT) y un servicio informático de big data interno (Cosmos) o Azure Data Explorer (Kusto) para almacenamiento a largo plazo. Esta transferencia de datos se produce a través de una conexión TLS validada por FIPS 140-2 en puertos y protocolos aprobados mediante herramientas de administración de registros automatizadas.

Los registros se procesan en NRT mediante métodos basados en reglas, estadísticas y aprendizaje automático para detectar indicadores de rendimiento del sistema y eventos de seguridad potenciales. Los modelos de aprendizaje automático usan datos de registro entrantes y datos de registro histórico almacenados en Cosmos o Kusto para mejorar continuamente las capacidades de detección. Las detecciones relacionadas con la seguridad generan alertas, notificando a los ingenieros de llamadas de un posible incidente y desencadenando acciones de corrección automatizadas cuando corresponda. Además de la supervisión de seguridad automatizada, los equipos de servicio usan herramientas de análisis y paneles para la correlación de datos, consultas interactivas y análisis de datos. Estos informes se usan para supervisar y mejorar el rendimiento general del servicio.

Para obtener más información sobre la supervisión de seguridad y las alertas, vea la información general [sobre la supervisión de seguridad](assurance-security-monitoring.md).

![Flujo de datos de auditoría.](../media/assurance-audit-data-flow.png)

## <a name="how-do-microsoft-online-services-protect-audit-logs"></a>¿Cómo protegen los registros de auditoría los servicios en línea de Microsoft?

Las herramientas usadas en los servicios en línea de Microsoft para recopilar y procesar registros de auditoría no permiten cambios permanentes o irreversibles en el contenido del registro de auditoría original ni en el orden de tiempo. El acceso a los datos del servicio en línea de Microsoft almacenados en Cosmos o Kusto está restringido al personal autorizado. Además, Microsoft restringe la administración de registros de auditoría a un subconjunto limitado de miembros del equipo de seguridad responsables de la funcionalidad de auditoría. El personal del equipo de seguridad no tiene acceso administrativo permanente a Cosmos o Kusto. El acceso administrativo requiere la aprobación de acceso just-in-time (JIT) y todos los cambios en los mecanismos de registro para Cosmos se registran y auditan. Los registros de auditoría se conservan lo suficiente como para admitir investigaciones de incidentes y cumplir los requisitos normativos. El período exacto de retención de datos del registro de auditoría determinado por los equipos de servicio; La mayoría de los datos del registro de auditoría se conservan durante 90 días en Cosmos y 180 días en Kusto.

## <a name="how-do-microsoft-online-services-protect-user-personal-data-that-may-be-captured-in-audit-logs"></a>¿Cómo protegen los servicios en línea de Microsoft los datos personales de los usuarios que se pueden capturar en los registros de auditoría?

Antes de cargar datos de registro, una aplicación de administración de registros automatizada usa un servicio de depuración para quitar los campos que contienen datos de clientes, como la información del inquilino y los datos personales del usuario, y reemplazar esos campos por un valor hash. Los registros anonimizados y hash se reescriben y, a continuación, se cargan en Cosmos. Todas las transferencias de registro se producen a través de una conexión cifrada TLS (FIPS 140-2).

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y certificaciones externas. Consulte la siguiente tabla para la validación de controles relacionados con el registro de auditoría.

### <a name="azure-and-dynamics-365"></a>Azure y Dynamics 365

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registro y supervisión | 2 de diciembre de 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registro y supervisión | 2 de diciembre de 2020 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registro y supervisión | 2 de diciembre de 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | VM-1: Registro y colección de eventos de seguridad | 31 de marzo de 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | C5-6: Acceso restringido a registros <br> VM-1: Registro y colección de eventos de seguridad | 31 de marzo de 2021 |

### <a name="office-365"></a>Office 365

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AU-2: Eventos de auditoría <br> AU-3: Contenido de registros de auditoría <br> AU-4: Capacidad de almacenamiento de auditoría <br> AU-5: Respuesta a errores de procesamiento de auditoría <br> AU-6: Revisión de auditoría, análisis e informes <br> AU-7: Reducción de auditoría y generación de informes <br> AU-8: Marcas de tiempo <br> AU-9: Protección de la información de auditoría  <br> AU-10: No repudio <br> AU-11: Retención de registros de auditoría <br> AU-12: Generación de auditoría  | 24 de septiembre de 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registro y supervisión | 20 de abril de 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: Registro de centros de datos <br> CA-60: Registro de auditoría | 24 de diciembre de 2020 |