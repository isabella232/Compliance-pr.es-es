---
title: Asegurando la infraestructura de Microsoft 365
description: Obtenga información sobre cómo Microsoft protege la Microsoft 365 de seguridad.
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
hideEdit: true
ms.openlocfilehash: d0ef6dc92820089259cd315713c0e7e4a9e11aaec50d731b15cd6e826a721107
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292757"
---
# <a name="securing-the-microsoft-365-infrastructure"></a>Asegurando la infraestructura de Microsoft 365

Microsoft 365 es uno de los servicios en la nube de consumo y empresa más grandes del mundo y sigue creciendo rápidamente, tanto en la base de clientes, productos y características. Los clientes se Microsoft 365 no solo por sus soluciones de productividad de clase mundial, sino para ayudar a proteger su información más confidencial del panorama de amenazas cibernéticas en constante evolución. La prioridad principal de Microsoft es mantener la seguridad de los datos de los clientes y mantener la confianza del cliente.

Proteger un sistema de esta escala y complejidad no es posible si la seguridad es una sucesión posterior, solo es eficaz si la seguridad se integra durante el proceso de diseño inicial. Requiere un sistema sólido de detección de amenazas con respuestas rápidas tanto de sistemas automatizados como de ingenieros altamente cualificados. La evaluación y validación continuas de estos sistemas es esencial para garantizar que las configuraciones seguras permanezcan intactas y se identifiquen vulnerabilidades desconocidas anteriormente.

## <a name="core-security-principles"></a>Principios básicos de seguridad

Siete principios de seguridad basan nuestro  marco en proteger los servicios de Microsoft 365 frente a *amenazas,* detectar y responder a amenazas, y evaluar continuamente la posición de seguridad y mejorar los servicios en función de los resultados de dichas evaluaciones. 

- **Privacidad de datos:** los clientes son propietarios de sus datos y Microsoft es el administrador. Microsoft 365 los servicios están diseñados para funcionar sin que los ingenieros accedan a los datos de los clientes, a menos que el cliente lo solicite y apruebe explícitamente.
- **Asuma la infracción:** el personal y los servicios se tratan como si el riesgo es una posibilidad real.
- **Privilegios mínimos:** el acceso y los permisos a los recursos solo se limitan a lo necesario para realizar las tareas necesarias.
- **Límites de vulneración:** las identidades y la infraestructura de un límite se aíslan de los recursos de otros límites. La transacción de un límite no debe llevar a un riesgo de otro.
- **Seguridad integrada de Service Fabric:** las prioridades y los requisitos de seguridad se integran en el diseño de nuevas características y capacidades, lo que garantiza que una postura de seguridad sólida se escala con cada servicio.
- **Automatizado** y automático: Microsoft se centra en desarrollar arquitecturas y productos duraderos que puedan aplicar de forma inteligente y automática la seguridad del servicio, al tiempo que ofrece a los ingenieros de Microsoft la capacidad de administrar de forma segura las respuestas a las amenazas de seguridad a escala.
- **Seguridad adaptable:** las capacidades de seguridad de Microsoft se adaptan y se mejoran mediante modelos de aprendizaje automático, pruebas de penetración rutinarias y evaluaciones automatizadas.

## <a name="protection"></a>Protección

### <a name="access-control"></a>Control de acceso

De forma predeterminada, el personal responsable del desarrollo y mantenimiento de Microsoft 365 servicios tienen acceso permanente cero (ZSA) a la infraestructura de servicio. Aunque Microsoft se esfuerza por contratar solo a los mejores ingenieros y se requieren rigurosas comprobaciones de antecedentes, Microsoft no asume que son de confianza de forma predeterminada en los servicios operativos. Además, cuando los ingenieros se aprueban para el acceso con privilegios, solo se les concede acceso durante una duración limitada para realizar solo las acciones necesarias para un ámbito específico de la infraestructura de servicio. Microsoft hace referencia a estas directivas como Just-in-Time (JIT) y Just-Enough-Access (JEA) que se implementan a través de un sistema denominado Lockbox.

Para obtener privilegios elevados, los ingenieros de Microsoft envían una solicitud para la tarea específica y especifican el período de tiempo para realizarla. Una vez aprobado, Lockbox genera una cuenta JIT especializada con la capacidad de realizar solo la tarea solicitada. Las acciones suelen tener la forma de flujos de trabajo automatizados que realizan de forma segura cualquier solución de problemas o recuperación necesaria. En raras ocasiones cuando es necesario tener acceso directo a la infraestructura, se requieren estaciones de trabajo de acceso privilegiado (PAW) estrictamente supervisadas.

Los usuarios no autorizados y las cuentas comprometidas son una posibilidad real en cualquier organización y nuestro sistema de control de acceso está diseñado para protegerse contra estas amenazas.

Para obtener más información sobre el control de acceso, vea [Identity and access management overview](assurance-identity-and-access-management.md).

### <a name="encryption"></a>Cifrado

Aunque los controles de acceso proporcionan un rol fundamental en la defensa de los servicios Microsoft 365, el cifrado se usa durante todo el ciclo de vida de los datos para proteger aún más la confidencialidad y la privacidad de los clientes de Microsoft.

Los datos en tránsito entre máquinas cliente, Microsoft 365 servidores y servidores que no Microsoft 365 se cifran mediante TLS 1.2. Periódicamente, se revisan los cifrados y protocolos en uso, agregando protocolos mejorados cuando están disponibles y quitando los más débiles según sea necesario.

El contenido del cliente en reposo en los servidores de Microsoft se cifra en el nivel de volumen mediante BitLocker. El cifrado a nivel de aplicación también se puede aplicar mediante claves administradas por Microsoft o el cliente. El acceso a las claves administradas por Microsoft solo es posible cuando se autoriza y aprueba a través del proceso JIT y JEA.

Para obtener más información acerca del cifrado en Microsoft 365, vea [Encryption and key management overview](assurance-encryption.md).

### <a name="network-isolation"></a>Aislamiento de red

De acuerdo con el principio de privilegios mínimos, Microsoft 365 limita la comunicación entre diferentes partes de la infraestructura de servicio a solo lo que es necesario para funcionar. De forma predeterminada, se deniega todo el tráfico de red y solo se permite la comunicación definida explícitamente. Esta restricción establece límites de vulneración en toda la infraestructura. Teams que quiera agregar nuevas rutas de red para dar cabida a una nueva característica a su servicio debe tener la solicitud evaluada y aprobada antes de que se pueda abrir.

Para obtener más información sobre el aislamiento de red en Microsoft 365, vea [Microsoft 365 de aislamiento](/microsoft-365/enterprise/microsoft-365-isolation-controls).

## <a name="detection--response"></a>Detección & respuesta

### <a name="security-monitoring"></a>Supervisión de seguridad

La supervisión de seguridad en la escala masiva de Microsoft solo es posible mediante la generación de alertas de alta precisión mediante soluciones automatizadas basadas en la nube. Los registros de auditoría de cada servicio y datos de telemetría recopilados desde toda la infraestructura principal se envían a una solución de alertas y procesamiento centralizados casi en tiempo real.

Las amenazas detectadas se corrigen mediante acciones desencadenadas automáticamente cuando es posible. Cuando las soluciones automatizadas no tienen éxito o no pueden resolver el problema, los ingenieros de Microsoft de llamadas inmediatamente toman medidas para mitigar la amenaza.

Para obtener más información acerca de la supervisión de seguridad en Microsoft 365, vea [Security monitoring overview](assurance-security-monitoring.md).

## <a name="assessment"></a>Evaluación

### <a name="automated-assessments"></a>Evaluaciones automatizadas

Independientemente de cómo se diseñe un sistema, la postura de seguridad puede degradarse debido a una deriva de configuración intencionada e involuntaria con el tiempo. Las herramientas automatizadas evalúan Microsoft 365 los sistemas que buscan servicios no configurados y no configurados. Esta evaluación a menudo se conoce como revisión, antivirus, vulnerabilidad y análisis de configuración (PAVC).

Nuestra arquitectura también se valida con frecuencia, identificando instancias como puertos abiertos sin usar y cuentas con acceso administrativo permanente. Los servicios que se derivan de un estado deseado predefinido se volverán a alinear automáticamente.

Para obtener más información acerca de la supervisión de seguridad en Microsoft 365, vea [Vulnerability management overview](assurance-vulnerability-management.md).

### <a name="attack-simulation-and-penetration-testing"></a>Simulación de ataques y pruebas de penetración

Microsoft 365 prioridad principal es evitar que los ataques se infiltren en las defensas. Microsoft 365 un equipo dedicado de expertos en seguridad que realizan constantemente ataques simulados para identificar vulnerabilidades desconocidas previamente y para proporcionar una secuencia constante de datos enriquecidos para mejorar las capacidades de supervisión de seguridad. Estos ataques simulados toman la forma de ataques a pequeña escala automatizados frecuentes y de inmersiones profundas controladas por expertos. A partir de estas actividades, Microsoft evalúa la capacidad de detectar, responder y desalojar a los atacantes.

Para obtener más información acerca de la supervisión de seguridad en Microsoft 365, vea [Attack simulation in Microsoft 365](assurance-monitoring-and-testing.md).

## <a name="resources"></a>Recursos

[Entre bastidores: protección de la infraestructura que impulsa el servicio Microsoft 365](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
