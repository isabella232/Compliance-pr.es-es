---
title: Controles de acceso de supervisión y auditoría de Microsoft 365
description: 'Resumen: un resumen de los distintos controles de acceso de supervisión y auditoría disponibles en Microsoft 365.'
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 3021ce1dd59d5d071edec22286ae9c63833f1277
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120449"
---
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a>Supervisión y auditoría de controles de acceso en Microsoft 365

Microsoft realiza una amplia supervisión y auditoría de todas las operaciones, privilegios y delegación que se producen en Microsoft 365. El control de acceso de Microsoft 365 es un proceso automatizado basado en el principio de privilegios mínimos e incorpora controles y auditorías de acceso a datos:

- Todo el acceso permitido es rastreable para un usuario único. Los administradores son responsables del tratamiento del contenido de los clientes.
- Las solicitudes de control de acceso, las aprobaciones y los registros de operaciones administrativas se capturan para analizar la seguridad y los eventos malintencionados.
- Los niveles de acceso se revisan casi en tiempo real en función de la pertenencia a grupos de seguridad para garantizar que solo los usuarios que tengan justificaciones comerciales autorizadas y cumplan los requisitos de elegibilidad tengan acceso a los sistemas.
- Microsoft 365, sus controles de acceso y servicios de soporte técnico, incluidos Azure Active Directory y los centros de datos físicos, son auditados periódicamente por terceros independientes para el cumplimiento de [iso/IEC 27001](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001), [ISO/IEC 27018](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018), [SOC](https://www.microsoft.com/TrustCenter/Compliance/SOC), [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)y otros estándares [.](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)
- Los ingenieros de Microsoft 365 deben tomar formación de seguridad anual, revisar los mejores procedimientos de acceso elevado y reconocer las directivas de seguridad y privacidad de Microsoft para mantener los derechos al servicio.

Las alertas automatizadas se activan cuando se detecta actividad sospechosa, como varios inicios de sesión con errores en un período corto. El equipo de respuesta de seguridad de Microsoft 365 usa el aprendizaje automático y el análisis de big data para revisar y analizar la actividad, buscar patrones de acceso irregulares y responder proactivamente a actividades anómalas e ilegales. Microsoft también emplea un equipo dedicado de evaluadores de penetración y participa en ejercicios periódicos del equipo rojo y el equipo azul para encontrar problemas de seguridad y control de acceso en el servicio. Los clientes pueden comprobar la eficacia de los sistemas de control de acceso mediante informes de auditoría y la API de actividad de administración proporcionada por Microsoft 365.

Para obtener más información, vea la referencia de la API de actividad de administración de [Office 365](/office/office-365-management-api/office-365-management-activity-api-reference) y la auditoría y los [informes en Microsoft 365.](assurance-auditing-and-reporting-overview.md)
