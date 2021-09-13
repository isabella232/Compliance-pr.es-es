---
title: Microsoft 365 Supervisión y auditoría de controles de acceso
description: 'Resumen: un resumen de los distintos controles de acceso de supervisión y auditoría disponibles en Microsoft 365.'
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: bf760bf68169092f99fe5a668c9f0087060f7ea2
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160217"
---
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a>Supervisión y auditoría de controles de acceso en Microsoft 365

Microsoft realiza una supervisión y auditoría exhaustivas de todas las operaciones, privilegios y delegación que se producen en Microsoft 365. Microsoft 365 control de acceso es un proceso automatizado basado en el principio de privilegios mínimos e incorpora controles y auditorías de acceso a datos:

- Todo el acceso permitido es rastreable a un usuario único. Los administradores son responsables del tratamiento del contenido del cliente.
- Las solicitudes de control de acceso, las aprobaciones y los registros de operaciones administrativas se capturan para analizar la seguridad y los eventos malintencionados.
- Los niveles de acceso se revisan casi en tiempo real en función de la pertenencia a grupos de seguridad para garantizar que solo los usuarios que tienen justificaciones empresariales autorizadas y cumplen los requisitos de elegibilidad tengan acceso a los sistemas.
- Microsoft 365, sus controles de acceso y los servicios de soporte técnico, incluidos los centros de datos físicos y Azure Active Directory, son auditados periódicamente por terceros independientes para cumplir con [iso/IEC 27001](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001), [ISO/IEC 27018](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018), [SOC](https://www.microsoft.com/TrustCenter/Compliance/SOC), [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)y otros estándares [.](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)
- Microsoft 365 los ingenieros deben realizar cursos de seguridad anuales, revisar los procedimientos de acceso elevado y reconocer las directivas de seguridad y privacidad de Microsoft para mantener los derechos al servicio.

Las alertas automatizadas se desencadenan cuando se detecta actividad sospechosa, como varios inicios de sesión con errores en un período corto. El equipo Microsoft 365 security response usa el aprendizaje automático y el análisis de big data para revisar y analizar la actividad, buscar patrones de acceso irregulares y responder proactivamente a actividades anómalas e ilícitas. Microsoft también emplea un equipo dedicado de evaluadores de penetración y realiza ejercicios periódicos de equipo rojo y equipo azul para encontrar problemas de seguridad y control de acceso en el servicio. Los clientes pueden comprobar la eficacia de los sistemas de control de acceso mediante informes de auditoría y la API de actividad de administración proporcionada por Microsoft 365.

Para obtener más información, [vea Office 365 referencia de la API](/office/office-365-management-api/office-365-management-activity-api-reference) de actividad de administración y Auditoría e informes en [Microsoft 365](assurance-auditing-and-reporting-overview.md).
