---
title: Destrucción de dispositivos portadores de datos
description: En este artículo, encontrará una introducción al proceso de destrucción de dispositivos portadores de datos para centros de datos de Microsoft.
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
ms.openlocfilehash: 6a26334b805be069298302d3ad1e8e5b9e728150
ms.sourcegitcommit: 1fd50ef5f165228109a3f2f0aef4b0c2aa59b2ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2021
ms.locfileid: "58862408"
---
# <a name="data-bearing-device-destruction"></a>Destrucción de dispositivos portadores de datos

## <a name="data-destruction-overview"></a>Introducción a la destrucción de datos

Microsoft tiene directrices, directivas, requisitos de seguridad y procedimientos para el tratamiento y la administración de dbds en centros de datos de Microsoft.

Un DBD es cualquier dispositivo de almacenamiento capaz de almacenar datos de Microsoft propietarios o de clientes:

- Unidades de disco duro (HDD)
- Unidades de estado sólido (SSD)
- Unidades USB
- Tarjetas aceleradoras de E/S
- Tarjetas Flash SD/Compact
- Tarjetas de HSM
- Tarjetas SSD PCIe
- NVDIMM (módulo de memoria en línea dual no volátil)

Los DBD con errores usados en centros de datos de Microsoft se auditan y destruyen en el campus del centro de datos. Cualquier activo retirado del servicio se evalúa para su eliminación de manera acorde con sus requisitos de seguridad/privacidad y clasificación de activos, y de acuerdo con las reglas, leyes y reglamentos aplicables.

Microsoft usa tres categorías de desinfección de datos para dbds y activos que contienen datos:

- **Clear:** se relaciona con las técnicas lógicas que ayudan a sanitizar los datos en todas las ubicaciones de almacenamiento direccionables por el usuario para protegerse contra técnicas sencillas de recuperación de datos no invasivas. Estas son técnicas que se suelen aplicar a través de los comandos estándar de lectura y escritura en el dispositivo de almacenamiento, como reescribir con un nuevo valor o usar una opción de menú para restablecer el dispositivo al estado de fábrica (donde no se admite la reescritura).
- **Purgar:** se relaciona con técnicas físicas o lógicas que hacen inviable la recuperación de datos de destino mediante técnicas de laboratorio de última generación.
- **Destruir:** hace que la recuperación de datos de destino sea inviable mediante técnicas de laboratorio de última generación y da como resultado la incapacidad posterior de usar los medios para el almacenamiento de datos.

La purga y eliminación de la desinfección se realiza con herramientas y procesos aprobados por el grupo de seguridad. Los registros se mantienen de la eliminación y destrucción de activos. Los dispositivos que no completan la depuración se desvian correctamente (solo para medios magnéticos), se perforan con varias patillas (para paneles basados en astillas, como los SSD) o se destruyen.

## <a name="clear"></a>Clear

Si se evalúa un activo retirado y se considera que no es accesible, se borra mediante una solución de eliminación de datos aprobada. Los centros de datos de Microsoft usan las directrices claras de NIST SP-800-88.

## <a name="purge"></a>Purge

Según la configuración del sitio y la disponibilidad del dispositivo, algunos dispositivos se purgan antes de la destrucción. Los dispositivos de purga incluyen desgosadores aprobados por la NSA para medios magnéticos y dispositivos de punzones de varios patillas para medios de estado sólido. Los centros de datos de Microsoft usan las directrices de purga de NIST SP-800-88.

## <a name="destroy"></a>Destruir

Si un activo retirado se evalúa y se considera accesible, se destruye in situ mediante un procedimiento operativo estándar aprobado que cumple las directrices de NIST SP-800-88. Estos DBD se rastrean física y lógicamente para mantener la cadena de custodia hasta la disposición final.

Cada centro de datos de Microsoft usa un proceso en el sitio para sanitizar y eliminar los DBD con errores y retirados. Durante este proceso, el personal de Microsoft garantiza que la cadena de custodia se mantenga durante todo el proceso de eliminación.

## <a name="resources"></a>Recursos

- [Nist Special Publication 800-88](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf)
