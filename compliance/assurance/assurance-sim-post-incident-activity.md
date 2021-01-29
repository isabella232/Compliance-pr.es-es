---
title: 'Administración de incidentes de seguridad de Microsoft 365: actividad posterior al incidente'
description: En este artículo se proporciona información general sobre el proceso de actividad posterior a la incidencia de administración de incidentes de seguridad en Microsoft 365.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 66c25503ac574de512f5201981112a0e54714968
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040353"
---
# <a name="microsoft-365-security-incident-management-post-incident-activity"></a><span data-ttu-id="009b0-103">Administración de incidentes de seguridad de Microsoft 365: actividad posterior al incidente</span><span class="sxs-lookup"><span data-stu-id="009b0-103">Microsoft 365 security incident management: Post-incident activity</span></span>

## <a name="postmortem"></a><span data-ttu-id="009b0-104">Postmortem</span><span class="sxs-lookup"><span data-stu-id="009b0-104">Postmortem</span></span>

<span data-ttu-id="009b0-105">Algunos incidentes de seguridad, especialmente aquellos incidentes que afectan al cliente o resultan en una infracción de datos, están sujetos a un postmortem completo del incidente.</span><span class="sxs-lookup"><span data-stu-id="009b0-105">Some security incidents, especially those incidents that are customer impacting or result in a data breach, are subject to a full incident postmortem.</span></span> <span data-ttu-id="009b0-106">El equipo de respuesta de seguridad de Microsoft 365 lleva a cabo un análisis posterior detallado con todas las partes implicadas en la respuesta a incidentes de seguridad para:</span><span class="sxs-lookup"><span data-stu-id="009b0-106">The Microsoft 365 Security Response team conducts a detailed postmortem with all the parties involved in security incident response to:</span></span>

- <span data-ttu-id="009b0-107">Documentar la secuencia de eventos que provocó el incidente</span><span class="sxs-lookup"><span data-stu-id="009b0-107">Document the sequence of events that caused the incident</span></span>
- <span data-ttu-id="009b0-108">Cree un resumen técnico del incidente tal como lo admiten las pruebas que incluyan a los actores implicados en la infracción (si se conocen).</span><span class="sxs-lookup"><span data-stu-id="009b0-108">Create a technical summary of the incident as supported by the evidence that includes the actors involved in the breach (if known).</span></span> <span data-ttu-id="009b0-109">Este resumen incluirá cómo se ejecutó la respuesta y otras claves lejos.</span><span class="sxs-lookup"><span data-stu-id="009b0-109">This summary will include how the response was executed and other key takeaways.</span></span>
- <span data-ttu-id="009b0-110">Identificar fallas técnicas, errores de procedimientos, errores manuales, defectos de procesos y problemas de comunicación, o cualquier vector de ataque desconocido previamente identificado durante la respuesta a incidentes de seguridad.</span><span class="sxs-lookup"><span data-stu-id="009b0-110">Identify technical lapses, procedural failures, manual errors, process flaws, and communication glitches, and/or any previously unknown attack vectors that were identified during the security incident response.</span></span>

<span data-ttu-id="009b0-111">El postmortem influirá directamente en la mejora del servicio de Microsoft 365, los procesos operativos y la documentación estableciendo nuevas prioridades en el ciclo de desarrollo de ingeniería de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="009b0-111">The postmortem will directly influence Microsoft 365 service improvement, operational processes, and documentation by setting new priorities in the Microsoft 365 engineering development cycle.</span></span>

## <a name="documentation"></a><span data-ttu-id="009b0-112">Documentación</span><span class="sxs-lookup"><span data-stu-id="009b0-112">Documentation</span></span>

<span data-ttu-id="009b0-113">Todos los resultados técnicos clave del proceso posterior al aprendizaje se capturan en un informe y las inversiones en servicios o correcciones en forma de errores o solicitudes de cambio de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="009b0-113">All key technical findings in the postmortem process are captured in a report and service investments or fixes in the form of bugs or development change requests.</span></span> <span data-ttu-id="009b0-114">Estos resultados se siguen con los equipos de ingeniería adecuados.</span><span class="sxs-lookup"><span data-stu-id="009b0-114">These findings are followed-up with the appropriate engineering teams.</span></span> <span data-ttu-id="009b0-115">Para los errores de procesos y problemas entre organizaciones, los problemas se documentan en la base de datos del equipo de respuesta de seguridad de Microsoft 365 y se les sigue con los grupos adecuados para resolverlos.</span><span class="sxs-lookup"><span data-stu-id="009b0-115">For process failures and cross-organizational issues, issues are documented in the Microsoft 365 Security Response team's database and followed-up with the appropriate groups to address them.</span></span>

## <a name="process-improvement"></a><span data-ttu-id="009b0-116">Mejora de procesos</span><span class="sxs-lookup"><span data-stu-id="009b0-116">Process improvement</span></span>

<span data-ttu-id="009b0-117">Responder a un incidente de seguridad en Microsoft 365 implica la coordinación con varios grupos distribuidos en distintas organizaciones dentro de Microsoft, e incluso con organizaciones externas potencialmente adecuadas, como las fuerzas del orden.</span><span class="sxs-lookup"><span data-stu-id="009b0-117">Responding to a security incident in Microsoft 365 involves coordination with multiple groups spread across different organizations within Microsoft, and potentially even appropriate external organizations such as law enforcement.</span></span> <span data-ttu-id="009b0-118">Sabemos que es fundamental evaluar nuestras respuestas después de cada incidente de seguridad para sufiencia y integridad.</span><span class="sxs-lookup"><span data-stu-id="009b0-118">We know that it is critical to evaluate our responses after every security incident for both sufficiency and completeness.</span></span> <span data-ttu-id="009b0-119">En el caso de las mejoras o cambios identificados, el equipo de respuesta de seguridad de Microsoft 365 evalúa las sugerencias en consulta con los equipos y partes interesadas adecuados y, si procede, las incorpora en los procedimientos operativos estándar.</span><span class="sxs-lookup"><span data-stu-id="009b0-119">For any identified improvements or changes, the Microsoft 365 Security Response team evaluates the suggestions in consultation with the appropriate teams and stakeholders, and where appropriate incorporates them into standard operating procedures.</span></span> <span data-ttu-id="009b0-120">Todos los cambios, errores o mejoras de servicio necesarios identificados durante la respuesta a incidentes de seguridad o la actividad posterior almortem se registran y se realiza un seguimiento en una base de datos interna de ingeniería de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="009b0-120">All required changes, bugs, or service improvements identified during the security incident response or postmortem activity are logged and tracked in an internal Microsoft 365 engineering database.</span></span> <span data-ttu-id="009b0-121">Todos los posibles errores o características se asignan al propietario adecuado.</span><span class="sxs-lookup"><span data-stu-id="009b0-121">All potential bugs or features are assigned to the appropriate owner.</span></span> <span data-ttu-id="009b0-122">El equipo de respuesta de seguridad de Microsoft 365 revisa todas las entradas hasta que se resuelve el problema.</span><span class="sxs-lookup"><span data-stu-id="009b0-122">The Microsoft 365 Security Response team reviews all entries until the issue is resolved.</span></span>

## <a name="related-articles"></a><span data-ttu-id="009b0-123">Artículos relacionados</span><span class="sxs-lookup"><span data-stu-id="009b0-123">Related articles</span></span>

- [<span data-ttu-id="009b0-124">Administración de incidentes de seguridad de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="009b0-124">Microsoft 365 security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="009b0-125">Preparación de la administración de incidentes de seguridad de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="009b0-125">Microsoft 365 security incident management preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="009b0-126">Análisis y detección de administración de incidentes de seguridad de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="009b0-126">Microsoft 365 security incident management detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="009b0-127">Contención, reactivación y recuperación de la administración de incidentes de seguridad de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="009b0-127">Microsoft 365 security incident management containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
