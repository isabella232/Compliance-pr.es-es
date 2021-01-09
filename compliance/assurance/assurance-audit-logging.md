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
ms.openlocfilehash: 6e32e089a5b42f846a332e32218959fef5103615
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787509"
---
# <a name="audit-logging-overview"></a>Información general sobre el registro de auditoría

## <a name="how-does-microsoft-365-employ-audit-logging"></a>¿Cómo emplea Microsoft 365 el registro de auditoría?

Microsoft 365 emplea el registro de auditoría para detectar actividades no autorizadas en sus productos y servicios y proporcionar responsabilidad al personal de Microsoft. Los registros de auditoría capturan detalles sobre los cambios de configuración del sistema y los eventos de acceso, con detalles para identificar quién fue responsable de la actividad, cuándo y dónde se produjo la actividad y cuál fue el resultado de la actividad. El análisis de registro automatizado admite la detección casi en tiempo real de comportamiento sospechoso. Los posibles incidentes se escalan al equipo de respuesta de seguridad de Microsoft 365 para una investigación más exhaustiva.

El registro de auditoría interna de Microsoft 365 captura datos de registro de una variedad de orígenes, como:

- Registros de eventos
- Registros de AppLocker
- Datos de rendimiento
- Datos de System Center
- Registros de detalles de llamadas
- Datos de calidad de la experiencia
- Registros del servidor web de IIS
- SQL Server registros
- Datos de Resalte
- Registros de auditoría de seguridad

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>¿Cómo centraliza e informa Microsoft 365 los registros de auditoría?

Muchos tipos diferentes de datos de registro se cargan desde los servidores de Microsoft 365 a un servicio informático interno de big data denominado Cosmos. Cada equipo de servicio carga registros de auditoría de sus respectivos servidores en la base de datos de Cosmos para su agregación y análisis. Esta transferencia de datos se produce a través de una conexión TLS validada por FIPS 140-2 en puertos y protocolos aprobados mediante una herramienta de automatización propietaria denominada Office Data Loader (ODL).

Los equipos de servicio ejecutan consultas con ámbito en sus datos en Cosmos para la correlación de registros, las alertas y los informes. Por ejemplo, el equipo de seguridad de Microsoft 365 usa datos de Cosmos con un analizador de registros de eventos propietario para correlacionar los datos de registro, enviar alertas y generar informes que pueden actuar sobre posibles actividades sospechosas en el entorno de producción de Microsoft 365. Los informes de estos datos se usan para corregir vulnerabilidades y mejorar el rendimiento general del servicio.

## <a name="how-does-microsoft-365-protect-audit-logs"></a>¿Cómo protege Microsoft 365 los registros de auditoría?

Las herramientas usadas en Microsoft 365 para recopilar y procesar registros de auditoría no permiten cambios permanentes o irreversibles en el contenido del registro de auditoría original ni en el orden de tiempo. El acceso a los datos de Microsoft 365 almacenados en Cosmos está restringido al personal autorizado. Microsoft 365 restringe la administración de la funcionalidad de auditoría al subconjunto limitado de miembros del equipo de servicio que son responsables de la funcionalidad de auditoría. Estos miembros del equipo no tienen la capacidad de modificar o eliminar datos del Cosmos, y todos los cambios en los mecanismos de registro de Cosmos se registran y auditan. Los registros de auditoría se conservan el tiempo suficiente para admitir investigaciones de incidentes y cumplir con los requisitos normativos. El período exacto de retención de datos del registro de auditoría en Cosmos lo determinan los equipos de servicio; La mayoría de los datos del registro de auditoría se conservan durante 90 días o más.

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>¿Cómo protege Microsoft 365 la información identificable del usuario final que se puede capturar en los registros de auditoría?

Antes de cargar datos en Cosmos, la aplicación ODL usa un servicio de limpieza para ofuscar los campos que contienen datos de clientes, como la información del inquilino y la información identificable del usuario final, y reemplazar esos campos con un valor hash. Los registros anonimizados y con hash se reescriben y, a continuación, se cargan en Cosmos.

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las certificaciones y normativas externas. Consulte la tabla siguiente para validar los controles relacionados con el registro de auditoría.

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AU-2: Eventos de auditoría <br> AU-3: Contenido de registros de auditoría <br> AU-4: Capacidad de almacenamiento de auditoría <br> AU-5: Respuesta a errores de procesamiento de auditoría <br> AU-6: Revisión, análisis e informes de auditoría <br> AU-7: Reducción de auditoría y generación de informes <br> AU-8: Marcas de tiempo <br> AU-9: Protección de la información de auditoría  <br> AU-10: No rechazo <br> AU-11: Retención de registros de auditoría <br> AU-12: Generación de auditoría  | 24 de septiembre de 2020 | 
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registro y supervisión | 22 de febrero de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registro y supervisión | 22 de febrero de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: Registro de centro de datos <br> CA-60: Registro de auditoría | 24 de diciembre de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: Registro de centro de datos <br> CA-60: Registro de auditoría | 24 de diciembre de 2020|