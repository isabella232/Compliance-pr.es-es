---
title: Seguridad de acceso físico del centro de datos
description: Obtenga más información sobre la seguridad de acceso físico del centro de datos de Microsoft.
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
ms.openlocfilehash: f7cc71354c4be52d97c8b4b6efbe5a88ca9413a5
ms.sourcegitcommit: cf424cb1e7c12048120977f294f780b776119a96
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/11/2021
ms.locfileid: "60265141"
---
# <a name="datacenter-physical-access-security"></a>Seguridad de acceso físico del centro de datos

Microsoft comprende la importancia de proteger los datos de los clientes y se compromete a proteger los centros de datos que los contienen. Los centros de datos de Microsoft están diseñados, creados y operados para limitar estrictamente el acceso físico a las áreas donde se almacenan los datos de los clientes.

La seguridad física en los centros de datos está alineada con el principio de defensa en profundidad. Se implementan varias medidas de seguridad para reducir el riesgo de que usuarios no autorizados accedan a datos y otros recursos del centro de datos.

- **Seguridad perimetral:** los centros de datos de Microsoft son edificios no descriptos con cercado perimetral e iluminación exterior las 24 horas. Las cercas altas de acero y concreto abarcan cada centímetro del perímetro y toda la entrada al campus del centro de datos debe pasar por un punto de acceso bien definido. Las puertas de entrada se encuentran vigiladas por cámaras y las patrullas de seguridad garantizan que la entrada y salida queden restringidas a las áreas designadas. Los bolardos y otras medidas protegen el exterior del centro de datos frente a posibles amenazas, incluido el acceso no autorizado.
- **Entrar en el centro de datos:** la entrada del centro de datos está equipada con agentes de seguridad profesionales que han sido sometidos a rigurosas comprobaciones de formación y antecedentes. Los agentes de seguridad supervisan de forma rutinaria el centro de datos y las fuentes de vídeo de las cámaras dentro del centro de datos siempre se supervisan.
- **Dentro del centro de datos:** al entrar en el edificio, se requiere la autenticación en dos fases con biometría para seguir moviéndose por el centro de datos. Una vez autenticado, se concede acceso a la parte autorizada del centro de datos y solo durante el tiempo aprobado. Dentro del centro de datos, las áreas designadas como extremadamente confidenciales requieren autenticación adicional en dos fases.
- **Planta del centro de** datos: solo se puede acceder al piso del centro de datos con aprobación previa y después de un examen de detección de metal de cuerpo completo en el momento de la entrada. Para reducir el riesgo de que los datos no autorizados entren o abandonen el centro de datos, solo los dispositivos aprobados pueden llegar a la planta del centro de datos. Además, las cámaras de vídeo supervisan la parte frontal y posterior de cada bastidor del servidor. Al salir del centro de datos, todos los individuos están sujetos a un examen adicional de detección de metal de cuerpo completo.
- **Salir del centro de** datos: para salir de la instalación del centro de datos, cada persona debe pasar por un punto de control de seguridad final y todos los visitantes deben entregar sus distintivos temporales. Después de la recopilación, se quitan todos los niveles de acceso a todos los distintivos de visitante antes de volver a usarlos para futuras visitas.

## <a name="access-provisioning"></a>Aprovisionamiento de acceso

El equipo de administración de centros de datos (DCM) ha implementado procedimientos operativos para restringir el acceso físico solo a los empleados, contratistas y visitantes autorizados. Se realiza un seguimiento de las solicitudes de acceso temporales o permanentes mediante un sistema de vales. Los distintivos se emiten o se activan para el personal que requiere acceso después de comprobar la identificación. Las claves físicas y los distintivos de acceso temporales se protegen en el Centro de operaciones de seguridad (SOC).

Los centros de datos de Microsoft están sujetos a una directiva de acceso con privilegios mínimos, lo que significa que el acceso al centro de datos está restringido al personal con una necesidad empresarial aprobada, sin más acceso del necesario. Las solicitudes de acceso tienen un límite de tiempo y solo se renuevan si la necesidad empresarial del solicitante sigue siendo válida.

Los registros de acceso al centro de datos se mantienen en forma de solicitudes aprobadas. Las solicitudes solo pueden ser aprobadas por el equipo de DCM y las solicitudes de acceso de visitantes a centros de datos se registran y se hacen disponibles para futuras investigaciones

## <a name="datacenter-security-personnel"></a>Personal de seguridad del centro de datos

El personal de seguridad en todas las instalaciones del centro de datos y el campus son responsables de las siguientes actividades:

- Operar estaciones de trabajo ubicadas en el Centro de operaciones de seguridad dentro del edificio de administración principal.
- Realice inspecciones periódicas a través de los tutoriales de las instalaciones y las patrullas de los terrenos.
- Responder a alarmas de incendio y problemas de seguridad
- Enviar personal de seguridad para ayudar a las solicitudes de servicio y emergencias
- Proporcionar al equipo de administración de centros de datos actualizaciones periódicas sobre los eventos de seguridad y los registros de entrada
- Operar y supervisar sistemas de alarma, control de acceso y vigilancia

## <a name="visitor-access"></a>Acceso de visitantes

La comprobación de seguridad y la protección son necesarias para el personal que requiere acceso temporal al interior de la instalación del centro de datos, incluidos los grupos de visitas y otros visitantes. Los visitantes del centro de datos deben firmar un acuerdo de confidencialidad, someterse a una revisión por parte de la administración del centro de datos y obtener la aprobación de la administración del centro de datos antes de su visita programada. A su llegada, se procesa a los visitantes del centro de datos con credenciales de acceso temporal con privilegios mínimos. Además, durante la visita, se les asigna un empleado a tiempo completo (FTE) de Microsoft o designado autorizado aprobado por la administración del centro de datos.

Todos los visitantes que han aprobado el  acceso al centro de datos se designan como solo acompañantes en sus distintivos y deben permanecer siempre con sus escoltas. Los visitantes escoltados no tienen ningún nivel de acceso concedido a ellos y solo pueden viajar en el acceso de sus acompañantes. La escolta es responsable de revisar las acciones y el acceso de su visitante durante su visita al centro de datos.

El acceso de los visitantes es supervisado por la escolta asignada y por el supervisor de la sala de control a través del circuito cerrado de televisión (CCTV) y el sistema de supervisión de alarmas. Los visitantes con una solicitud de acceso aprobada tienen su solicitud de acceso revisada en el momento en que se comprueba su identificación con una forma de identificación emitida por el gobierno o una credencial emitida por Microsoft. A los visitantes aprobados para el acceso escoltado se les emite una etiqueta adhesiva autoexcediendo, y al devolver el registro de acceso dentro de la herramienta se termina. Si un visitante sale con su distintivo, el distintivo expira automáticamente en 24 horas.

Los distintivos de acceso temporal se almacenan en el SOC controlado por acceso y se inventarian al principio y al final de cada turno. Los agentes de seguridad tienen personal 24 x 7 y las claves físicas se almacenan en un sistema de administración de claves electrónicas que está vinculado al sistema de acceso físico que requiere el PIN y el distintivo de acceso de un oficial de seguridad para obtener acceso.

## <a name="access-review-and-deprovisioning"></a>Revisión y desavisionación de Access

El equipo de DCM es responsable de revisar periódicamente el acceso a los centros de datos y de realizar una auditoría trimestral para comprobar que el acceso individual sigue siendo necesario.

Para las terminaciones o transferencias, el acceso de la persona se quita inmediatamente del sistema y se quita su distintivo de acceso. Esto quita cualquier acceso al centro de datos que la persona haya tenido. Los equipos de DCM también realizan revisiones trimestrales de acceso para validar la adecuadaidad de la lista de acceso al centro de datos en el sistema.

## <a name="key-management"></a>Administración de claves

Las claves físicas y duras se desproteden a personal específico al hacer coincidir el distintivo de acceso de la persona con la clave física. Una persona debe tener el nivel de acceso adecuado en la herramienta para comprobar claves específicas. Las claves no están permitidas fuera del sitio.

Las claves y distintivos duros se mantienen bajo control estricto por Parte de Microsoft y se auditan diariamente. Microsoft también mitiga los riesgos implementando una asignación estricta de los niveles de acceso y una distribución y administración controladas de claves. Los métodos de acceso principales en los centros de datos son distintivos de acceso electrónico y biometría, lo que permite la revocación inmediata del acceso según sea necesario. Microsoft tiene procedimientos establecidos para determinar las acciones apropiadas que se correspondan con el riesgo de todas las claves perdidas. Estas acciones pueden requerir la reclave de un bastidor o puerta de un solo servidor y hasta la reclave de toda la instalación del centro de datos.

## <a name="access-logging-and-monitoring"></a>Registro y supervisión de acceso

Las solicitudes de acceso y los eventos de entrada y salida se registran y se conservan como parte de una traza de auditoría electrónica, lo que permite el acceso después de la interrogación y conciliación de los datos de hechos. Los informes del sistema de control de acceso y el análisis de datos permiten una mayor detección de anomalías para identificar y evitar el acceso innecesario y no autorizado.

Los sistemas de vigilancia de centros de datos supervisan áreas críticas del centro de datos, como la entrada y salida principal del centro de datos, la entrada y salida de las colocaciones del centro de datos, las celdas, los armarios bloqueados, las formas de los pasillos, las áreas de envío y recepción, los entornos críticos, las puertas perimetrales y las áreas de estacionamiento. Las grabaciones de vigilancia se conservan durante un mínimo de 90 días, a menos que la legislación local dicte lo contrario.

Un supervisor de sala de control siempre está en el SOC para proporcionar supervisión del acceso físico en el centro de datos. La videovigilancia se emplea para supervisar el acceso físico al centro de datos y al sistema de información. El sistema de video vigilancia está vinculado al sistema de supervisión de alarmas de creación para admitir la supervisión de acceso físico de los puntos de alarma. Los responsables de seguridad se aseguran de que solo se permita el acceso a aquellos empleados con autorización adecuada y comprueben que cualquier persona que traiga equipamiento dentro y fuera de las instalaciones de infraestructura críticas siga los procedimientos adecuados.

El equipo de seguridad documenta los eventos de seguridad que se producen en el centro de datos en un informe denominado Notificación de eventos de seguridad (SEN). Los informes SEN capturan los detalles de un evento de seguridad y deben documentarse después de que se produzca un evento para capturar los detalles con la mayor precisión posible. Los informes SEN también contienen el análisis de investigación realizado en un Informe de acción posterior (AAR), que documenta la investigación de un evento de seguridad, intenta identificar la causa raíz del evento y registra las acciones de corrección y las lecciones aprendidas. Las acciones de corrección y las lecciones aprendidas se usan para mejorar los procedimientos de seguridad y reducir el parecido de la repetición del evento. Si un incidente afecta a los activos o servicios de Microsoft, el equipo de Administración de incidentes de seguridad (SIM) tiene procedimientos detallados para responder.

Además de la seguridad 24x7 in situ, los centros de datos de Microsoft usan sistemas de supervisión de alarmas que proporcionan supervisión de vídeo y alarma en tiempo real. Las puertas del centro de datos tienen alarmas que informan sobre cada apertura y cuando permanecen abiertas más allá de un período de tiempo programado. El sistema de seguridad está programado para mostrar una imagen de vídeo en directo cuando se activa una alarma de puerta. Los lectores biométricos y de tarjeta de acceso se programan y supervisan a través del sistema de supervisión de alarmas. Las alarmas son supervisadas y respondidas a 24 x 7 por el supervisor de la sala de control que usa cámaras en el área del incidente que se está investigando para proporcionar información en tiempo real al respondedor.
