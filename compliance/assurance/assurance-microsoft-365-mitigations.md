---
title: Microsoft 365 para mitigaciones de administración de continuidad empresarial
description: Algunos ejemplos de mitigaciones para escenarios de incidentes del servicio de Microsoft 365.
author: robmazz
ms.author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
f1.keywords:
- NOCSH
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 5f88f9b5b3dee2279e37bee5137819802f68502d163e4eaa1f75c3abf57a4c53
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "54290649"
---
# <a name="service-incident-mitigation-strategies"></a>Estrategias de mitigación de incidentes del servicio

Estas son algunas estrategias y escenarios que muestran cómo mitigar el impacto de un incidente del servicio de Microsoft 365 en el proceso empresarial.

## <a name="service-incident-scenarios-and-potential-mitigations"></a>Escenarios de incidentes del servicio y posibles mitigaciones

|Dependencia de Microsoft 365|posibles mitigaciones|
|---------|---------|
|El sistema de Administración de Incidencias se basa en Exchange Online para conectar a Ingenieros de Guardia y Administradores de Incidentes.|Asegúrese de que el sistema de Administración de Incidentes es compatible con las comunicaciones multicanales, como el correo electrónico paralelo, las llamadas de teléfono, las notificaciones de SMS y las jerarquías de árbol de llamadas. En caso de que la primera llamada principal no se establezca, el sistema automáticamente activará la copia de seguridad. Incluya también métodos de contacto para la copia de seguridad en cada notificación, de modo que los métodos de comunicación de respaldo estén integrados para una fácil referencia. Los métodos de comunicación alternativos, como Yammer, se pueden usar para la colaboración de emergencia si el servicio de administración de incidencias no está disponible.|
|Microsoft Teams se usa para almacenar archivos a los que se accede a través del cliente.|Teams almacena los archivos cargados en el cliente en una biblioteca de documentos de SharePoint Online. Los archivos aún son accesibles a través de SharePoint Online. Capacite a los usuarios en ubicaciones de archivos en SharePoint Online.|
|Las llamadas de conferencia de Microsoft Teams son un servicio confiable para la comunicación general y la evaluación de la administración de incidentes.|Establezca una solución de respaldo para conferencias con un proveedor de terceros.|
|Los teléfonos VoIP se usan como métodos de comunicación secundarios.|Implemente teléfonos no compatibles con VoIP, capaces de realizar llamadas RTC, especialmente para centros de operaciones de red y servicios durante los incidentes. Agregar los números de teléfono móvil de empleados al directorio de la empresa para que el personal importante puede ser contactado a través de la red móvil.|
|OneDrive para la Empresa es un servicio confiable para el almacenamiento de archivos y la productividad de los usuarios. [Archivos a petición](https://techcommunity.microsoft.com/t5/Microsoft-OneDrive-Blog/OneDrive-Files-On-Demand-For-The-Enterprise/ba-p/117234) se configura para liberar espacio en las unidades de usuario locales.|La sincronización de OneDrive proporciona directivas de grupo que permiten a los administradores solicitar que un contenido específico se sincronice localmente o liberar espacio cuando se desee. Para mitigar el riesgo de inaccesibilidad del documento, configure esta directiva para sincronizar localmente los documentos importantes. Capacite a los usuarios para aplicar manualmente la configuración "mantener siempre en este dispositivo" para los documentos clave.|
|La comunicación de las alteraciones del negocio a los clientes y proveedores depende de Exchange Online.|Las redes sociales de terceros pueden usarse como medio alternativo de comunicación masiva.
|La arquitectura híbrida local, como ADFS o Pass Through Autenticación, falla y causa interrupciones en la capacidad del usuario para autenticarse en los servicios en la nube.|Configure [Password Hash Sync](/azure/active-directory/authentication/concept-resilient-controls#deploy-password-hash-sync-even-if-you-are-federated-or-use-pass-through-authentication), junto con sus servicios de autenticación híbrida, como un mecanismo secundario de autenticación basado en la nube para evitar la interrupción del inicio de sesión durante la interrupción. [Consulte Crear una estrategia de administración de control de acceso resistente con Azure Active Directory](/azure/active-directory/authentication/concept-resilient-controls) para obtener más información sobre cómo crear una autenticación resistente y arquitecturas de control de acceso.|  

## <a name="leveraging-mobile-app-access"></a>Aproveche el acceso a las aplicaciones móviles

A medida que el uso móvil ha proliferado, existen nuevos medios para mantenerse conectado y las aplicaciones móviles de Microsoft 365 pueden ser una parte clave de la estrategia de resiliencia. Debido a que se conectan a los servicios en la nube mediante la red de proveedor de telefonía móvil, no dependen de la infraestructura de red de su organización.

Comencemos por usar Outlook como ejemplo. Los usuarios se pueden conectar a sus buzones de Exchange Online a través de diferentes protocolos de red (https o MAPI) según la aplicación de correo electrónico que se utilice. Si hay un incidente del servicio que involucra uno de los protocolos, digamos MAPI, que utiliza el cliente de escritorio, los usuarios podrán seguir teniendo acceso a su buzón a través de la aplicación Móvil de Outlook o de Outlook en la Web.
  
Si decide permitir que los usuarios se conecten a los servicios de Microsoft 365 mediante sus dispositivos móviles, puede usar Microsoft Intune para configurar y administrar esos dispositivos de forma segura. Una vez que las cuentas y los dispositivos de los usuarios se inscriban en la solución de administración móvil, asegúrese de que se hayan descargado y configurado las aplicaciones.
