---
title: Clasificación de datos & taxonomía de etiqueta de confidencialidad
description: En este artículo, encontrará información general sobre cómo usar la clasificación de datos & taxonomía de etiqueta de confidencialidad con Microsoft 365.
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
ms.openlocfilehash: a68332971da909d8739039be6f0c8d84310ff9f9
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947242"
---
# <a name="data-classification--sensitivity-label-taxonomy"></a>Clasificación de datos & taxonomía de etiqueta de confidencialidad

Los datos confidenciales presentan un riesgo importante para una empresa si se roban, se comparten accidentalmente o se exponen a través de una infracción. Los factores de riesgo incluyen daños reputacionales, impacto financiero y pérdida de ventaja competitiva. Proteger los datos y la información que administra su empresa es una prioridad para su organización, pero puede resultar difícil saber si sus esfuerzos son realmente efectivos, dada la cantidad de contenido que tiene la empresa.

Además del volumen, el contenido puede variar en importancia de alta sensibilidad e impacto a trivial y transitorio. También puede estar bajo el control de varios requisitos de cumplimiento normativo. Saber qué priorizar y dónde aplicar controles puede ser un desafío. Siga leyendo para obtener información sobre la clasificación de *datos,* una herramienta importante para proteger el contenido contra robos, sabotajes o destrucción involuntaria, y cómo Microsoft 365 puede ayudarle a cumplir sus objetivos de seguridad de la información.

## <a name="what-is-data-classification"></a>¿Qué es la clasificación de datos?

[La clasificación de](/microsoft-365/compliance/data-classification-overview) datos es un término especializado que se usa en los campos de ciberseguridad y gobierno de la información para describir el proceso de identificación, categorización y protección del contenido según su nivel de confidencialidad o impacto. En su forma más básica, la clasificación de datos es un medio para proteger los datos de la divulgación, alteración o destrucción no autorizadas en función de su sensibilidad o impacto.

## <a name="what-is-a-data-classification-framework"></a>¿Qué es un marco de clasificación de datos?

A menudo codificada en una directiva formal de toda la empresa, un marco de clasificación de datos (a veces denominado "directiva de clasificación de datos") suele estar compuesto de 3 a 5 niveles de clasificación. Normalmente incluyen tres elementos: un nombre, una descripción y ejemplos reales. Microsoft recomienda no más de cinco etiquetas principales de nivel superior, cada una con cinco subetiquetas (25 en total) para que la interfaz de usuario (UI) sea manejable. Normalmente, los niveles se organizan de menos a más confidenciales, como *Public*, *Internal*, *Confidential* y *Highly* 
 *Confidential*. Otras variaciones de nombre de nivel que puede encontrar *incluyen Restricted*, *Unrestricted* y *Consumer Protected*. Microsoft recomienda nombres de etiquetas que son autodescriptivas y que resaltan claramente su confidencialidad relativa. Por ejemplo, *Confidencial* *y* Restringido puede dejar a los usuarios  adivinar qué etiqueta es adecuada, mientras que *Confidencial* y Extremadamente confidencial son más claros en los que es más confidencial. 

En la tabla siguiente se muestra un ejemplo de un nivel de marco *de* clasificación de datos extremadamente confidencial:

|**Nivel de clasificación**|**Descripción**|**Ejemplos**|
|:-----------------------|:--------------|:-----------|
| Extremadamente confidencial | Los datos extremadamente confidenciales son el tipo de datos más confidenciales almacenados o administrados por la empresa y pueden requerir notificaciones legales si se infringen o se divulgan de otro modo. <br><br> Los datos restringidos requieren el más alto nivel de control y seguridad, y el acceso debe limitarse a "necesidad de saber". | Información de identificación personal confidencial (PII confidencial) <br> Datos del titular de la tarjeta <br> Información de estado protegida (PHI) <br> Datos de cuentas bancarias |

>[!TIP]
>El marco de clasificación de datos corporativos de Microsoft usó originalmente una categoría y una etiqueta denominada "Internal" durante la fase piloto, pero encontró que había motivos legítimos para que un documento se compartiese externamente y se cambiara al uso de "General".

Otro componente importante de un marco de clasificación de datos son los controles asociados a cada nivel. Los niveles de clasificación de datos por sí solos son simplemente etiquetas (o etiquetas) que indican el valor o la confidencialidad del contenido. Para *proteger* ese contenido, los marcos de clasificación de datos definen los controles que deben estar en su lugar para cada uno de los niveles de clasificación de datos. Estos controles pueden incluir requisitos relacionados con:

- Storage y ubicación
- Cifrado
- Control de acceso
- Destrucción de datos
- Prevención de pérdida de datos
- Divulgación pública
- Registro y seguimiento del acceso
- Otros objetivos de control, según sea necesario

Los controles de seguridad variarán según el nivel de clasificación de datos, de forma que las medidas de protección definidas en el marco aumenten en función de la confidencialidad del contenido. Por ejemplo, los requisitos de control de almacenamiento de datos variarán en función de los medios que se usan, así como del nivel de clasificación aplicado a un determinado elemento de contenido. En la tabla siguiente se muestra un ejemplo de controles de clasificación de datos para un tipo de almacenamiento específico:

|**Tipo de almacenamiento**|**Confidencial**|**Interna**|**Sin restricciones**|
|:---------------|:---------------|:-----------|:---------------|
| Storage | Prohibido | Prohibido a menos que esté cifrado | No se requiere ningún control |

Aplicar correctamente el nivel correcto de clasificación de datos puede ser complejo en situaciones reales y a veces puede saturar a los usuarios finales. Una vez creada una directiva o un estándar que define los niveles necesarios de clasificación de datos, es importante guiar a los usuarios finales sobre cómo dar vida a este marco en su trabajo diario. Esta área es donde se incluyen reglas o directrices de control de clasificación de datos.

Las directrices de control de clasificación de datos ayudarán a los usuarios finales con instrucciones específicas sobre cómo controlar cada nivel de datos de forma adecuada, para distintos medios de almacenamiento a lo largo de su ciclo de vida. Estas directrices ayudan a los usuarios finales a aplicar correctamente reglas en la práctica, por ejemplo, al compartir documentos, enviar correos electrónicos o colaborar en diferentes plataformas y organizaciones.

Los clientes de Microsoft indican que aproximadamente el 50 % de un proyecto de Protección de la información está centrado en el negocio en lugar de técnico, por lo que la formación y la comunicación de los usuarios finales son fundamentales para el éxito.
