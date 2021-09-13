---
title: Notificación de vulneración de seguridad de Azure, Dynamics 365 y Windows en virtud del RGPD
description: Le explicamos cómo Azure y Dynamics 365 protege contra una vulneración de datos personales y cómo Microsoft responde y le notifica si se produce una vulneración.
keywords: Azure, Microsoft 365, Dynamics 365, documentación de Microsoft 365, RGPD
ms.localizationpriority: high
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft GDPR
hideEdit: true
ms.openlocfilehash: 23d6b1ebb30f34fcb549e3e1f44c98a0c0e11b12
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160961"
---
# <a name="azure-dynamics-365-and-windows-breach-notification-under-the-gdpr"></a>Notificación de vulneración de seguridad de Azure, Dynamics 365 y Windows en virtud del RGPD

Microsoft toma muy en serio sus obligaciones sobre el Reglamento general de protección de datos (RGPD). Microsoft toma amplias medidas de seguridad en sus servicios en línea para protegerse de las infracciones de datos, incluidos controles de seguridad físicos y lógicos, así como la automatización de los procesos de seguridad, directivas de seguridad y privacidad de la información completas y formación en seguridad y privacidad para todo el personal.

La seguridad se integra en Microsoft Azure desde cero, comenzando con el [Ciclo de vida de desarrollo de seguridad](https://www.microsoft.com/sdl/), un proceso de desarrollo obligatorio que incorpora metodologías de privacidad por diseño y privacidad de forma predeterminada. El criterio rector de la estrategia de seguridad de Microsoft es "asumir la infracción" que es una extensión de la estrategia de defensa exhaustiva. Al poner a prueba capacidades de seguridad de Azure constantemente, Microsoft puede mantenerse por delante de las amenazas emergentes. Para obtener más información sobre la seguridad de Azure, revise estos [recursos](https://www.microsoft.com/trustcenter/security/azure-security).

Microsoft tiene un servicio de respuesta a incidentes 24/7 global adecuado para reducir los efectos de los ataques contra Microsoft Azure. Acreditado mediante varias auditorías de seguridad y cumplimiento (por ejemplo, [ISO/CEI 27018](offering-iso-27018.md)), Microsoft emplea operaciones y procesos de gran rigor en sus centros de datos para evitar el acceso no autorizado, incluidos la supervisión en vídeo 24/7, el personal de seguridad formado, las tarjetas inteligentes y los controles biométricos.

## <a name="detection-of-potential-breaches"></a>Detección de posibles vulneraciones

Debido a la naturaleza de la informática moderna en la nube, no todas las vulneraciones de datos que se ocurren en el entorno de la nube del cliente involucran a los servicios de Microsoft Azure. Microsoft utiliza un modelo de responsabilidad compartida para los servicios de Azure que define las responsabilidades operativas y de seguridad. La responsabilidad compartida es importante al tratar la seguridad de los servicios en la nube, ya que tanto el proveedor de servicios como el cliente son responsables de distintos aspectos de seguridad en la nube.

Microsoft no supervisa ni responde a los incidentes de seguridad responsabilidad del cliente. Una vulneración del cliente no puede tratarse como incidente de seguridad de Azure y es responsabilidad del inquilino del cliente administrar la respuesta. La respuesta al incidente del cliente puede implicar la colaboración con [atención al cliente](https://azure.microsoft.com/support/options/) de Microsoft Azure, según los contratos de servicio correspondientes. Microsoft Azure también ofrece varios servicios (por ejemplo, [Azure Security Center](https://azure.microsoft.com/services/security-center/)) que los clientes pueden utilizar para desarrollar y administrar la respuesta a incidentes de seguridad.

Azure responde a una posible vulneración de datos según el proceso de respuesta a incidentes de seguridad, un subconjunto del plan de administración de incidentes de Microsoft Azure. La respuesta de Microsoft a incidentes de seguridad de Azure se implementa con un proceso de cinco fases: detección, evaluación, diagnóstico, estabilización y cierre. El equipo de respuesta a incidentes de seguridad puede alternar entre las fases de diagnóstico y estabilización a medida que avanza la investigación. A continuación se expone información general sobre el proceso de respuesta a incidentes de seguridad:

| Etapa | Descripción |
|:------- |------------- |
| ***1: Detección*** | Primera indicación de un posible incidente. |
| ***2: Evaluación*** | Un miembro del equipo de respuesta ante incidentes evalúa el impacto y la gravedad del evento. Según las pruebas, la evaluación puede o no provocar una escalación al equipo de respuesta de seguridad. |
| ***3: Diagnóstico*** | Los expertos en respuestas de seguridad llevan a cabo la investigación técnica o forense, la identificación de estrategias de contención, la mitigación y la aplicación de soluciones alternativas. Si el equipo de seguridad cree que los datos del cliente pueden haberse expuesto a una ejecución individual ilegal o no autorizada, se inicia el proceso de notificación de incidentes del cliente de forma paralela. |
| ***4: Estabilización y recuperación*** | El equipo de respuesta ante incidentes crea un plan de recuperación para mitigar el problema. De forma inmediata y en paralelo al diagnóstico, pueden darse pasos de contención de crisis, como poner en cuarentena los sistemas afectados. Pueden planearse mitigaciones a largo plazo después de solucionar el riesgo inmediato. |
| ***5: Cierre y análisis posterior*** | El equipo de respuesta ante incidentes crea un análisis posterior que expone los detalles del incidente, con la intención de revisar directivas, procedimientos y procesos para evitar que el evento vuelva a producirse. |

Los procesos de detección usados por Microsoft Azure están diseñados para detectar sobre eventos que ponen en riesgo la integridad, confidencialidad y disponibilidad de los servicios de Azure. Algunas situaciones pueden desencadenar una investigación:

- Alertas del sistema automatizadas a través de marcos de supervisión y alerta internos. Estas alertas podrían estar en medio de alarmas basadas en firmas, como antimalware, detección de intrusiones o a través de algoritmos diseñados para generar perfiles de actividad esperada y alertar sobre anomalías.
- Informes internos de los servicios Microsoft ejecutándose en Microsoft Azure y Azure Government.
- Las vulnerabilidades de seguridad se notifican al [Centro de respuestas de seguridad de Microsoft (MSRC)](https://www.microsoft.com/msrc) a través de [Informa un problema](https://msrc.microsoft.com/create-report). El Centro de respuestas de seguridad de Microsoft trabaja con asociados e investigadores de seguridad de todo el mundo para impedir que se produzcan incidentes de seguridad y mejorar la seguridad de los productos de Microsoft.
- Los informes de cliente a través del [Portal de soporte técnico al cliente](https://www.windowsazure.com/support/contact/) o el portal de administración de Microsoft Azure y Azure Government, que describen la actividad sospechosa atribuida a la infraestructura de Azure (en lugar de la actividad que se produce en el ámbito de responsabilidad del cliente).
- Actividad de los [equipos de seguridad rojo y azul](https://azure.microsoft.com/blog/red-teaming-using-cutting-edge-threat-simulation-to-harden-the-microsoft-enterprise-cloud/). Esta estrategia usa un equipo Rojo de expertos altamente cualificados en seguridad ofensiva de Microsoft para descubrir y atacar debilidades potenciales en los servicios de Azure. El equipo Azul de respuesta de seguridad debe detectar la actividad del equipo rojo y defenderse contra ella. Las acciones de los equipos Rojo y Azul se usan para comprobar que los esfuerzos de respuesta de seguridad de Azure son efectivos a la hora de administrar incidentes de seguridad. Las actividades de los equipos de seguridad Rojo y Azul se basan en las reglas de compromiso para garantizar la protección de los datos de clientes.
- Remisiones por parte de los operadores de servicios de Azure. Los empleados de Microsoft están preparados para identificar y remitir los posibles problemas de seguridad a instancias superiores.

## <a name="azures-data-breach-response"></a>Respuesta de infracción de datos de Azure

Microsoft asigna la prioridad y los niveles de gravedad adecuados a la investigación al determinar el impacto funcional, la capacidad de recuperación y el impacto de la información del incidente. Tanto la prioridad como la gravedad pueden cambiar a lo largo de la investigación en función de las conclusiones y de nuevos hallazgos. Los eventos de seguridad que implican riesgo inminente o confirmado para los datos del cliente son tratados como graves y se trabaja en ellos de forma ininterrumpida para resolverlos.

El equipo de respuesta de seguridad trabaja con los ingenieros de seguridad de Microsoft Azure y PYME para clasificar el evento con datos reales de las pruebas. Un evento de seguridad se puede clasificar como:

- **Falso positivo**: un evento que cumple los criterios de detección, pero que forma parte de un procedimiento normal del negocio y es preciso filtrarlo. Los equipos de servicio identifican la causa de los falsos positivos y los solucionan de forma sistemática ajustándolos según sea necesario.
- **Evento de seguridad**: una actividad repetida observable en un sistema, servicio o red de intento de ataque, eliminación de los controles de seguridad o problema identificado en el que los hechos indican que los datos del cliente o los datos personales pueden haberse perdido, destruido, modificado, divulgado o accedido sin autorización.
- **Incidente de seguridad o Incidente de seguridad/privacidad notificado por el cliente (CRSPI)**: infracción de seguridad confirmada (por ejemplo, declarada) que conduce a la destrucción (accidental o ilegal), pérdida, modificación, divulgación no autorizada o acceso a los datos de los clientes o datos personales mientras Microsoft los procesa.
- **Evento de privacidad**: un evento de seguridad que afecta a los datos personales o al procesamiento de datos que da lugar a consecuencias no deseadas para la privacidad y que incluye el incumplimiento de las directivas, los estándares y los controles de privacidad de Microsoft.
- **Incidente de privacidad o Incidente de seguridad/privacidad notificado por el cliente (CRSPI)**: incidente de seguridad que afecta a los datos personales, los datos o el procesamiento de datos y que da lugar a consecuencias no deseadas para la privacidad. Esto incluye el incumplimiento de las directivas, los estándares y los controles de privacidad de Microsoft.

Para que se declare un CRSPI, Microsoft debe determinar que se haya producido o que sea posible que se produzca un acceso no autorizado a los datos del cliente, o que exista un compromiso legal o contractual de que deba producirse la notificación. Es deseable, aunque no es necesario, que se conozcan los pasos específicos de impacto en el cliente, del acceso a los recursos y de la reparación. Por lo general, un incidente se declara como CRSPI después de la conclusión de la fase de diagnóstico de un incidente de seguridad. Sin embargo, la declaración puede producirse en cualquier momento en el que toda la información pertinente esté disponible.

Microsoft comprueba que el riesgo para los clientes y negocios se ha contenido con éxito y que las medidas correctivas se han implementado. En caso necesario, se llevan a cabo pasos de atenuación de emergencia para resolver los riesgos de seguridad inmediatos asociados con el evento.

Microsoft también realiza un análisis final interno para las vulneraciones de datos. Como parte de este ejercicio, se evalúan los procedimientos operativos y la suficiencia de la respuesta, y se identifican e implementan las actualizaciones necesarias para la SOP de respuesta ante incidencias de seguridad o los procesos relacionados. Los análisis finales internos para las infracciones de datos son registros altamente confidenciales que no están disponibles para los clientes. Los análisis finales pueden, sin embargo, resumirse e incluirse en otras notificaciones de eventos del cliente. Estos informes se proporcionan a auditores externos para su revisión como parte del ciclo de auditoría rutinario de Azure.

## <a name="customer-notification"></a>Notificación al cliente

Microsoft Azure notifica de las vulneraciones de datos a los clientes afectados y a los organismos reguladores, según sea necesario. Microsoft depende de una gran compartimentación interna en la operación de Azure. Los registros de flujo de datos también son sólidos. Una ventaja de este diseño es que la mayoría de incidentes pueden rastrearse hasta clientes específicos. El objetivo es proporcionar a los clientes afectados un aviso preciso, puntual y efectivo cuando hayan sufrido una vulneración de datos.

Tras la declaración de un CRSPI, el proceso de notificación tiene lugar tan pronto como sea posible, pero hay que considerar los riesgos de seguridad de actuar demasiado rápido. Por lo general, se comienza a redactar las notificaciones durante la investigación de la incidencia. Los avisos a los clientes se entregan en no más de 72 horas desde el momento en que se declaró una vulneración, *excepto* en las siguientes circunstancias:

- Microsoft considera que el acto de realizar una notificación incrementará el riesgo para otros clientes. Por ejemplo, el acto de enviar una notificación puede alertar al adversario e impedir la corrección adecuada.
- Otras circunstancias poco frecuentes o extremas determinadas por el departamento jurídico de Microsoft y por el director ejecutivo de incidentes.
- El plazo de 72 horas puede permitir que algunos detalles del incidente estén disponibles. Estos se proporcionan a los clientes y a las autoridades de reglamentación mientras avanza la investigación.

Microsoft Azure proporciona a los clientes información detallada, lo que les permite realizar investigaciones internas y ayudar a cumplir los compromisos de usuario final, mientras no retrase indebidamente el proceso de notificación.

La notificación de una vulneración de datos personales se entregará al cliente por cualquier medio elegido por Microsoft, incluido el correo electrónico. La notificación de una vulneración de datos se enviará a la lista de contactos de seguridad proporcionada en Azure Security Center, que puede configurarse siguiendo las [directrices de implementación](/azure/security-center/security-center-provide-security-contact-details). Si no se proporciona información de contacto en el centro de seguridad de Azure, la notificación se envía a uno o varios administradores de una suscripción de Azure. Para asegurar que la notificación pueda entregarse correctamente, es responsabilidad del cliente proporcionar información de contacto administrativa correcta en cada suscripción y portal de servicios en línea aplicables.

El equipo de Microsoft Azure o de Azure Government también puede elegir notificar a otro personal de Microsoft, como los miembros del equipo de Servicio de atención al cliente (CSS) de Microsoft y el Administrador de cuentas (AM) o el Administrador de cuentas técnicas (TAM) del cliente. Estos individuos a menudo tienen una relación cercana con el cliente y pueden facilitar una corrección más rápida.

## <a name="microsoft-dynamics-365-built-in-security-features"></a>Características de seguridad integradas en Microsoft Dynamics 365

Microsoft Dynamics 365 usa la infraestructura de servicios en la nube y las características de seguridad integradas para garantizar la integridad de los datos con medidas de seguridad y mecanismos de protección. Además, Dynamics 365 ofrece acceso a datos y colaboración eficientes con integridad de los datos y privacidad en las áreas siguientes: [identidad segura, protección de datos, seguridad basada en roles y administración de amenazas](https://www.microsoft.com/trustcenter/security/dynamics365-security).

La oferta de Microsoft Dynamics 365 sigue las mismas medidas técnicas y de organización que los equipos del servicio de Microsoft Azure llevan a cabo para proteger contra posibles vulneración de datos. Por tanto, cualquier información registrada en el documento de notificación "Vulneración de datos de Microsoft Azure" es en este caso también aplicable al servicio de Microsoft Dynamics 365.

## <a name="windows-diagnostic-data-processor-configuration"></a>Configuración del encargado de los datos de diagnóstico de Windows

La [Configuración del encargado de los datos de diagnóstico de Windows](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) aprovecha la infraestructura de servicios en la nube y las características de seguridad integradas para proteger los datos mediante medidas y mecanismos de seguridad para proteger los datos.

Sigue las mismas medidas técnicas y de organización que los equipos del servicio de Microsoft Azure llevan a cabo para proteger contra la posible vulneración de datos. Por lo tanto, toda la información documentada en el documento de notificación "Vulneración de datos de Microsoft Azure" también es análoga a la configuración del encargado de los datos de diagnóstico de Windows.

## <a name="learn-more"></a>Más información

[Centro de confianza de Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
