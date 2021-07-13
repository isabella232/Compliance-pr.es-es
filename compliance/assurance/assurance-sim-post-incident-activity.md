---
title: 'Administración de incidentes de seguridad de Microsoft: actividad posterior al incidente'
description: En este artículo, se proporciona información general sobre el proceso de actividad posterior a la incidencia de administración de incidentes de seguridad en los servicios en línea de Microsoft.
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
hideEdit: true
ms.openlocfilehash: 965c7d6d0d469b9eea981252805bda598c92a4c8
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377537"
---
# <a name="microsoft-security-incident-management-post-incident-activity"></a><span data-ttu-id="f4427-103">Administración de incidentes de seguridad de Microsoft: actividad posterior al incidente</span><span class="sxs-lookup"><span data-stu-id="f4427-103">Microsoft security incident management: Post-incident activity</span></span>

## <a name="postmortem"></a><span data-ttu-id="f4427-104">Postmortem</span><span class="sxs-lookup"><span data-stu-id="f4427-104">Postmortem</span></span>

<span data-ttu-id="f4427-105">Algunos incidentes de seguridad, especialmente los incidentes que afectan al cliente o resultan en una vulneración de datos, están sujetos a un postmortem completo de incidentes.</span><span class="sxs-lookup"><span data-stu-id="f4427-105">Some security incidents, especially those incidents that are customer impacting or result in a data breach, are subject to a full incident postmortem.</span></span> <span data-ttu-id="f4427-106">El equipo de respuesta de seguridad lleva a cabo un postmortem detallado con todas las partes implicadas en la respuesta a incidentes de seguridad para:</span><span class="sxs-lookup"><span data-stu-id="f4427-106">The security response team conducts a detailed postmortem with all the parties involved in security incident response to:</span></span>

- <span data-ttu-id="f4427-107">Documente la secuencia de eventos que provocaron el incidente.</span><span class="sxs-lookup"><span data-stu-id="f4427-107">Document the sequence of events that caused the incident.</span></span>
- <span data-ttu-id="f4427-108">Cree un resumen técnico del incidente tal como lo admiten las pruebas que incluyen los actores implicados en la infracción (si se conoce).</span><span class="sxs-lookup"><span data-stu-id="f4427-108">Create a technical summary of the incident as supported by the evidence that includes the actors involved in the breach (if known).</span></span> <span data-ttu-id="f4427-109">Este resumen incluirá cómo se ejecutó la respuesta y otras claves.</span><span class="sxs-lookup"><span data-stu-id="f4427-109">This summary will include how the response was executed and other key takeaways.</span></span>
- <span data-ttu-id="f4427-110">Identifique lapsos técnicos, errores de procedimiento, errores manuales, defectos de proceso y problemas de comunicación, o cualquier vector de ataque desconocido anteriormente que se identificara durante la respuesta a incidentes de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f4427-110">Identify technical lapses, procedural failures, manual errors, process flaws, and communication glitches, and/or any previously unknown attack vectors that were identified during the security incident response.</span></span>

<span data-ttu-id="f4427-111">The postmortem will directly influence Microsoft online service improvement, operational processes, and documentation by setting new priorities in the Microsoft online services engineering development cycle.</span><span class="sxs-lookup"><span data-stu-id="f4427-111">The postmortem will directly influence Microsoft online service improvement, operational processes, and documentation by setting new priorities in the Microsoft online services engineering development cycle.</span></span>

## <a name="documentation"></a><span data-ttu-id="f4427-112">Documentación</span><span class="sxs-lookup"><span data-stu-id="f4427-112">Documentation</span></span>

<span data-ttu-id="f4427-113">Todas las conclusiones técnicas clave del proceso postmortem se capturan en un informe y las inversiones de servicio o correcciones en forma de errores o solicitudes de cambio de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="f4427-113">All key technical findings in the postmortem process are captured in a report and service investments or fixes in the form of bugs or development change requests.</span></span> <span data-ttu-id="f4427-114">Estos resultados se siguen con los equipos de ingeniería adecuados.</span><span class="sxs-lookup"><span data-stu-id="f4427-114">These findings are followed-up with the appropriate engineering teams.</span></span> <span data-ttu-id="f4427-115">Para los errores de proceso y problemas entre organizaciones, los problemas se documentan en la base de datos del equipo de respuesta de seguridad y se siguen con los grupos adecuados para solucionarlos.</span><span class="sxs-lookup"><span data-stu-id="f4427-115">For process failures and cross-organizational issues, issues are documented in the security response team's database and followed-up with the appropriate groups to address them.</span></span>

## <a name="process-improvement"></a><span data-ttu-id="f4427-116">Mejora de procesos</span><span class="sxs-lookup"><span data-stu-id="f4427-116">Process improvement</span></span>

<span data-ttu-id="f4427-117">Responder a un incidente de seguridad en los servicios en línea de Microsoft implica la coordinación con varios grupos repartidos entre distintas organizaciones dentro de Microsoft, e incluso organizaciones externas potencialmente adecuadas, como las fuerzas del orden.</span><span class="sxs-lookup"><span data-stu-id="f4427-117">Responding to a security incident in Microsoft online services involves coordination with multiple groups spread across different organizations within Microsoft, and potentially even appropriate external organizations such as law enforcement.</span></span> <span data-ttu-id="f4427-118">Sabemos que es fundamental evaluar nuestras respuestas después de cada incidente de seguridad para la suficiencia y la integridad.</span><span class="sxs-lookup"><span data-stu-id="f4427-118">We know that it is critical to evaluate our responses after every security incident for both sufficiency and completeness.</span></span> <span data-ttu-id="f4427-119">Para las mejoras o cambios identificados, el equipo de respuesta de seguridad evalúa las sugerencias en consulta con los equipos y partes interesadas adecuados, y, si procede, las incorpora en los procedimientos operativos estándar.</span><span class="sxs-lookup"><span data-stu-id="f4427-119">For any identified improvements or changes, the security response team evaluates the suggestions in consultation with the appropriate teams and stakeholders, and where appropriate incorporates them into standard operating procedures.</span></span> <span data-ttu-id="f4427-120">Todos los cambios, errores o mejoras de servicio necesarios identificados durante la respuesta a incidentes de seguridad o la actividad postmortem se registran y se realiza un seguimiento en una base de datos de ingeniería interna de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f4427-120">All required changes, bugs, or service improvements identified during the security incident response or postmortem activity are logged and tracked in an internal Microsoft engineering database.</span></span> <span data-ttu-id="f4427-121">Todos los posibles errores o características se asignan al propietario adecuado.</span><span class="sxs-lookup"><span data-stu-id="f4427-121">All potential bugs or features are assigned to the appropriate owner.</span></span> <span data-ttu-id="f4427-122">El equipo de respuesta de seguridad de Microsoft revisa todas las entradas hasta que se resuelve el problema.</span><span class="sxs-lookup"><span data-stu-id="f4427-122">The Microsoft security response team reviews all entries until the issue is resolved.</span></span>

## <a name="related-articles"></a><span data-ttu-id="f4427-123">Artículos relacionados</span><span class="sxs-lookup"><span data-stu-id="f4427-123">Related articles</span></span>

- [<span data-ttu-id="f4427-124">Administración de incidentes de seguridad de Microsoft</span><span class="sxs-lookup"><span data-stu-id="f4427-124">Microsoft security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="f4427-125">Administración de incidentes de seguridad de Microsoft: Preparación</span><span class="sxs-lookup"><span data-stu-id="f4427-125">Microsoft security incident management: Preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="f4427-126">Administración de incidentes de seguridad de Microsoft: detección y análisis</span><span class="sxs-lookup"><span data-stu-id="f4427-126">Microsoft security incident management: Detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="f4427-127">Administración de incidentes de seguridad de Microsoft: contención, eliminación y recuperación</span><span class="sxs-lookup"><span data-stu-id="f4427-127">Microsoft security incident management: Containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
- [<span data-ttu-id="f4427-128">Cómo registrar un vale de soporte de eventos de seguridad</span><span class="sxs-lookup"><span data-stu-id="f4427-128">How to Log a Security Event Support Ticket</span></span>](/azure/security/fundamentals/event-support-ticket)
- [<span data-ttu-id="f4427-129">Azure y Dynamics 365 notificación de infracciones bajo el GDPR</span><span class="sxs-lookup"><span data-stu-id="f4427-129">Azure and Dynamics 365 breach notification under the GDPR</span></span>](/compliance/regulatory/gdpr-breach-azure-dynamics)
