---
title: Protecciones del entorno del centro de datos
description: Obtenga más información sobre las protecciones del entorno del centro de datos de Microsoft.
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
ms.openlocfilehash: 525aab55d3f56490ecd1f1da1e00d6c5ddd32dc4
ms.sourcegitcommit: cf424cb1e7c12048120977f294f780b776119a96
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/11/2021
ms.locfileid: "60265138"
---
# <a name="datacenter-environmental-safeguards"></a>Protecciones del entorno del centro de datos

Microsoft emplea varias medidas de seguridad para proteger contra las amenazas ambientales a la disponibilidad del centro de datos. Estas protecciones permiten a Microsoft proporcionar plataformas en la nube seguras y disponibles de confianza para los clientes.

## <a name="site-selection"></a>Selección de sitio

La protección de los centros de datos de Microsoft frente a los riesgos ambientales comienza con la selección de sitios. Las ubicaciones de los centros de datos de Microsoft se someten a una evaluación estricta antes de la selección para la construcción del centro de datos. Los sitios de centros de datos de Microsoft se seleccionan estratégicamente para minimizar el riesgo de varios factores, como inundaciones, sismos, huracanes y otros desastres naturales. Además de minimizar el riesgo ambiental, el acceso a la infraestructura de telecomunicaciones confiable y de bajo costo es uno de los factores clave que influyen en la selección del sitio del centro de datos.

## <a name="climate-control"></a>Climatización

La climatización es un componente fundamental de la infraestructura esencial dentro de un centro de datos, y se utiliza para supervisar y mantener los espacios optimizados para el personal y el equipo o el hardware. La carga térmica (como producto derivado del consumo energético) y la humedad deben administrarse para garantizar condiciones operativas adecuadas mediante la intervención mecánica. Las condiciones climatológicas locales, los diversos requisitos normativos y las restricciones determinarán la manera más eficaz de tener una climatización adecuada.

Los niveles de temperatura y humedad se mantienen de acuerdo con los requisitos ambientales del hardware de IT que se espera en cada centro de datos. Los centros de datos de Microsoft mantienen un acuerdo de nivel operativo con sus clientes de modo que se cumple una eficiencia óptima al tiempo que se mantienen los requisitos mínimos del entorno. El sistema de administración de edificios (BMS) del centro de datos supervisa continuamente los niveles de temperatura y humedad. Los miembros del equipo de Entornos críticos (CE) supervisan el BMS desde el Centro de operaciones de instalaciones (FOC), para que puedan administrar la temperatura y la humedad dentro del centro de datos antes de que se superen los puntos de alarma. BMS está configurado para notificar al equipo ce cuando se alcanzan determinados marcadores, que luego investigan y hacen ajustes para corregir el problema del clima. Los intervalos aceptables para la temperatura y la humedad son coherentes con las directrices de la American Society of Heating, Refrigerating, and Air-conditioning Engineers (ASHRAE) o directrices similares aplicables localmente. La humedad del centro de datos se mide por porcentaje de humedad relativa, sin condensar con el intervalo actual entre el 40%-55%. El intervalo de temperatura suele estar entre 18 grados centígrados y 27 grados centígrados (entre 64,4 grados Fahrenheit y 80,6 grados Fahrenheit).

## <a name="fire-and-water-damage-protection"></a>Protección contra incendios y daños por inundación

Microsoft emplea sistemas de detección y supresión de incendios de última generación en cada instalación del centro de datos. Los sistemas de prevención de incendios son compatibles con una fuente de energía independiente para garantizar la protección de los empleados e infraestructura de Microsoft si hay un incendio. Las instalaciones de centros de datos también están protegidas de daños por inundaciones mediante sensores de agua colocados en áreas en las que se considera que existe un riesgo fuga. Estos sensores de agua notifican, de manera rápida, al personal adecuado si existe una emergencia relacionada con el agua. Las válvulas de cierre de agua están diseñadas para ser accesibles y los empleados están entrenados con respecto a su funcionamiento y ubicación.

Los centros de datos de Microsoft implementan mecanismos robustos de detección de incendios, incluidos los detectores de humo fotoeléctricos instalados debajo del piso y el techo, los sistemas Xtralis Very Early Smoke Detection Apparatus (VESDA) en cada colocación, los cuadros de alarma de incendio de la estación instalados en todos los centros de datos, los extintores de incendios ubicados en todos los centros de datos, las patrullas del personal de seguridad en todas las áreas de construcción varias veces cada turno de ocho horas,  y los sistemas de detección/supresión de incendios e iluminación de emergencia se cablean en los sistemas de energía de copia de seguridad del centro de datos que proporcionan una fuente de alimentación redundante. Las áreas que contienen equipos eléctricos confidenciales están protegidas por sistemas de aspersores de doble interbloqueo previo a la acción (tubo seco).

El equipo de CE realiza un recorrido diario por el sitio (DSWT) para comprobar cada sala y muchas partes de componentes dentro de ellos para garantizar que se cumplen todos los requisitos de protección contra incendios.

Microsoft emplea dispositivos o sistemas de detección de incendios para el sistema de información que se activan automáticamente y notifican al personal del centro de datos junto con los respondedores de emergencia si se produce un incendio. Si uno de los mecanismos de detección de incendios se activa en cualquier espacio de colocación, se notificará automáticamente al departamento de bomberos local y al Centro de operaciones de seguridad global de Redmond, Washington. Los sistemas de protección contra incendios y detección están vinculados al sistema de seguridad que notifica a la instalación local y al personal de seguridad.

Microsoft proporciona detección de agua/fugas en áreas con riesgo de fuga de agua. Los sistemas de supresión de incendios también tienen alarmas de detección de fugas que se supervisan. El sistema de detección de agua/fugas se integra con el sistema de notificación y alarma de la instalación, y los sistemas de aspersores dentro de los centros de datos están ubicados en zonas. Los equipos de administración de centros de datos y CE están familiarizados con los procedimientos de emergencia que requieren el uso de las válvulas de cierre de agua y sus ubicaciones. Los elevadores de aspersores se pueden apagar individualmente o como grupo a través de las válvulas de la puerta. Todos los aspersores del espacio crítico son aspersores de tipo de acción previa al enclavamiento doble que requieren dos formas de activación antes de iniciar el flujo. La presión del sistema del aspersor se supervisa y se alarma contra la fuga de agua.

## <a name="health-and-safety"></a>Salud y seguridad

El compromiso con la salud y la seguridad de los empleados de Microsoft es fundamental para medir el éxito. Los centros de datos de Microsoft funcionan de acuerdo con las normativas locales, regionales, nacionales y federales de seguridad y salud. En la mayoría de los casos, las directivas de seguridad y salud de Microsoft superan los requisitos gubernamentales y reglamentarios para garantizar la protección de la salud, la seguridad y el bienestar de todos los trabajadores del centro de datos durante todas las fases del ciclo de vida del centro de datos, desde la construcción hasta el desmantelamiento. Los planes de administración de seguridad, la evaluación de riesgos, la administración de actividades de alto riesgo y la formación en seguridad son principios centrales para proporcionar un entorno de trabajo seguro para todos los empleados.

## <a name="energy-efficiency"></a>Energía eficiente

Microsoft opera con neutralidad de carbono desde 2012. Para 2030, Microsoft será negativo en carbono y, para 2050, Microsoft habrá quitado del entorno todo el carbono que la compañía ha emitido directamente o por consumo eléctrico desde que se fundó en 1975. Para 2025, los centros de datos de Microsoft se suministrarán con energía 100% renovable. Para lograr este objetivo, Microsoft ha implementado herramientas de contratación como contratos de compra de energía de generación de proxy para energía verde con el fin de suministrar el 100% de la electricidad que emite carbono que consumen todos los centros de datos.
