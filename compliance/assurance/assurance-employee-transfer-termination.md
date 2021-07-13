---
title: Transferencia y terminación de empleados de Microsoft
description: Obtenga información sobre el proceso de transferencia y terminación de empleados de Microsoft en Microsoft 365
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
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 862bd05a84e5144602a24ac2aca1780cffaff3fe
ms.sourcegitcommit: 48b8ec2dd00e957508e5af82458bf697e1a97ebb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/12/2021
ms.locfileid: "53395620"
---
# <a name="microsoft-employee-transfer-and-termination"></a>Transferencia y terminación de empleados de Microsoft

Microsoft, como cualquier otra organización, controla las transferencias y terminaciones de empleados como parte de su operación comercial normal. Cuando un empleado cambia de posición o deja la empresa, es esencial revocar el acceso inadecuado en tiempo y forma. Para facilitar cambios de acceso eficientes y revocaciones de acceso, Microsoft usa procedimientos estandarizados y procesos automatizados para coordinar el Sistema de información de recursos humanos (HRIS) con el sistema de administración de identidades (IDM). La orquestación automatizada entre estos dos sistemas es esencial para mantener la coherencia operativa, proteger los datos y los servicios en línea de Microsoft, evitar la pérdida de privilegios y reducir los riesgos relacionados con amenazas internas.

Los servicios en línea de Microsoft están diseñados para funcionar sin tener acceso administrativo permanente a entornos de producción para nuestros ingenieros. Microsoft usa un modelo Just-In-Time (JIT), Just-Enough-Access (JEA) para proporcionar a los ingenieros el acceso temporal necesario para admitir su servicio cuando sea necesario. Para solicitar y usar una cuenta de equipo de servicio para el acceso de JIT, los ingenieros deben solicitar y mantener los requisitos a través de la herramienta IDM. Cuando los empleados se transfieren o terminan, su cuenta de equipo de servicio y las elegibilidades relacionadas se modifican automáticamente para evitar un acceso inadecuado.

## <a name="transfer-and-reassignment"></a>Transferencia y reasignación

Las transferencias de empleados se inician a través de una solicitud de transacción de transferencia por parte del administrador del empleado. El administrador crea una solicitud de solicitud y se compromete con La adquisición global de talento para el proceso de carta de oferta. Una vez que el empleado acepta la oferta para el nuevo rol, los servicios de RRHH completan la transferencia en las herramientas principales de RRHH, lo que desencadena que IDM establezca una fecha de expiración para todas las elegibilidades del empleado. El empleado debe enviar una solicitud y recibir la aprobación de su nuevo administrador para conservar sus elegibilidades. Si no se envía una solicitud o se recibe la aprobación del administrador, se revocan los requisitos de los empleados transferidos. Para las transferencias que incluyen implicaciones de seguridad específicas, los accesos al sistema y las pertenencias a grupos de seguridad se reevaluan inmediatamente para reflejar su nuevo rol.

## <a name="termination"></a>Terminación

Microsoft usa directivas y procedimientos claramente definidos para revocar rápidamente el acceso físico y lógico a los sistemas y recursos de Microsoft cuando finaliza un empleado. Cuando un empleado da su aviso, el administrador del empleado escribe la fecha de terminación en el HRIS. Después del último día laborable del empleado, el HRIS marca al empleado como terminado y comparte la información con IDM, que quita automáticamente todas las cuentas y elegibilidad del equipo de servicio.

Para las terminaciones involuntarias, RRHH trabaja con el administrador del empleado para seguir los pasos adecuados para finalizar y salir del empleado. Al igual que una terminación voluntaria, la información de terminación se introduce en el HRIS junto con los pasos necesarios, como la coordinación de fechas efectivas, la eliminación del acceso. y cualquier otro paso relativo a la transición fuera del rol.
