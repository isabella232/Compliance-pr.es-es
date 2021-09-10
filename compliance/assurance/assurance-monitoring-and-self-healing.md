---
title: Supervisión de datos y recuperación automática en Microsoft 365
description: En este artículo, aprenderá sobre las capacidades de supervisión y recuperación automática de Microsoft 365.
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
ms.custom:
- seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: d4188448038a3b47c2cf7a0a8193f1772740eb7f
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947259"
---
# <a name="data-monitoring-and-self-healing-in-microsoft-365"></a>Supervisión de datos y recuperación automática en Microsoft 365

Dada la escala de Microsoft 365, sería imposible mantener los datos de los clientes resistentes y seguros contra el malware sin una supervisión integrada que sea completa, que alerte de que es inteligente y de recuperación automática que es rápida y confiable. Supervisar un conjunto de servicios a la escala de Microsoft 365 es muy difícil. Es necesario introducir nuevas mentalidades y metodologías y crear nuevos conjuntos de tecnología para operar y administrar el servicio en un entorno global conectado. Nos hemos alejado del enfoque de supervisión tradicional de la recopilación y filtrado de datos para crear alertas a un enfoque basado en el análisis de datos; tomar señales y generar confianza en los datos y, a continuación, usar la automatización para recuperar o resolver el problema. Este enfoque ayuda a sacar a los humanos de la ecuación de recuperación, lo que a su vez hace que las operaciones sea menos costosas, más rápidas y menos propensas a errores. 

Fundamental para Microsoft 365 supervisión es una colección de tecnologías que componen nuestro motor de Ideas de datos, que se basa en azure, SQL Azure y tecnología de base de datos de streaming de código [abierto.](https://cassandra.apache.org/) Está diseñado para recopilar y agregar datos y llegar a conclusiones. Actualmente, procesa más de 500 millones de eventos por hora desde más de 100 000 servidores (aproximadamente 15 TB al día) dispersos en decenas de centros de datos en muchas regiones, y estas cifras están creciendo. 

Microsoft 365 la *supervisión externa,* que implica la creación de transacciones sintéticas para probar todo lo que es importante. Por ejemplo, en Exchange Online cada escenario está probando cada base de datos en todo el mundo cada cinco minutos de forma dispersa, lo que proporciona una cobertura casi continua de todo lo que vive en el sistema. Desde varias ubicaciones, se realizan 250 millones de transacciones de prueba al día para crear una línea base o latido sólido para el servicio. 

Microsoft 365 también usa el concepto de *alerta* roja , que reduce todas las señales de supervisión de todas las máquinas de nuestros centros de datos a algo manejable por un ser humano. El concepto es bastante simple: si algo está sucediendo en varias señales, debe haber algo en marcha. No se trata de generar confianza en una señal, se trata de tener una fidelidad razonable para cada señal para que obtenga una mayor precisión. Este sistema de supervisión es tan eficaz que no tenemos personal 24 x 7 observando nuestros monitores; lo único que tenemos es la máquina que se reactiva si detecta un problema, en cuyo caso se va a paginar el personal de llamada adecuado, o más a menudo, como es el caso, simplemente irá adelante y resolverá el problema. Una vez que empezamos a recopilar señales y crear alertas rojas, podemos empezar a triangular en todas nuestras particiones de servicio. 

En función de la combinación de la alerta de error y las alertas rojas, esta alerta indica exactamente qué componentes podrían tener un problema y que el sistema va a intentar corregir el problema por sí mismo reiniciando un servidor de buzones de correo. 

Además de las funciones de recuperación automática, como la restauración de una sola página, Exchange Online incluye varias características que toman un enfoque de supervisión y recuperación automática que se centra en conservar la experiencia del usuario final. Estas características incluyen *Disponibilidad* administrada, que proporciona acciones integradas de supervisión y recuperación, y AutoReseed, que restaura automáticamente la redundancia de la base de datos después de un error de disco. 

## <a name="managed-availability"></a>Disponibilidad administrada 

La disponibilidad administrada proporciona una solución nativa de recuperación y comprobación de estado que supervisa y protege la experiencia del usuario final mediante acciones orientadas a la recuperación. La disponibilidad administrada es la integración de acciones integradas de supervisión y recuperación con la Exchange de alta disponibilidad. Está diseñada para detectar y solucionar problemas a medida que surgen y que el sistema los detecta. A diferencia de las técnicas y soluciones de supervisión externas para Exchange, la disponibilidad administrada no intenta identificar ni comunicar la causa principal de un problema. En su lugar, se centra en aspectos de recuperación que abordan tres áreas clave de la experiencia del usuario final:

- **Disponibilidad:** ¿los usuarios pueden acceder al servicio? 
- **Latencia:** ¿cómo es la experiencia para los usuarios? 
- **Errores:** ¿los usuarios pueden lograr lo que desean? 

La disponibilidad administrada es una característica interna que se ejecuta en todos los Microsoft 365 que se ejecutan Exchange Online. Sondea y analiza cientos de métricas de mantenimiento cada segundo. Si se encuentra que algo está mal, la mayoría de las veces se soluciona automáticamente. Pero siempre habrá problemas que la disponibilidad administrada no podrá solucionar por sí sola. En esos casos, la disponibilidad administrada escalará el problema a un Microsoft 365 de soporte técnico mediante el registro de eventos.

## <a name="autoreseed"></a>AutoReseed

Exchange Online servidores se implementan en una configuración que almacena varias bases de datos y sus secuencias de registro en el mismo disco que no es RAID. Esta configuración a menudo  se conoce como un montón de discos (JBOD) porque no se usan mecanismos de redundancia de almacenamiento, como RAID, para duplicar los datos del disco. Cuando se produce un error en un disco en un entorno JBOD, se pierden los datos de ese disco. 

Dado el tamaño de Exchange Online y el hecho de que se han implementado en él millones de unidades de disco, los errores de unidad de disco son una ocurrencia regular en Exchange Online. De hecho, más de 100 fallan cada día. Cuando se produce un error en un disco en una implementación de empresa local, un administrador debe reemplazar manualmente el disco con errores y restaurar los datos afectados. En una implementación en la nube, el tamaño de Microsoft 365, tener operadores (administradores de la nube) reemplazando manualmente discos no es práctico ni económicamente viable. 

El reseed automático o *AutoReseed* es una característica que sustituye a lo que normalmente es una acción controlada por el operador en respuesta a un error de disco, un evento de daños en la base de datos u otro problema que requiere una reseedación de una copia de base de datos. AutoReseed se ha diseñado con el fin de restaurar automáticamente la redundancia de bases de datos después de un error en el disco mediante el uso de discos de reserva que se aprovisionan al sistema. Si se produce un error en un disco, las copias de base de datos almacenadas en ese disco se reseban automáticamente en un disco de reserva preconfigurado en el servidor, lo que restaura la redundancia. 