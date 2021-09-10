---
title: Crear un marco de clasificación de datos bien diseñado
description: En este artículo, encontrará información general sobre cómo crear un marco de clasificación de datos bien diseñado para Microsoft 365.
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
ms.openlocfilehash: 17aa73258f1ecc4db9cc13a5df08b1aa76a583a7
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947203"
---
# <a name="create-a-well-designed-data-classification-framework"></a>Crear un marco de clasificación de datos bien diseñado

Al desarrollar, renovar o refinar el marco de clasificación de datos, tenga en cuenta los siguientes procedimientos principales:

- No espere pasar de 0 a **100** el día 1: Microsoft recomienda un enfoque de rastreo y ejecución a pie, priorizando las características críticas para la organización y asignandolas a una escala de tiempo. Complete el primer paso, asegúrese de que se ha realizado correctamente y, a continuación, pase a la siguiente fase aplicando las lecciones aprendidas. Recuerde que es posible que su organización aún esté expuesta al riesgo mientras diseña el marco de clasificación de datos, por lo que está bien empezar pequeño con solo unos pocos niveles de clasificación y expandirse más adelante según sea necesario.
- **No solo está** escribiendo para profesionales de ciberseguridad: los marcos de clasificación de datos están diseñados para una amplia audiencia, incluido el miembro promedio del personal, los equipos legales y de cumplimiento, y su equipo de TI. Es importante escribir definiciones claras y fáciles de comprender para los niveles de clasificación de datos, proporcionando ejemplos reales siempre que sea posible. Intente evitar la jerga y considere un glosario para acrónimos y términos altamente técnicos. Por ejemplo, use "Información de identificación personal" y proporcione una definición en lugar de simplemente decir "PII".
- **Los marcos de clasificación de datos están diseñados** para implementarse: para que los marcos de clasificación de datos sean correctos, deben implementarse. Es especialmente relevante al elaborar los requisitos de control para cada nivel de clasificación de datos. Asegúrese de que los requisitos están claramente definidos y que anticipan y abordan cualquier ambigüedad que pueda surgir durante la implementación. Por ejemplo, si tienes un control alrededor de la información de identificación personal, asegúrate de detallar exactamente lo que significa ese control, como la Seguridad Social o el número de pasaporte.
- **Solo vaya pormenorizado si necesita**: Los marcos de clasificación de datos normalmente contienen entre 3 y 5 niveles de clasificación de datos. Pero el hecho de *que se puedan* incluir cinco niveles no significa que *deba*. Tenga en cuenta los siguientes criterios al decidir el número de niveles de clasificación que necesita:

    - Su industria y sus obligaciones reglamentarias asociadas (las industrias altamente reguladas tienden a necesitar más niveles de clasificación)
    - La sobrecarga operativa necesaria para mantener un marco más complejo
    - Los usuarios y su capacidad para cumplir con la mayor complejidad y matiz asociados con más niveles de clasificación
    - Experiencia del usuario y accesibilidad al intentar aplicar la clasificación manual en varios tipos de dispositivos

- **Involucrar a las personas correctas:** tener una parte interesada sénior es fundamental para el éxito, ya que muchos proyectos tienen dificultades para iniciarse o tardar más tiempo sin el respaldo de la administración superior. Los marcos de clasificación de datos suelen pertenecer a equipos de tecnología de la información, pero pueden tener implicaciones legales, de cumplimiento, de privacidad y de administración de cambios. Para asegurarse de que está creando un marco que ayude a proteger su negocio, asegúrese de incluir la privacidad y las partes interesadas legales, como su director de privacidad y el Office de asesor general en el desarrollo de su directiva. Si su organización tiene una división de cumplimiento, profesionales de gobierno de la información o un equipo de administración de registros, también pueden tener valiosas aportaciones. A medida que el marco se va implantando en la empresa, el departamento de comunicaciones también tiene un rol clave que desempeñar para la mensajería interna y la adopción.
- **Equilibrar la seguridad frente** a la comodidad: un error común es redactar un marco de clasificación de datos seguro pero excesivamente restrictivo. Este marco puede haber sido diseñado pensando en la seguridad, pero a menudo es difícil de implementar en la práctica. Si los usuarios necesitan seguir procedimientos complejos, rígidos y que requieren mucho tiempo para aplicar el marco en su vida diaria, siempre existe el riesgo de que ya no crean en su valor y que, finalmente, dejarán de seguir los procedimientos. Este riesgo existe en todos los niveles de la organización, incluidos los administradores de nivel ejecutivo (conjunto de C) dentro de la organización. Un buen equilibrio entre la seguridad y la comodidad junto con las herramientas fáciles de usar suelen llevar a una adopción y un uso más amplios de los usuarios. Si hay vacíos en el marco, no espere hasta que todo sea perfecto para iniciar la implementación. En su lugar, evalúe el riesgo o la diferencia, cree un plan para mitigar y continúe avanzando. Recuerde que la protección de la información es un viaje, no es algo que se activa durante la noche y luego se realiza. Planee, implemente algunas funcionalidades, confirme el éxito e in iteración hasta el siguiente hito a medida que las herramientas evolucionan y los usuarios adquieren madurez y experiencia.

También tenga en cuenta que un marco de clasificación de datos solo aborda *lo* que su organización debe hacer para proteger los datos confidenciales. Los marcos de clasificación de datos suelen ir acompañados de reglas o directrices de tratamiento de datos que *definen* cómo establecer estas directivas desde una perspectiva técnica y tecnológica. En las secciones siguientes, nos ocupamos de algunas instrucciones prácticas sobre cómo llevar el marco de clasificación de datos de un documento de directiva a una iniciativa totalmente implementada y que se puede llevar a cabo.

## <a name="pain-points-in-creating-a-data-classification-framework"></a>Puntos de dolor en la creación de un marco de clasificación de datos

Los esfuerzos de clasificación de datos son, por naturaleza, de amplio alcance, que tocan casi todas las funciones empresariales de una empresa. Debido a este amplio ámbito y a la complejidad de la administración de contenido en entornos digitales modernos, las empresas a menudo se enfrentan a desafíos al saber dónde empezar, cómo administrar una implementación correcta y cómo medir su progreso. Los puntos de dolor comunes a menudo incluyen:

- Diseño de un marco de clasificación de datos sólido y fácil de comprender, incluidos los niveles de clasificación y los controles de seguridad asociados.
- Desarrollar un plan de implementación que incluya confirmar la solución de tecnología adecuada, alinear el plan con los procesos empresariales existentes e identificar el impacto para los empleados.
- Configurar un marco de clasificación de datos dentro de la solución de tecnología elegida y solucionar las diferencias entre las capacidades tecnológicas de la herramienta y el propio marco.
- Establecer una estructura de gobierno que supervise el mantenimiento y el estado en marcha de los esfuerzos de clasificación de datos.
- Identificación de indicadores clave de rendimiento (KPI) específicos para supervisar y medir el progreso.
- Aumentar el conocimiento y la comprensión de las directivas de clasificación de datos, por qué son importantes y cómo cumplirlas.
- Cumplir con las revisiones de auditoría interna destinadas a los controles de pérdida de datos y ciberseguridad.
- Formación y participación de los usuarios para que estén conscientes de la necesidad de una clasificación correcta en su trabajo diario y apliquen las medidas de clasificación adecuadas.

## <a name="change-management-and-training"></a>Administración y aprendizaje de cambios

Las organizaciones usan hoy en día herramientas como Microsoft 365 para implementar su marco de clasificación de datos. El objetivo es intentar automatizar la clasificación de los datos y no aumentar la carga de trabajo. Esta estructura no significa que su organización no tenga la responsabilidad de aumentar el conocimiento de la necesidad de administrar el contenido y proteger a la organización de los riesgos que se debate en este documento. La práctica principal sigue siendo realizar cursos de sensibilización en toda la organización como parte del programa de formación anual. Nuestra experiencia muestra que poner un esfuerzo sólido y completo en la formación de los usuarios, que son el público clave que realiza este trabajo, aumenta su "entrada" al esfuerzo y puede aumentar la adopción y la calidad. Agregar [recomendaciones de etiquetas](/microsoft-365/compliance/apply-sensitivity-label-automatically#recommend-that-the-user-apply-a-sensitivity-label) y sugerencias desde la aplicación puede amplificar estos esfuerzos. Esta formación no necesita ser un curso independiente extenso. Su organización puede incorporarla a otra formación regular, como la formación anual de seguridad de la información y, a continuación, incluir una introducción a los niveles y definiciones de clasificación de datos. El punto principal es que los empleados tienen la idea de que, aunque la herramienta automatiza la clasificación de datos, eso no elimina la responsabilidad general de cada usuario de proteger los datos de acuerdo con la directiva de la empresa.

Además, debe considerar una formación más detallada para los equipos de ti y seguridad de la información para reforzar la preparación operativa. Los equipos que administran la herramienta y el marco de clasificación de datos deben estar en la misma página. Esta coordinación puede requerir que invierta en un programa de formación más sólido que sea más frecuente que anualmente. La inversión en formación más frecuente representa otra vía para reducir los riesgos para la organización. Este equipo es responsable de la implementación y, por lo tanto, podría ser un punto de error si no está capacitado en la herramienta y la directiva.

Si necesitas etiquetar manualmente el contenido de la herramienta, es apropiado desarrollar un grupo de superusuarias que han recibido formación más avanzada. Estos superusuarias estarían comprometidos para situaciones en las que los usuarios deben etiquetar manualmente los documentos con etiquetas de confidencialidad de datos y tendrían un conocimiento profundo del marco de clasificación de datos y los requisitos normativos de la organización.

Por último, su liderazgo debe priorizar la defensa de los comportamientos de seguridad de la información para reforzar a los empleados la importancia de las iniciativas de administración de riesgos. Entre ellas se incluyen el desarrollo e implementación de un marco de clasificación de datos sólido y la asignación de líderes clave para promover la iniciativa, a veces denominadas "embajadoras o campeonas del cambio".

## <a name="governance-and-maintenance"></a>Gobierno y mantenimiento

Después de desarrollar e implementar el marco de clasificación de datos, el gobierno y el mantenimiento continuos serán fundamentales para su éxito. Además de realizar un seguimiento de cómo se usan las etiquetas de confidencialidad en la práctica, deberá actualizar los requisitos de control en función de los cambios en las normativas, las prácticas líderes en ciberseguridad y la naturaleza del contenido que administre. Los esfuerzos de gobierno y mantenimiento pueden incluir:

- Establecer un cuerpo de gobierno dedicado a la clasificación de datos o agregar una responsabilidad de clasificación de datos a la carta de un cuerpo de seguridad de la información existente.
- Definición de roles y responsabilidades para los usuarios que supervisan la clasificación de datos.
- Establecer KPI para supervisar y medir el progreso.
- Seguimiento de prácticas líderes de ciberseguridad y cambios normativos.
- Desarrollar procedimientos operativos estándar que admitan y exijan un marco de clasificación de datos.

## <a name="industry-considerations"></a>Consideraciones del sector

Aunque los principios básicos para desarrollar un marco de clasificación de datos sólido son universales, los detalles de su marco dependerán de la naturaleza de su sector y de los factores de cumplimiento y seguridad únicos que sus datos demande.

Por ejemplo, es posible que las empresas de servicios financieros deban considerar el cumplimiento de varios marcos normativos en función del ámbito de su negocio y las regiones en las que operan. Las empresas de valores de los Estados Unidos deben cumplir con las normativas de cuentas como la Regla [17a-4(f)](/compliance/regulatory/offering-sec-17a-4) de la SEC o la Regla [4511](/microsoft-365/compliance/offering-finra-4511) de FINRA que abordan los requisitos relacionados con la seguridad y retención de libros y registros. Del mismo modo, las empresas que operan en el Reino Unido deben considerar el [cumplimiento de fca](/microsoft-365/compliance/offering-fca-uk).

Las agencias gubernamentales se enfrentan a diversas normativas que rigen sus datos, que varían según el territorio y la naturaleza de su trabajo. En los Estados Unidos, por ejemplo, las agencias gubernamentales y sus agentes que tienen acceso a información fiscal federal (FTI) están sujetos al [IRS 1075](/microsoft-365/compliance/offering-irs-1075), que tiene como objetivo minimizar el riesgo de pérdida, infracción o uso incorrecto de información fiscal federal.

Aunque las empresas de servicios financieros y las agencias gubernamentales se encuentran entre las organizaciones más reguladas del mundo, la mayoría de las empresas tienen consideraciones específicas del sector que deben tenerse en cuenta. Algunos ejemplos incluyen:

- Organizaciones del sector de [la salud que garantizan el cumplimiento de hipaa.](/microsoft-365/compliance/offering-hipaa-hitech)
- Instituciones educativas, desde escuelas K-12 hasta universidades, administrando el [cumplimiento de FERPA.](/microsoft-365/compliance/offering-ferpa)
- Los fabricantes de medicamentos trabajan para cumplir con las directrices [de GxP](/microsoft-365/compliance/offering-gxp) en su país o región en torno a la seguridad de la información.
- Media, retail y muchas otras empresas que se ocupa del cumplimiento [del RGPD.](/microsoft-365/compliance/gdpr)
- Entrega y almacenamiento de contenido de entretenimiento, software e información relacionados con [CDSA](/microsoft-365/compliance/offering-cdsa).
- Seguridad de la información del sector energético que cumple con [el estándar NERC CIP](/microsoft-365/compliance/offering-nerc-cip).

## <a name="implementing-your-data-classification-framework-in-microsoft-365"></a>Implementar el marco de clasificación de datos en Microsoft 365

Una vez desarrollado el marco de clasificación de datos, el siguiente paso es la implementación. El [Centro de cumplimiento de Microsoft 365](https://compliance.microsoft.com/) permite a los administradores detectar, clasificar, revisar y supervisar sus datos de acuerdo con su marco de clasificación de datos. Las etiquetas de confidencialidad se pueden usar para ayudar a proteger los datos mediante la aplicación de varias protecciones, como el cifrado y el marcado de contenido. Se pueden aplicar a los datos manualmente; de forma predeterminada, en función de la configuración de directiva; o automáticamente, como resultado de una condición como la PII identificada.

Para organizaciones más pequeñas u organizaciones con un marco de clasificación de datos relativamente simplificado, es posible que sea suficiente crear una sola etiqueta de confidencialidad para cada uno de los niveles de clasificación de datos. En el ejemplo siguiente se muestra un nivel de clasificación de datos uno a uno a la asignación de etiquetas de confidencialidad:

|**Etiqueta de clasificación**|**Etiqueta de confidencialidad**|**Configuración de la etiqueta**|**Publicado en**|
|:-----------------------|:--------------------|:-----------------|:---------------|
| Sin restricciones | Sin restricciones | Aplicar pie de página "sin restricciones" | Todos los usuarios |
| General | General | Aplicar pie de página "General" | Todos los usuarios |

>[!TIP]
>Durante un piloto de protección de información interna de Microsoft, hubo dificultades para comprender y usar la etiqueta "Personal". Los usuarios estaban confundidos en cuanto a si esto significaba PII o simplemente se relacionaba con un asunto personal. La etiqueta se cambió a "no comercial" para que sea más clara. En este ejemplo se muestra que la taxonomía no necesita ser perfecta desde el principio. Comience con lo que crea correcto, pilote y ajuste la etiqueta en función de los comentarios si es necesario.

Para organizaciones más grandes con un alcance global o necesidades de seguridad de la información más complejas, es posible que esta relación uno a uno entre el número de niveles de clasificación en la directiva y el número de etiquetas de confidencialidad en el entorno de Microsoft 365 sea un desafío. Este desafío es especialmente cierto en las organizaciones globales donde un nivel de clasificación de datos determinado, como "Restringido", puede tener una definición diferente o un conjunto de controles diferente según la región.

Para obtener más información sobre la implementación, vea [Understand data classification](/microsoft-365/compliance/data-classification-overview) y Learn about sensitivity [labels](/microsoft-365/compliance/sensitivity-labels).

## <a name="references"></a>Referencias

- [Ofertas de cumplimiento de Microsoft](/microsoft-365/compliance/offering-home)
