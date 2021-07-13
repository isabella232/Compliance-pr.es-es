---
title: Publicación 140-2 del Estándar federal de procesamiento de información (FIPS)
description: Microsoft certifica que sus módulos criptográficos cumplen con el Estándar federal de procesamiento de información de Estados Unidos.
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
ms.openlocfilehash: 2c51979122aaedda90bac74740e95c9d1265de74
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385010"
---
# <a name="federal-information-processing-standard-fips-publication-140-2"></a>Publicación 140-2 del Estándar federal de procesamiento de información (FIPS)

## <a name="fips-140-2-standard-overview"></a>Introducción estándar a FIPS 140-2

La Publicación 140-2 del Estándar federal de procesamiento de información (FIPS) es un estándar gubernamental de Estados Unidos que define los requisitos mínimos de seguridad para módulos criptográficos en productos de tecnología de la información, tal como se define en la sección 5131 de la Ley de reforma de la administración de tecnologías de la información de 1996.

El Programa de validación de módulos criptográficos (CMVP), un esfuerzo conjunto del Instituto Nacional de Estándares y Tecnología de  Estados Unidos (NIST) y el Centro Canadiense de Seguridad Cibernética (CCCS), valida los módulos criptográficos con el estándar de requisitos de seguridad para módulos criptográficos (es decir, FIPS 140-2) y los estándares de criptografía FIPS relacionados. [](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) Los requisitos de seguridad de FIPS 140-2 abarcan 11 áreas relacionadas con el diseño y la implementación de un módulo criptográfico. El Laboratorio de tecnología de la información de NIST opera un programa relacionado que valida los algoritmos criptográficos aprobados por FIPS en el módulo.

## <a name="microsofts-approach-to-fips-140-2-validation"></a>Enfoque de Microsoft para la validación de FIPS 140-2

Microsoft mantiene un compromiso activo de cumplir los 140-2 requisitos, después de validar módulos criptográficos desde el inicio del estándar en 2001. Microsoft valida sus módulos criptográficos en el Programa de validación de módulos criptográficos (CMVP) del Instituto Nacional de Estándares y [Tecnología](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) (NIST). Varios productos de Microsoft, incluidos muchos servicios en la nube, usan estos módulos criptográficos.

Para obtener información técnica sobre los módulos criptográficos de Microsoft Windows, la directiva de seguridad de cada módulo y el catálogo de detalles del certificado CMVP, vea el contenido de Windows y [Windows Server FIPS 140-2](https://aka.ms/AA6ehud).

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plataformas en la nube de ámbito de Microsoft & servicios

Aunque la guía de implementación actual de CMVP FIPS 140-2 impide una validación fips 140-2 para un servicio en la nube en sí; Los proveedores de servicios en la nube pueden elegir obtener y operar módulos criptográficos validados por FIPS 140 para los elementos informáticos que componen su servicio en la nube. Los servicios en línea de Microsoft que incluyen componentes, que han sido validados por FIPS 140-2, incluyen, entre otros:

- Azure y Azure Government
- Dynamics 365 y Dynamics 365 Government
- Office 365, Office 365 Administración Pública para Estados Unidos y Office 365 U.S. Government Defense

## <a name="azure-dynamics-365-and-fips-140-2"></a>Azure, Dynamics 365 y FIPS 140-2

Para obtener más información acerca del cumplimiento de Azure, Dynamics 365 y otros servicios en línea, vea la oferta de [Azure FIPS 140-2](/azure/compliance/offerings/offering-fips-140-2).

## <a name="office-365-and-fips-140-2"></a>Office 365 y FIPS 140-2

### <a name="office-365-cloud-environments"></a>Office 365 entornos de nube

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 aplicabilidad y servicios en el ámbito

Use la tabla siguiente para determinar la aplicabilidad de los servicios Office 365 y suscripción:

| **Aplicabilidad** | **Servicios en el ámbito** |
|:------------------|:----------------------|
| Office 365, GCC, GCC High, DoD | Consulta [Validación de FIPS 140-2](/windows/security/threat-protection/fips-140-validation) |

### <a name="frequently-asked-questions"></a>Preguntas más frecuentes

**¿Cuál es la diferencia entre "FIPS 140 Validated" y "FIPS 140 compliant"?**

"FIPS 140 Validated" significa que el CMVP ha validado el módulo criptográfico o un producto que inserta el módulo ('certificado') como que cumple los requisitos fips 140-2. "Compatible con FIPS 140" es un término del sector para productos de TI que dependen de los productos validados fips 140 para la funcionalidad criptográfica.

**¿Cuándo realiza Microsoft una validación fips 140?**

La cadencia para iniciar una validación de módulo se alinea con las actualizaciones de características de Windows 10 y Windows Server. A medida que el sector de software evolucionó, los sistemas operativos se lanzan con más frecuencia, con actualizaciones de software mensuales. Microsoft realiza la validación de las versiones de características, pero entre versiones, busca minimizar los cambios en los módulos criptográficos.

**¿Qué equipos se incluyen en una validación fips 140?**

Microsoft valida módulos criptográficos en una muestra representativa de configuraciones de hardware que ejecutan Windows 10 y Windows Server. Es una práctica habitual del sector aceptar esta validación fips 140-2 cuando un entorno usa hardware, que es similar a los ejemplos usados para el proceso de validación.

**Hay muchos módulos enumerados en el sitio web de NIST. ¿Cómo sé cuál se aplica a mi agencia?**

Si necesita usar módulos criptográficos validados a través de FIPS 140-2, debe comprobar que la versión que use aparezca en la lista de validación. El CMVP y Microsoft mantienen una lista de módulos criptográficos validados, organizados por la versión del producto, junto con instrucciones para identificar qué módulos están instalados en un Windows web. Para obtener más información sobre cómo configurar los sistemas para que sean compatibles, vea el Windows y [Windows contenido fips 140-2 del servidor](https://aka.ms/AA6ehud).

**¿Qué significa "Cuando se opera en modo FIPS" en un certificado?**

Esta advertencia informa al lector de que se deben seguir las reglas de configuración y seguridad necesarias para usar el módulo criptográfico de forma coherente con su directiva de seguridad FIPS 140-2. Cada módulo tiene su propia directiva de seguridad, una especificación precisa de las reglas de seguridad bajo las que funcionará, y emplea algoritmos criptográficos aprobados, administración de claves criptográficas y técnicas de autenticación. Las reglas de seguridad se definen en la directiva de seguridad de cada módulo. Para obtener más información, incluidos los vínculos a la directiva de seguridad de cada módulo validado a través del CMVP, vea el contenido Windows y [Windows Server FIPS 140-2](https://aka.ms/AA6ehud).

**¿FedRAMP requiere la validación fips 140-2?**

Sí, el Programa federal de administración de riesgos y autorización (FedRAMP) se basa en las líneas base de control definidas por la revisión 4 de [NIST SP 800-53,](https://nvd.nist.gov/800-53/Rev4/)incluida la protección criptográfica [SC-13](https://nvd.nist.gov/800-53/Rev4/control/SC-13) que exige el uso de criptografía validada por FIPS o criptografía aprobada por la NSA.

**¿Puedo usar la adherencia de Microsoft a FIPS 140-2 en el proceso de certificación de mi agencia?**

Para cumplir con FIPS 140-2, el sistema debe configurarse para que se ejecute en un modo de operación aprobado por FIPS, lo que incluye garantizar que un módulo criptográfico use solo algoritmos aprobados por FIPS. Para obtener más información sobre cómo configurar los sistemas para que sean compatibles, vea el Windows y [Windows contenido fips 140-2 del servidor](https://aka.ms/AA6ehud).

**¿Cuál es la relación entre FIPS 140-2 y Criterios comunes?**

Se trata de dos estándares de seguridad independientes con fines diferentes, pero complementarios. FIPS 140-2 está diseñado específicamente para validar módulos criptográficos de software y hardware, mientras que common criteria está diseñado para evaluar las funciones de seguridad en productos de hardware y software de TI. Las evaluaciones de criterios comunes suelen basarse en validaciones fips 140-2 para garantizar que la funcionalidad criptográfica básica se implementa correctamente.

### <a name="resources"></a>Recursos

- [Requisitos de seguridad de FIPS Pub 140-2 para módulos criptográficos](https://csrc.nist.gov/publications/fips/fips140-2/fips1402.pdf)
- [Programa de validación de módulo criptográfico NIST](https://csrc.nist.gov/groups/STM/cmvp/index.html)
- [Windows, Windows Server y FIPS 140-2](/windows/security/threat-protection/fips-140-validation)
- [Cumplimiento en el Centro de Confianza de Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
