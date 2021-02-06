---
title: Publicación 140-2 del Estándar Federal de Procesamiento de Información (FIPS)
description: Microsoft certifica que sus módulos criptográficos cumplen con el estándar federal de procesamiento de información de estados unidos.
keywords: Microsoft 365, cumplimiento, ofertas
localization_priority: None
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: d7d1f47d7f76f9fc6d3cefa6cac5be807af98cbc
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120839"
---
# <a name="federal-information-processing-standard-fips-publication-140-2"></a>Publicación 140-2 del Estándar Federal de Procesamiento de Información (FIPS)

## <a name="fips-140-2-standard-overview"></a>Introducción al estándar FIPS 140-2

La Publicación 140-2 del Estándar Federal de Procesamiento de Información (FIPS) es un estándar gubernamental de Estados Unidos que define los requisitos de seguridad mínimos para módulos criptográficos en productos de tecnología de la información, tal como se define en la sección 5131 de la Ley de reforma de la administración de tecnologías de la información de 1996.

El Programa de validación de módulos criptográficos (CMVP), un esfuerzo conjunto del Instituto Nacional de Estándares y Tecnología (NIST) de Estados Unidos y el Centro Canadiense de Seguridad Cibernética (CCCS), valida los módulos criptográficos según los requisitos de seguridad del estándar de módulos criptográficos (es decir, FIPS 140-2) y los estándares de criptografía FIPS relacionados. [](https://csrc.nist.gov/Projects/cryptographic-module-validation-program)  Los requisitos de seguridad fips 140-2 abarcan 11 áreas relacionadas con el diseño y la implementación de un módulo criptográfico. El Laboratorio de tecnología de la información de NIST opera un programa relacionado que valida los algoritmos criptográficos aprobados por FIPS en el módulo.

## <a name="microsofts-approach-to-fips-140-2-validation"></a>Enfoque de Microsoft para la validación fips 140-2

Microsoft mantiene un compromiso activo con el cumplimiento de los requisitos 140-2, después de validar módulos criptográficos desde la creación del estándar en 2001. Microsoft valida sus módulos criptográficos en el Programa de validación de módulos criptográficos (CMVP) del Instituto Nacional de Estándares y [Tecnología](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) (NIST). Varios productos de Microsoft, incluidos muchos servicios en la nube, usan estos módulos criptográficos.

Para obtener información técnica sobre los módulos criptográficos de Microsoft Windows, la directiva de seguridad de cada módulo y el catálogo de detalles del certificado CMVP, consulta el contenido de [Windows y Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

## <a name="microsoft-in-scope-cloud-services"></a>Servicios de la nube dentro del alcance de Microsoft

Aunque la guía de implementación actual de CMVP FIPS 140-2 excluye una validación FIPS 140-2 para un servicio en la nube en sí; los proveedores de servicios en la nube pueden elegir obtener y operar módulos criptográficos validados por FIPS 140 para los elementos informáticos que componen su servicio en la nube. Los servicios en línea de Microsoft que incluyen componentes, que han sido validados por FIPS 140-2 incluyen, entre otros:

- [Azure y Azure Government](/azure/azure-government/documentation-government-plan-security)
- [Dynamics 365 y Dynamics 365 Government](/microsoft-365/compliance/office-365-encryption-in-microsoft-dynamics-365)
- [Office 365, Office 365 Administración Pública para Estados Unidos y Office 365 U.S. Government Defense](/microsoft-365/compliance/office-365-encryption-risks-and-protections)

## <a name="frequently-asked-questions"></a>Preguntas más frecuentes

**¿Cuál es la diferencia entre "FIPS 140 Validated" y "FIPS 140 compliant"?**

"FIPS 140 Validated" significa que el CMVP validó el módulo criptográfico o un producto que inserta el módulo ("certificado") para cumplir los requisitos de FIPS 140-2. "Compatible con FIPS 140" es un término del sector para los productos de TI que dependen de los productos validados fips 140 para la funcionalidad criptográfica.

**¿Cuándo realiza Microsoft una validación FIPS 140?**

La cadencia para iniciar la validación de un módulo se alinea con las actualizaciones de características de Windows 10 y Windows Server. A medida que la industria del software ha evolucionado, los sistemas operativos se lanzan con más frecuencia, con actualizaciones de software mensuales. Microsoft lleva a cabo la validación de las versiones de características, pero entre versiones, intenta minimizar los cambios en los módulos criptográficos.

**¿Qué equipos se incluyen en una validación FIPS 140?**

Microsoft valida los módulos criptográficos en una muestra representativa de configuraciones de hardware que ejecutan Windows 10 y Windows Server. Es una práctica habitual del sector aceptar esta validación FIPS 140-2 cuando un entorno usa hardware, que es similar a los ejemplos usados para el proceso de validación.

**Hay muchos módulos enumerados en el sitio web de NIST. ¿Cómo sé cuál se aplica a mi agencia?**

Si necesita usar módulos criptográficos validados a través de FIPS 140-2, debe comprobar que la versión que usa aparece en la lista de validación. Cmvp y Microsoft mantienen una lista de módulos criptográficos validados, organizados por versión del producto, junto con instrucciones para identificar qué módulos están instalados en un sistema Windows. Para obtener más información sobre cómo configurar sistemas para que sean compatibles, consulta el contenido de [Windows y Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

**¿Qué significa "Cuando se opera en modo FIPS" en un certificado?**

Esta advertencia informa al lector de que se deben seguir las reglas de configuración y seguridad necesarias para usar el módulo criptográfico de forma coherente con su directiva de seguridad FIPS 140-2. Cada módulo tiene su propia directiva de seguridad , una especificación precisa de las reglas de seguridad con las que operará, y emplea algoritmos criptográficos aprobados, administración de claves criptográficas y técnicas de autenticación. Las reglas de seguridad se definen en la directiva de seguridad de cada módulo. Para obtener más información, incluidos los vínculos a la directiva de seguridad de cada módulo validado a través del CMVP, consulta el contenido de [Windows y Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

**¿FedRAMP requiere la validación FIPS 140-2?**

Sí, el Programa federal de administración de riesgos y autorización (FedRAMP) se basa en las líneas base de control definidas por la revisión 4 de [NIST SP 800-53,](https://nvd.nist.gov/800-53/Rev4/)incluida la protección criptográfica [SC-13](https://nvd.nist.gov/800-53/Rev4/control/SC-13) que exige el uso de criptografía validada por FIPS o criptografía aprobada por la NSA.

**¿Cómo admite Microsoft Azure FIPS 140-2?**

Azure se ha creado con una combinación de hardware, sistemas operativos disponibles comercialmente (Linux y Windows) y una versión específica de Azure de Windows. A través [](https://www.microsoft.com/securityengineering/sdl/) del Ciclo de vida de desarrollo de seguridad (SDL) de Microsoft, todos los servicios de Azure usan algoritmos aprobados por FIPS 140-2 para la seguridad de datos, ya que el sistema operativo usa algoritmos aprobados por FIPS 140-2 mientras se opera en una nube de hiperespacio.

**¿Puedo usar la adherencia de Microsoft a FIPS 140-2 en el proceso de certificación de mi agencia?**

Para cumplir con FIPS 140-2, el sistema debe configurarse para ejecutarse en un modo de operación aprobado por FIPS, que incluye garantizar que un módulo criptográfico use solo algoritmos aprobados por FIPS. Para obtener más información sobre cómo configurar sistemas para que sean compatibles, consulta el contenido de [Windows y Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

**¿Cuál es la relación entre FIPS 140-2 y criterios comunes?**

Se trata de dos estándares de seguridad independientes con fines diferentes, pero complementarios. FIPS 140-2 está diseñado específicamente para validar módulos criptográficos de software y hardware, mientras que los criterios comunes están diseñados para evaluar las funciones de seguridad de los productos de software y hardware de TI. Las evaluaciones de criterios comunes a menudo se basan en validaciones FIPS 140-2 para garantizar que la funcionalidad criptográfica básica se implementa correctamente.

## <a name="resources"></a>Recursos

- [Requisitos de seguridad de FIPS Pub 140-2 para módulos criptográficos](https://csrc.nist.gov/publications/fips/fips140-2/fips1402.pdf)
- [Programa de validación de módulo criptográfico NIST](https://csrc.nist.gov/groups/STM/cmvp/index.html)
- [Windows, Windows Server y FIPS 140-2](/windows/security/threat-protection/fips-140-validation)
- [Cumplimiento en el Centro de Confianza de Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
