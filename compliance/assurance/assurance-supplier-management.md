---
title: Información general sobre administración de suministros
description: Información sobre la administración de proveedores en Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH'
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 73ec8ca99f880a3c6277bd917dab99b9aff49999
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496697"
---
# <a name="supplier-management-overview"></a>Información general sobre administración de suministros

## <a name="how-does-microsoft-manage-risk-related-to-suppliers"></a>¿Cómo administra Microsoft los riesgos relacionados con los proveedores?

Microsoft se asocia con compañías de terceros para ayudar a satisfacer las necesidades de nuestros clientes. Estas compañías de terceros se denominan proveedores o subprocesadores. La seguridad y privacidad de los proveedores en Microsoft se rige por nuestro programa De seguridad y privacidad de proveedores [(SSPA),](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)un conjunto de requisitos de toda la empresa para que todos los proveedores asociados con Microsoft entreguen nuestros servicios en línea. Aunque el programa SSPA proporciona un gobierno y una administración integrales de nuestra base de proveedores, las unidades de negocio individuales, como Microsoft 365, pueden mantener requisitos adicionales para sus proveedores.

## <a name="how-does-microsofts-supplier-security-and-privacy-assurance-sspa-program-protect-customer-data"></a>¿Cómo protege el Programa de seguridad y privacidad de proveedores (SSPA) de Microsoft los datos de los clientes?

SSPA es una asociación entre Microsoft Procurement, Corporate External and Legal Affairs y Corporate Security para garantizar que los proveedores cumplan los principios de privacidad y seguridad de Microsoft. El ámbito de SSPA abarca todos los proveedores que procesan datos personales o datos confidenciales de Microsoft. La inscripción del programa SSPA incluye el cumplimiento de los requisitos de protección de datos (DPR) de Microsoft. La DPR consiste en controles de seguridad y privacidad que los proveedores deben implementar antes de comenzar el trabajo contratado con Microsoft. Todos los proveedores inscritos autoatestan el cumplimiento de la RPD anualmente.

Los requisitos de DPR se basan en seis categorías distintas de procesamiento de datos para las que un proveedor puede aprobarse como parte de su inscripción en SSPA. Estas categorías se usan para identificar el riesgo asociado con los servicios que un proveedor proporciona a Microsoft. El perfil de procesamiento de datos del proveedor determina qué controles DPR se consideran en el ámbito para proporcionar la protección de datos adecuada. Los proveedores que procesan datos que se consideran de mayor riesgo deben cumplir con todos los requisitos de DPR y también deben proporcionar una comprobación independiente del cumplimiento. Las herramientas de compra de Microsoft validan el estado de SSPA de todos los proveedores, incluido el cumplimiento de las partes aplicables de la RPD, antes de permitir la adquisición de ese proveedor.

## <a name="what-types-of-subprocessors-provide-services-for-microsoft"></a>¿Qué tipos de subprocesadores proporcionan servicios para Microsoft?

Un "subprocesador" es un tercero al que Microsoft participa, cuyas funciones incluyen el procesamiento de datos personales de Microsoft para los que Microsoft es un procesador. Los subprocesadores de Microsoft se divide en tres categorías distintas. Cada uno debe demostrar el cumplimiento con el SSPA antes de poder procesar los datos de los clientes en nombre de Microsoft.

- **Los** subprocesadores tecnológicos proporcionan tecnologías usadas para ofrecer servicios en línea específicos de Microsoft. Si un cliente implementa uno de estos servicios, los subprocesadores identificados para ese servicio pueden procesar, almacenar o tener acceso a datos personales o datos personales de los clientes mientras ayudan a proporcionar ese servicio.
- **Los subprocesadores** auxiliares proporcionan servicios que admiten, operan y mantienen los servicios en línea. Si un cliente implementa uno de estos servicios, los subprocesadores identificados pueden procesar, almacenar o tener acceso a datos personales o datos personales limitados mientras proporcionan sus servicios auxiliares.
- **Los subprocesadores** de aumento de personal tienen dos formas diferentes: en ambos escenarios, los datos personales residen solo en instalaciones de Microsoft, en sistemas Microsoft y están sujetos a directivas y supervisión de Microsoft.

    - La primera forma de aumento de personal proporciona personal que admite, opera y mantiene los servicios en línea de Microsoft. Mientras se cumplen sus responsabilidades, estos subprocesadores pueden exponerse a datos de clientes o datos personales. Por ejemplo, un subprocesador puede realizar la solución remota de problemas en un servidor microsoft y, al hacerlo, puede exponerse a fragmentos de datos de clientes en un registro de volcado de memoria del servidor.
    - La segunda forma de aumento de personal implica subprocesadores que trabajan en paralelo con los empleados a tiempo completo de Microsoft para admitir, operar y mantener los servicios en línea de Microsoft. Estos subprocesadores pueden exponerse a datos seudonimizados como parte de su trabajo junto con los empleados a tiempo completo de Microsoft.

La tecnología y los subprocesadores auxiliares son necesarios para implementar controles de acceso de acuerdo con los requisitos de protección de datos (DPR) de Microsoft. Estos requisitos cumplen o superan los compromisos contractuales que Microsoft realiza con sus clientes en los Términos de servicio en línea (OST). Los proveedores que realizan trabajos de aumento de personal están sujetos a los mismos controles de acceso para los empleados a tiempo completo de Microsoft.

## <a name="how-does-microsoft-onboard-suppliers"></a>¿Cómo incorpora Microsoft proveedores?

Los proveedores de terceros deben firmar un contrato maestro de Microsoft como parte del proceso de incorporación. Este contrato rige la relación entre Microsoft y sus proveedores y garantiza una administración coherente de las relaciones de los proveedores. Como parte de la incorporación, los proveedores se inscriben en el SSPA y deben completar todos los requisitos aplicables antes de poder aprobarse para cualquier categoría de procesamiento de datos. Las unidades de negocio de Microsoft solo pueden crear interacciones con los proveedores cuando la actividad de procesamiento de datos de la interacción coincide con las categorías de procesamiento de datos para las que el proveedor ha sido aprobado.

## <a name="how-does-microsoft-notify-customers-of-changes-to-suppliers-who-process-their-data"></a>¿Cómo notifica Microsoft a los clientes los cambios en los proveedores que procesan sus datos?

Según el Addendum de Protección de datos del servicio en línea de Microsoft (DPA), Microsoft realiza compromisos adicionales con respecto a los períodos de aviso para la adición de cualquier subprocesador. Observe que los plazos dependen del tipo de datos que el subprocesador procesará en nombre de Microsoft. Como se indica en el DPA, Microsoft se compromete a proporcionar aviso a los clientes al menos seis meses antes de cualquier nuevo subprocesador que procesará los datos del cliente. Para cualquier otro dato personal, Microsoft proporcionará al menos 30 días de aviso. La actualización de la lista de [subprocesadores Microsoft Online Services aviso.](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=926b2cf5-6b6e-43ca-9bc3-f73e961aad5f&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Subprocessor_List)

## <a name="related-external-regulations--certifications"></a>Normativas externas relacionadas & certificaciones

Los servicios en línea de Microsoft se auditan periódicamente para cumplir con las normativas y certificaciones externas. Consulte la tabla siguiente para la validación de controles relacionados con la administración de proveedores.

| **Auditorías externas** | **Section** | **Fecha de informe más reciente** |
|:--------------------|:------------|:-----------------------|  
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CA-3: Interconexiones del sistema <br> IA-4: Administración de identificadores <br> PS-6: Acuerdos de acceso <br> PS-7: Seguridad del personal de terceros <br> SA-4: Proceso de adquisiciones <br> SA-9: Servicios del sistema de información externa <br> SA-12: Protección de la cadena de suministro | 24 de septiembre de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: Seguridad de la información en las relaciones con proveedores | 22 de febrero de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: Seguridad de la información en las relaciones con proveedores | 22 de febrero de 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaración de aplicabilidad](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificación](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) |  A.8.1: Divulgación del procesamiento de PII subcontratado | 24 de diciembre de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-53: Supervisión de terceros | 24 de diciembre de 2020 |

## <a name="resources"></a>Recursos

- [Programa de seguridad y privacidad de proveedores](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)
