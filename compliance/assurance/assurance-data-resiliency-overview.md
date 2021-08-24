---
title: Resistencia de datos en Microsoft 365
description: En este artículo, obtenga información sobre el diseño y los principios de resistencia y recuperación de datos en Microsoft 365.
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
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 48fe50347e7e81c7e5f8552299c04a268b8b449c
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482113"
---
# <a name="data-resiliency-in-microsoft-365"></a>Resistencia de datos en Microsoft 365

Dada la naturaleza compleja de la informática en la nube, Microsoft tiene en cuenta que no se trata de si las cosas van a salir mal, sino de cuándo. Diseñamos nuestros servicios en la nube para maximizar la confiabilidad y minimizar los efectos negativos en los clientes cuando las cosas van mal. Hemos ido más allá de la estrategia tradicional de depender de una infraestructura física compleja y hemos integrado redundancia directamente en nuestros servicios en la nube. Usamos una combinación de infraestructura física menos compleja y software más inteligente que crea resistencia de datos en nuestros servicios y ofrece alta disponibilidad a nuestros clientes.

## <a name="resiliency-and-recoverability-are-built-in"></a>La resistencia y la capacidad de recuperación están integradas

La creación de resistencia y recuperación comienza con la suposición de que la infraestructura y los procesos subyacentes fallarán en algún momento: el hardware (infraestructura) fallará, los humanos cometen errores y el software tendrá errores. Aunque sería incorrecto decir que los desarrolladores de software no estaban pensando en estas cosas antes de la nube, la forma en que se trataron estos problemas en una implementación de TI típica era diferente antes de la nube:

- En primer lugar, las protecciones de hardware e infraestructura eran significativas. Esta estructura significaba que los centros de datos con una confiabilidad del 99,99 % requerían una redundancia significativa de red y energía, y los servidores se implementaron con clústeres basados en hardware, fuentes de alimentación duales, interfaces de red duales y similar.
- En segundo lugar, el proceso era fundamental. Los equipos de operaciones mantuvieron procedimientos rigurosos, se emplearon ventanas de cambio y, a menudo, hubo una sobrecarga importante en la administración de proyectos.
- En tercer lugar, la implementación se realizó a un ritmo glacial. Implementar código sin poseer el origen significaba esperar las versiones de revisión y las versiones principales implicaban reemplazo de hardware y un importante desembolso de capital. Además, la única forma de corregir un problema era revertir. Por lo tanto, la mayoría de las organizaciones de TI implementarían solo versiones principales para evitar que el trabajo se mantenga actualizado.
- Por último, la escala de los sistemas implementados y el nivel de su interconexión era históricamente mucho menor que ahora.

En la actualidad, los clientes esperan una innovación continua de Microsoft sin comprometer la calidad, y esta es una de las razones por las que los servicios y el software de Microsoft se construyen pensando en la resistencia y la capacidad de recuperación.

## <a name="microsoft-365-data-resiliency-principles"></a>Microsoft 365 principios de resistencia de datos

La resistencia hace referencia a la capacidad de un servicio basado en la nube para resistir determinados tipos de errores y, sin embargo, permanece totalmente funcional desde la perspectiva de los clientes. La resistencia de los datos significa que, independientemente de los errores que se produzcan en Microsoft 365, los datos críticos de los clientes permanecen intactos y no se ven afectados. Para ello, los Microsoft 365 se han diseñado en torno a cinco principios de resistencia específicos:

- Hay datos críticos y no críticos. Los datos no críticos (por ejemplo, si se leyó un mensaje) se pueden descartar en escenarios de error poco frecuentes. Los datos críticos (por ejemplo, datos de clientes como mensajes de correo electrónico) deben protegerse a un costo extremo. Como objetivo de diseño, los mensajes de correo entregados siempre son críticos y cosas como si se ha leído un mensaje no son críticos.
- Las copias de datos del cliente deben separarse en diferentes zonas de error o en el mayor número posible de dominios de error (por ejemplo, centros de datos, accesibles mediante credenciales únicas (proceso, servidor u operador)) para proporcionar aislamiento de errores. 
- Los datos críticos de los clientes deben supervisarse para que no se puedan realizar errores en cualquier parte de Atomicity, Consistency, Isolation, Durability (ACID).
- Los datos del cliente deben estar protegidos contra daños. Debe examinarse o supervisarse activamente, repararse y recuperarse.
- La mayoría de los resultados de pérdida de datos se deben a acciones del cliente, por lo que permite a los clientes recuperarse por su cuenta mediante una GUI que les permita restaurar elementos eliminados accidentalmente.

A través de la creación de nuestros servicios en la nube a estos principios, junto con pruebas y validación sólidas, Microsoft 365 puede cumplir y superar los requisitos de los clientes al tiempo que garantiza una plataforma para la innovación y la mejora continuas.

## <a name="related-articles"></a>Artículos relacionados

- [Trabajar con datos dañados](assurance-dealing-with-data-corruption.md)
- [Protección de malware y Ransomware](assurance-malware-and-ransomware-protection.md)
- [Supervisión y recuperación automática](assurance-monitoring-and-self-healing.md)
- [Exchange Resistencia de datos](assurance-exchange-data-resiliency.md)
