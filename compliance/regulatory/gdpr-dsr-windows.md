---
title: Configuración del procesador de datos de diagnóstico de Windows Solicitudes del sujeto de datos para el GDPR y la CCPA
description: Aprenda a utilizar los productos, servicios y herramientas de administración de Microsoft para encontrar datos personales y realizar acciones sobre ellos para responder a las DSR.
keywords: Microsoft 365, Microsoft 365 Educación, documentación de Microsoft 365, RGPD
localization_priority: Priority
ROBOTS: NOINDEX, NOFOLLOW
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmaz
manager: laurawi
ms.reviewer: delinat
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
hideEdit: true
ms.openlocfilehash: b79d856591566aa1e13633377600c605429ee68e
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377967"
---
# <a name="windows-diagnostic-data-processor-configuration-data-subject-requests-for-the-gdpr-and-ccpa"></a>Configuración del procesador de datos de diagnóstico de Windows Solicitudes del sujeto de datos para el GDPR y la CCPA

>[!NOTE]
>Este tema se aplica a las ediciones Windows 10 Enterprise, Pro y Education, versión 1809 con la actualización de julio de 2021 y posteriores.

## <a name="introduction-to-data-subject-requests-dsrs"></a>Introducción a las solicitudes de los interesados (DSR)

El Reglamento General de Protección de Datos (RGPD) otorga derechos a las personas (denominadas _interesados_ en el reglamento) para administrar los datos personales recopilados por una empresa u otro tipo de agencia u organización (denominado _responsable de los datos_ o simplemente _responsable_). Los datos personales se definen ampliamente en el RGPD como cualquier dato que guarde relación con una persona física identificada o identificable. El RGPD ofrece a los interesados derechos específicos sobre sus datos personales, como la obtención de copias de ellos, la solicitud de modificaciones, la restricción de tratamiento, la eliminación o la recepción en un formato electrónico que permita su transferencia a otro responsable. Una solicitud formal de un interesado a un responsable para que realice una acción sobre sus datos personales se denomina _Solicitud del interesado_ o DSR.

De manera similar, la Ley de privacidad del consumidor de California (CCPA por sus siglas en inglés), establece derechos y obligaciones de privacidad para los consumidores de California, incluyendo derechos similares a los derechos de las solicitudes del interesado del RGPD, como el derecho a borrar, acceder y recibir (portabilidad) su información personal. La CCPA también prevé casos de divulgación de información, protecciones contra la discriminación en el ejercicio de derechos y requisitos de "cancelación/suscripción" para ciertas transferencias de datos clasificadas como "ventas". Las ventas se definen de forma amplia para incluir el uso compartido de datos con ánimo de lucro. Para obtener más información sobre la CCPA, consulte la [Ley de Privacidad de los Consumidores California](/microsoft-365/compliance/offering-ccpa) y las [Preguntas más frecuentes sobre la privacidad del consumidor de California](/microsoft-365/compliance/ccpa-faq).

En esta guía se explica cómo usar los productos, servicios y herramientas administrativas de Microsoft para ayudar a nuestros clientes responsables de los datos a encontrar datos personales y actuar sobre ellos para responder a solicitudes de interesado. En concreto, esto abarca cómo encontrar datos personales hospedados en la nube de Microsoft, cómo tener acceso a ellos y cómo actuar en consecuencia. Este es un breve resumen de los procedimientos descritos en esta guía:

1. **Acceso:** Recupere los datos de diagnóstico de Windows asociados con un sujeto de datos y, si se solicita, haga una copia de ellos que pueda estar disponible para el sujeto de datos.
2. **Eliminar**: elimina de forma permanente los datos de diagnóstico de Windows asociados con un sujeto de datos.
3. **Exportar**: Proporcionar una copia electrónica (en un formato legible por máquina) de los datos de diagnóstico de Windows al interesado.

La información personal bajo la CCPA es cualquier información relacionada con una persona identificada o identificable. No hay distinción entre los roles privados, públicos o laborales de una persona. La definición del término "información personal" es, a grandes rasgos, similar a la que el RGPD da al término "datos personales". Sin embargo, la CCPA también incluye datos domésticos y familiares. Para obtener más información sobre la CCPA, consulte la [Ley de Privacidad de los Consumidores California](/microsoft-365/compliance/offering-ccpa) y las [Preguntas más frecuentes sobre la privacidad del consumidor de California](/microsoft-365/compliance/ccpa-faq).

Cada sección de esta guía describe los procedimientos técnicos que una organización de controlador de datos puede tomar para responder a un DSR para datos de diagnóstico de Windows recopilados por Microsoft cuando la configuración del procesador de datos de diagnóstico de Windows está habilitada.

## <a name="terminology"></a>Terminología

En la siguiente lista, se proporcionan definiciones de términos relevantes para esta guía.

* _Poseedor:_ la persona física o jurídica, entidad pública, agencia u organismo que, solo o junto a otras personas, determina los fines y los medios del procesamiento de datos personales; donde los fines y los medios de dicho procesamiento están determinados por la ley de la Unión Europea o de los Estados miembros, el poseedor o los criterios específicos para su designación pueden estar proporcionados por la ley de la Unión Europea o de los Estados miembros.

* _Datos personales y titular de los datos:_ Cualquier información sobre una persona física identificada o identificable ("interesado"); una persona física identificable es una que puede identificarse, directa o indirectamente, especialmente en referencia a un identificador, con un nombre, un número de identificación, datos de ubicación, un identificador en línea o uno o más factores específicos físicos, fisiológicos, genéticos, mentales, económicos, culturales o de identidad social de esa persona física.

* _Encargado de los datos:_ una persona física o jurídica, una autoridad pública, una agencia u otro organismo que procesa datos personales en nombre del responsable.

* _Datos de cliente_: todos los datos, incluidos el software y todos los archivos de texto, sonido, vídeo o imagen, proporcionados a Microsoft por un cliente o en su representación mediante el uso del servicio empresarial. 

* _Datos de diagnóstico de Windows_: datos técnicos de los dispositivos Windows sobre el dispositivo y sobre el funcionamiento de Windows y el software relacionado. Se usa para mantener Windows actualizado, seguro, confiable, eficaz y realizar mejoras en el producto. Algunos ejemplos de datos de diagnóstico de Windows son el tipo de hardware que se usa, las aplicaciones que hay instaladas y el uso que se les da, y la información de confiabilidad sobre los controladores de dispositivos. Algunos componentes y aplicaciones de Windows se conectan directamente a servicios Microsoft, pero los datos que intercambian no son datos de diagnóstico de Windows. Por ejemplo, intercambiar la ubicación de un usuario para obtener la información local del tiempo o las noticias locales no es un ejemplo de datos de diagnóstico de Windows.

## <a name="how-to-use-this-guide"></a>Cómo usar esta guía

Al habilitar la configuración del procesador de datos de diagnóstico de Windows, se convierte en el controlador del datos de diagnóstico de Windows recopilado de los dispositivos. Para obtener más información sobre esta configuración, consulte [Configurar datos de diagnóstico de Windows en su organización](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

## <a name="windows-diagnostic-data"></a>Datos de diagnóstico de Windows

Microsoft le proporciona la capacidad de acceder, eliminar y exportar datos de diagnóstico de Windows asociados al uso por parte de un usuario de los dispositivos habilitados con la configuración del procesador de datos de diagnóstico de Windows.

> [!IMPORTANT]
> Algunos datos de diagnóstico de Windows solo están asociados a un identificador de dispositivo y no están asociados a un usuario específico. Este tipo de datos de nivel de dispositivo no se exporta y se elimina de nuestros sistemas en un plazo de 30 días.<br><br>
> No se admite la capacidad de rectificar los datos de diagnóstico de Windows. Los datos de diagnóstico de Windows constituyen acciones realizadas en Windows. Modificar este tipo de datos podría afectar a los registros históricos de acciones, lo que aumentaría los riesgos de seguridad y perjudicaría la fiabilidad.

En la sección siguiente se proporcionan los pasos para ejecutar una solicitud de interesado para datos de diagnóstico de Windows asociada a un identificador de usuario de Azure Active Directory (AAD). Para obtener más información, consulte [Windows 10 y cumplimiento de la privacidad: una guía para profesionales de TI y cumplimiento](/windows/privacy/windows-10-and-privacy-compliance).

## <a name="executing-dsrs-against-windows-diagnostic-data"></a>Ejecución de las DSR con respecto a los datos de diagnóstico de Windows

Microsoft ofrece la posibilidad de acceder a determinados datos de diagnóstico de Windows, así como de eliminarlos y exportarlos, a través del Portal Azure y también directamente a través de interfaces de programación de aplicaciones (API) ya existentes.

### <a name="step-1-access"></a>Paso 1: Acceso

Microsoft proporciona una forma para que el administrador de inquilinos dentro de su organización acceda a los datos de diagnóstico de Windows asociados con el uso de un usuario en particular de un dispositivo habilitado con la configuración del procesador de datos de diagnóstico de Windows. Los datos recuperados para una solicitud de acceso se proporcionarán, mediante exportación, en un formato legible por máquina y se proporcionarán en archivos que permitirán al usuario saber con qué dispositivos y servicios están asociados los datos. Como se señaló anteriormente, los datos recuperados no incluirán datos que puedan comprometer la seguridad o estabilidad del dispositivo Windows.

El Azure Portal proporciona al administrador de inquilinos del cliente empresarial la capacidad de administrar las solicitudes de acceso de DSR. [Azure DSR, Parte 2, Paso 3: Exportar](/microsoft-365/compliance/gdpr-dsr-azure#step-3-export), describe cómo ejecutar una solicitud de acceso DSR para datos de diagnóstico de Windows, a través de la exportación, a través del Portal de Azure.

### <a name="step-2-delete"></a>Paso 2: Eliminar

Microsoft proporciona una forma de ejecutar peticiones de eliminación de DSR basadas en el objeto de Azure Active Directory de un usuario particular.

Para las solicitudes de eliminación basadas en el usuario, Microsoft ofrece dos soluciones.  Existe una experiencia de portal que proporciona al administrador de inquilinos del cliente empresarial la capacidad de administrar las solicitudes de eliminación de DSR. [Azure DSR, parte 1, paso 5: eliminar](/microsoft-365/compliance/gdpr-dsr-azure#step-5-delete), describe cómo ejecutar una solicitud de eliminación de DSR para datos de diagnóstico de Windows a través del Azure Portal mediante la eliminación de un usuario y los datos asociados.

Microsoft también ofrece la posibilidad de eliminar usuarios, que a su vez eliminarán los datos de diagnóstico de Windows, directamente a través de una interfaz de programación de aplicaciones (API) preexistente. Los detalles se describen en la [documentación de referencia de la API](/graph/api/directory-deleteditems-delete).

>[!IMPORTANT]
>La eliminación de datos recopilados no detiene la recopilación posterior del dispositivo. Para desactivar la recopilación de datos, siga el procedimiento descrito en la [documentación de referencia del servicio correspondiente](/windows/privacy/configure-windows-diagnostic-data-in-your-organization#enterprise-management).

### <a name="step-3-export"></a>Paso 3: exportar

El administrador de espacio empresarial es la única persona de su organización que puede tener acceso a datos de diagnóstico de Windows asociadas al uso de un usuario determinado de un dispositivo habilitado con la configuración del procesador datos de diagnóstico de Windows. Los datos recuperados para una solicitud de exportación se proporcionarán en un formato legible por una máquina y se facilitarán en archivos que permitirán al usuario saber a qué dispositivos y servicios se asocian los datos. Como se ha señalado anteriormente, los datos recuperados no incluirán datos que puedan comprometer la seguridad o la estabilidad del dispositivo Windows. [Azure DSR, parte 2, paso 3: Exportar](/microsoft-365/compliance/gdpr-dsr-azure#step-3-export), describe cómo ejecutar una solicitud de exportación de DSR para datos de diagnóstico de Windows a través del Azure Portal.

Microsoft también ofrece la capacidad de exportar datos de diagnóstico de Windows directamente a través de una interfaz de programación de aplicaciones (API) preexistente. Los detalles se describen en la [documentación de referencia de la API](/graph/api/user-exportpersonaldata).

## <a name="notify-us-about-exporting-or-deleting-issues"></a>Avísenos sobre los problemas de exportación o eliminación

Si tiene problemas al exportar o eliminar datos de diagnóstico de Windows desde Azure Portal, vaya a la hoja **Ayuda + Soporte técnico** de Azure Portal y envíe un nuevo ticket en **Administración de suscripciones> Solicitudes de privacidad y cumplimiento para suscripciones> Hoja de privacidad y Solicitudes de GDPR**.
