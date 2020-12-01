---
title: Introducción al registro de auditoría
description: Obtenga información sobre el registro de auditorías en Microsoft 365
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
ms.openlocfilehash: 3714a5df73253d0814e1d4067248116cb6e10a40
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/30/2020
ms.locfileid: "49509791"
---
# <a name="audit-logging-overview"></a>Introducción al registro de auditoría

## <a name="how-does-microsoft-365-employ-audit-logging"></a>¿Cómo usa Microsoft 365 el registro de auditoría?

Microsoft 365 emplea el registro de auditoría para detectar actividades no autorizadas en sus productos y servicios y proporcionar responsabilidad para el personal de Microsoft. Registros de auditoría Capture detalles sobre los cambios en la configuración del sistema y los eventos de acceso, con detalles para identificar quién es responsable de la actividad, Cuándo y dónde tuvo lugar la actividad y cuál era el resultado de la actividad. El análisis de registros automatizado admite la detección en tiempo real del comportamiento sospechoso. Los posibles incidentes se escalan a Microsoft 365 Security Response Team para una mayor investigación.

El registro de auditoría interno de Microsoft 365 captura datos de registro de una gran variedad de orígenes, como:

- Registros de eventos
- Registros de AppLocker
- Datos de rendimiento
- Datos de System Center
- Registros de detalles de llamadas
- Datos de la calidad de la experiencia
- Registros del servidor Web de IIS
- Registros de SQL Server
- Datos de syslog
- Registros de auditoría de seguridad

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>¿Cómo centraliza y reporte Microsoft 365 los registros de auditoría?

Se cargan muchos tipos diferentes de datos de registro de los servidores de Microsoft 365 en un servicio informático interno de gran tamaño denominado cosmos. Cada equipo de servicio carga los registros de auditoría desde sus servidores respectivos a la base de datos cosmos para agregación y análisis. Esta transferencia de datos se produce a través de una conexión TLS validada por FIPS 140-2 en puertos y protocolos aprobados mediante una herramienta de automatización patentada llamada Office Data Loader (ODL).

Los equipos de servicio ejecutan consultas con ámbito en sus datos en cosmos para la correlación de registros, las alertas y los informes. Por ejemplo, el equipo de seguridad 365 de Microsoft usa los datos de cosmos con un analizador de registro de eventos propietario para correlacionar los datos de registro, enviar alertas y generar informes que requieren acción en el entorno de producción Microsoft 365. Los informes de estos datos se usan para corregir las vulnerabilidades y mejorar el rendimiento general del servicio.

## <a name="how-does-microsoft-365-protect-audit-logs"></a>¿Cómo protege Microsoft 365 los registros de auditoría?

Las herramientas usadas en Microsoft 365 para recopilar y procesar registros de auditoría no permiten cambios permanentes o irreversibles en el contenido del registro de auditoría original o el pedido de tiempo. El acceso a los datos de Microsoft 365 almacenados en cosmos está restringido al personal autorizado. Microsoft 365 restringe la administración de la funcionalidad de auditoría al subconjunto limitado de miembros del equipo de servicio que son responsables de la funcionalidad de auditoría. Estos miembros del equipo no tienen la capacidad de modificar o eliminar datos de Cosmos, y todos los cambios en los mecanismos de registro para cosmos se registran y auditan. Los registros de auditoría se conservan durante el tiempo suficiente como para admitir investigaciones de incidentes y cumplir con los requisitos normativos. El período exacto de retención de datos del registro de auditoría en cosmos está determinado por los equipos de servicio; la mayoría de los datos del registro de auditoría se conservan durante 90 días o más.

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>¿Cómo protege Microsoft 365 la información de identificación del usuario final que se puede capturar en los registros de auditoría?

Antes de cargar datos en cosmos, la aplicación ODL usa un servicio de limpieza para ofuscar cualquier campo que contenga datos de clientes, como información de inquilinos e información de identificación del usuario final, y reemplazar los campos con un valor hash. Los registros hash y anonimizan se reescriben y, a continuación, se cargan en cosmos.

## <a name="related-external-regulations--certifications"></a>Certificaciones & de las reglamentaciones externas relacionadas

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y las certificaciones externas. Consulte la tabla siguiente para validar los controles relacionados con el registro de auditoría.

| **Auditorías externas** | **Section** | **Fecha del informe más reciente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AU-2: eventos de auditoría <br> AU-3: contenido de registros de auditoría <br> AU-4: capacidad de almacenamiento de auditoría <br> AU-5: respuesta a errores de procesamiento de auditoría <br> AU-6: revisión de auditoría, análisis e informes <br> AU-7: reducción de auditoría y generación de informes <br> AU-8: marcas de tiempo <br> AU-9: protección de la información de auditoría  <br> AU-10: sin rechazo <br> AU-11: retención de registro de auditoría <br> AU-12: generación de auditoría  | 24 de septiembre de 2020 | 
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.-hasta: registro y supervisión | 22 de febrero de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.-hasta: registro y supervisión | 22 de febrero de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-48: registro de centro de conexión <br> CA-60: registro de auditoría | 30 de septiembre de 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-48: registro de centro de conexión <br> CA-60: registro de auditoría | 30 de septiembre de 2019 |