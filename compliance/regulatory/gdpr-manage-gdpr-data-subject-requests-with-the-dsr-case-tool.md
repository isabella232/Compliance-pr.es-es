---
title: Administrar las solicitudes de los interesados del RGPD con la herramienta de casos de DSR en el Centro de cumplimiento de Microsoft 365
description: Obtenga información sobre cómo administrar las solicitudes de los interesados del Reglamento general de protección de datos (RGPD) de la UE con la herramienta de casos de DSR.
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: high
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- SPO_Content
- MS-Compliance
ms.assetid: ce9eb942-3589-42cb-88fd-1576ecb09c5c
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: e29c6501ce4c8f1ee645a8c4b5bf22eee6e9cab8
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "59160153"
---
# <a name="manage-gdpr-data-subject-requests-with-the-dsr-case-tool-in-the-microsoft-365-compliance-center"></a>Administrar solicitudes de los interesado del RGPD con la herramienta de casos de DSR en el Centro de cumplimiento de Microsoft 365

El Reglamento general de protección de datos (RGPD) de la UE trata de proteger y facilitar los derechos de privacidad individuales dentro de la Unión Europea (UE). El GDPR proporciona a los individuos de la Unión Europea (conocidos como interesados) el derecho a acceder, recuperar, corregir, borrar y restringir el procesamiento de sus datos personales. Según el GDPR, los datos personales hacen referencia a cualquier información relacionada con una persona física identificada o identificable. Una solicitud formal de una persona de la organización para que realice una acción sobre sus datos personales se denomina Solicitud del interesado o DSR. Para obtener información detallada sobre cómo responder a las DSR de datos en Office 365, vea [Guía de solicitud de inquilino en Office 365](https://go.microsoft.com/fwlink/?linkid=871169 ).
  
Para administrar las investigaciones en respuesta a un DSR enviado por una persona de la organización, puede usar la herramienta de casos de DSR del Centro de cumplimiento para buscar contenido almacenado en:
  
- Cualquier buzón de usuario de su organización. Esto incluye las conversaciones de Skype Empresarial y los chats uno a uno en Microsoft Teams

- Todos los buzones asociados a un Grupo de Microsoft 365 y todos los buzones de equipo en Microsoft Teams

- Todos los sitios de SharePoint Online y OneDrive para la Empresa de la organización

- Todos los sitios de Teams y sitios de grupo de Microsoft 365 de su organización

- Todas las carpetas públicas de Exchange Online

Con la herramienta de casos de DSR puede:
  
- Crear un caso independiente para cada investigación de DSR.

- Controlar quién tiene acceso al caso de DSR agregando personas como miembros del caso. Solo los miembros pueden acceder al caso y solo pueden ver sus propios casos en la lista de la página de **casos de DSR** en el Centro de cumplimiento. También, puede asignar permisos diferentes a distintos miembros del mismo caso. Por ejemplo, puede permitir que algunos miembros solo vean el caso y los resultados de búsqueda, mientras que otros son capaces de crear búsquedas y exportar resultados de búsqueda.

- Usar la búsqueda integrada para buscar todo el contenido relacionado o cargado por un determinado interesado.

- Opcionalmente, revise la consulta de búsqueda integrada y vuelva a ejecutar la búsqueda para restringir los resultados de búsqueda.

- Agregar otras búsquedas de contenido asociadas al caso de DSR. Esto incluye la creación de búsquedas que devuelven elementos indizados parcialmente y registros generados por el sistema desde el Servicio de roaming de Office.

- Exportar datos como respuesta a una solicitud de exportación o a un acceso de DSR.

- Eliminar los casos cuando se complete el proceso de investigación de DSR. Se quitarán todas las búsquedas de contenido y trabajos de exportación asociados al caso.

Este es el proceso de alto nivel para usar la herramienta de casos de DSR para administrar investigaciones de DSR:
  
[Paso 1: Asignar los permisos eDiscovery a miembros de casos potenciales](#step-1-assign-ediscovery-permissions-to-potential-case-members)

[Paso 2: Crear un caso de DSR y agregar miembros](#step-2-create-a-dsr-case-and-add-members)

[Paso 3: Ejecutar la consulta de búsqueda](#step-3-run-the-search-query)

[Paso 4: Exportar los datos](#step-4-export-the-data)

[(Opcional) Paso 5: Revisar la consulta de búsqueda integrada](#optional-step-5-revise-the-built-in-search-query)

[Más información acerca del uso de la herramienta de casos de DSR](#more-information-about-using-the-dsr-case-tool)
  
> [!IMPORTANT]
> Nuestras herramientas pueden ayudar a los administradores a realizar solicitudes de exportación o acceso de DSR permitiéndoles usar la búsqueda integrada y la función de exportación que se encuentra en la herramienta de casos de DSR. La herramienta ayuda a facilitar un mejor método de esfuerzo para exportar datos relevantes para una solicitud DSR enviada por un interesado. Sin embargo, es importante tener en cuenta que los resultados de búsqueda pueden variar en función del interesado o de las acciones del administrador realizadas que pueden afectar a si un elemento se consideraría o no como "datos personales" con fines de exportación. Por ejemplo, si el interesado era la última persona en modificar un archivo que no creó, es posible que el archivo no se devuelva en los resultados de la búsqueda. De forma similar, un administrador podría exportar datos sin incluir elementos parcialmente indizados o todas las versiones de documentos de SharePoint. Por lo tanto, las herramientas proporcionadas pueden ayudar a facilitar el acceso y la exportación de solicitudes de datos. No obstante, los resultados están sujetos a escenarios de uso específicos de administradores e interesados.
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a>Paso 1: Asignar permisos de exhibición de documentos electrónicos a posibles miembros del caso

De forma predeterminada, un administrador global puede acceder a la herramienta de casos de DSR en el Centro de cumplimiento de Microsoft 365. Por diseño, otros usuarios como un responsable de privacidad de datos, un administrador de recursos humanos u otras personas implicadas en investigaciones de DSR no tienen acceso a la herramienta del caso de DSR y tendrán que asignar los permisos adecuados para acceder a la herramienta. La manera más sencilla de hacerlo es ir a la página de **Permisos** del Centro de cumplimiento y añadir usuarios al grupo de roles del Supervisor de eDiscovery. También tiene que asignar estos permisos para que pueda agregarlos como miembros del caso de DSR que cree en el paso 2. 
  
Para obtener instrucciones paso a paso, vea [Asignar permisos de eDiscovery](/microsoft-365/compliance/assign-ediscovery-permissions).
  
> [!NOTE]
> De forma predeterminada, los administradores globales (u otros miembros del Grupo de roles de administración de la organización en el Centro de cumplimiento) no tienen los permisos necesarios para exportar los resultados de la Búsqueda de contenido (vea el paso 4 de este artículo). Para abordar esto, un administrador puede agregarse a sí mismo como miembro del grupo de roles de administración de eDiscovery. 
  
## <a name="step-2-create-a-dsr-case-and-add-members"></a>Paso 2: Crear un caso de DSR y agregar miembros

El siguiente paso consiste en crear un caso de DSR. Al crear un caso, puede elegir iniciar la búsqueda integrada o puede crear el caso sin iniciar la búsqueda. El procedimiento siguiente le indica cómo crear un caso sin iniciar la búsqueda y, a continuación, le mostrará cómo agregar miembros al caso.
  
1. Vaya a <https://compliance.microsoft.com> e inicie sesión con su cuenta profesional o educativa.

2. En el panel izquierdo del Centro de cumplimiento de Microsoft 365, seleccione **Solicitudes de los interesados**.

3. En la página de **Solicitudes de los interesados**, haga clic en **Crear un caso**.

4. En la página del asistente de **Nuevo caso de DSR**, asigne un nombre al caso, escriba una descripción opcional y, después, haga clic en **Siguiente**. El nombre del caso debe ser exclusivo en la organización.

    > [!TIP]
    > Considere la posibilidad de agregar el nombre de la persona que envió la solicitud de DSR que está investigando en el nombre y/o descripción del nuevo caso. Tenga en cuenta que solo los miembros de este caso (y los administradores de eDiscovery) podrán ver el caso en la lista de casos de la página **Solicitudes del interesado**.
  
5. En la página **Detalles de la solicitud**, en **Interesado (la persona que presentó esta solicitud)**, seleccione la persona para la que desea buscar y exportar datos y después haga clic en **Siguiente**.

6. En la página **Confirmar la configuración del caso**, puede cambiar el nombre y la descripción del caso y seleccionar un interesado diferente. En caso contrario, haga clic en **Guardar**.

    Se muestra una página que confirma que se ha creado el nuevo caso de DSR.

    ![Inicie la búsqueda o cierre la página del nuevo caso de DSR.](../media/b5e62c2c-cafe-4a8d-a38c-789ed9f9ccbd.png)
  
    En este punto, puede llevar a cabo una de estas dos cosas:

    a. Al hacer clic en **Mostrar resultados de búsqueda** se inicia la búsqueda. Esa es la selección predeterminada. La búsqueda integrada que se ejecuta al seleccionar esta opción y los resultados devueltos se analizan en el paso 3.

    b. Al hacer clic en **Finalizar** se cierra el nuevo caso de DSR sin iniciar la búsqueda integrada. Al seleccionar esta opción, se muestra el nuevo caso de DSR en la página **Solicitudes del interesado**.

7. Haga clic en **Finalizar** para poder acceder al nuevo caso de DSR y agregarle miembros.

8. En la página **Solicitudes del interesado**, haga clic en el nombre del caso de DSR que creó.

9. En la página desplegable **Controlar este caso**, en **Administrar miembros**, haga clic en **Agregar**.

    En **Usuarios**, se muestra una lista de personas a las que se les han asignado los permisos de eDiscovery adecuados. Las personas a las que asignó los permisos de eDiscovery en el paso 1 se mostrarán en esta lista.

10. Seleccione a las personas que desea agregar como miembros del caso de DSR, haga clic en **Agregar** y, después, guarde los cambios.

    También puede agregar un grupo de roles como miembros del caso de DSR haciendo clic en **Agregar** en **Administrar grupos de roles**. 

## <a name="step-3-run-the-search-query"></a>Paso 3: Ejecutar la consulta de búsqueda

Una vez creado un caso DSR y agregados los miembros, el siguiente paso es ejecutar la búsqueda incorporada que está asociada al caso. Esta consulta de búsqueda predeterminada permite hacer lo siguiente:
  
- Busca en todos los buzones de su organización todos los elementos de correo electrónico que el interesado ha enviado o recibido. Esto se consigue con la propiedad de correo  *Participantes*, que busca al interesado en todos los campos personas de un mensaje de correo. Esta propiedad devuelve los elementos en los que el interesado está en los campos **De**, **Para**, **CC** y **CCO**. En las carpetas públicas en Exchange Online también se buscan los mensajes enviados o recibidos por el interesado.

- Busca documentos y elementos creados o cargados por el interesado en todos los sitios de su organización. Esto se consigue por medio de las siguientes propiedades del sitio:

  - La propiedad  *Author*  devuelve los elementos en los que el interesado aparece en el campo de autor de los documentos de Office. Este valor persiste, incluso si otra persona copia y carga el documento.

  - La propiedad  *CreatedBy*  devuelve los elementos creados o cargados por el interesado.

Este es el aspecto de la consulta de palabras clave para la búsqueda integrada que se crea automáticamente al crear un caso de DSR.
  
```powershell
participants:"<email address>" OR author:"<display name>" OR createdby:"<display name>"
```

Por ejemplo, si el nombre del interesado es Ina Leonte, la consulta de palabras clave tendría el siguiente aspecto:
  
```powershell
participants:"ina@contoso.com" OR author:"Ina Leonte" OR createdby:"Ina Leonte"
```

 **Para ejecutar la búsqueda integrada de un caso de DSR:**
  
1. En el Centro de cumplimiento de Microsoft 365, haga clic en **Solicitudes de los interesados**, seleccione el caso que creó en el paso 2 y, a continuación, haga clic en **Abrir caso**.

2. Haga clic en la pestaña **Búsquedas** en la parte superior de la página y, después, haga clic en la casilla situada junto a la búsqueda integrada que se creó cuando al crear el caso de DSR. La búsqueda tiene el mismo nombre que el caso de DSR. 

3. En la página del control flotante de búsqueda, haga clic en **Volver a ejecutar** para iniciar la búsqueda.

4. Una vez completada la búsqueda, haga clic en **Vista previa de los resultados** para obtener una vista previa de los resultados de la búsqueda. Para más información, vea [Vista previa de los resultados de la búsqueda](/microsoft-365/compliance/content-search#preview-search-results).

    > [!TIP]
    > También puede ver las estadísticas de la consulta de búsqueda para ver el número de elementos de buzón y de sitio devueltos por la búsqueda, y las ubicaciones de contenido principales que contienen elementos que coinciden con la consulta de la búsqueda. Para mas información, vea [Ver información y estadísticas sobre una búsqueda](/microsoft-365/compliance/content-search#view-information-and-statistics-about-a-search). 
  
Puede editar la consulta de búsqueda integrada, cambiar las ubicaciones de contenido en las que se buscan y, después, volver a ejecutar la búsqueda. Vea el [Paso 5](#optional-step-5-revise-the-built-in-search-query) para obtener más información.
  
## <a name="step-4-export-the-data"></a>Paso 4: Exportar los datos

Después de ejecutar una búsqueda integrada, puede exportar los resultados de la búsqueda. Como alternativa, antes de exportar los datos, puede que quiera revisar la consulta para reducir el número de resultados de la búsqueda. Vea el Paso 5 para obtener más información sobre cómo acotar los resultados de la búsqueda.
  
Al exportar los resultados de la búsqueda, los elementos de buzón se pueden descargar en archivos PST o como mensajes individuales. Al exportar contenido de las cuentas de SharePoint y OneDrive, se exportan copias de documentos nativos de Office y otros documentos. En los resultados de la búsqueda se incluye un archivo de resultados que contiene información sobre todos los elementos exportados. Para obtener más información detallada sobre la exportación, vea [Exportar resultados de la búsqueda de contenido](/microsoft-365/compliance/export-search-results).
  
> [!NOTE]
> De forma predeterminada, los administradores globales (u otros miembros del Grupo de roles de administrador de la organización en el Centro de cumplimiento) no tienen los permisos necesarios para exportar los resultados de la Búsqueda de contenido. Para abordar esto, un administrador puede agregarse a sí mismo como miembro del grupo de roles de administración de eDiscovery. 
  
El equipo que usa para exportar datos debe cumplir los siguientes requisitos del sistema:
  
- Versiones de 32 o 64 bits de Windows 7 y versiones posteriores
    
- Microsoft .NET Framework 4.7
    
- Un explorador compatible:
    
  - Microsoft Edge
    
    O bien
    
  - Microsoft Internet Explorer 10 y versiones posteriores
    
    > [!NOTE]
    > Microsoft no produce extensiones de terceros ni complementos para aplicaciones ClickOnce. No se admite la exportación de datos con un explorador no compatible con extensiones o complementos de terceros. 
  
 **Para exportar datos de la búsqueda integrada en un caso de DSR:**
  
1. En el Centro de cumplimiento de Microsoft 365, haga clic en **Solicitudes de los interesados**, seleccione el caso que creó en el paso 2 y, a continuación, haga clic en **Abrir caso**.

2. Haga clic en la pestaña **Búsquedas** en la parte superior de la página y, después, haga clic en la casilla situada junto a la búsqueda integrada que se creó cuando al crear el caso de DSR.

3. En la página del control flotante, haga clic en **Exportar resultados**. 

4. En la página **Opciones de exportación**, seleccione las siguientes opciones recomendadas para solicitudes de exportación de DSR. 

    ![Establecer la configuración de exportación.](../media/25416b79-57da-46a1-ae07-e640602a8fa4.png)
  
    a. En **Opciones de salida**, seleccione la primera opción (**Todos los elementos, excluidos los que tienen un formato no reconocido, están cifrados o no se han indexado por otras razones**) para exportar solo elementos indizados. El motivo por el que no quiere exportar elementos indizados parcialmente desde la búsqueda integrada es que también se exportarán elementos indizados parcialmente de otros usuarios. Para exportar solo los elementos indizados parcialmente para el interesado, le recomendamos que cree una búsqueda independiente. Para más información, vea [Exportar elementos indizados parcialmente](#exporting-partially-indexed-items) en la sección "Más información sobre el uso de la herramienta de casos de DSR".

    b. En **Exportar contenido de Exchange como**, seleccione la tercera opción: **Un archivo PST que contenga todos los mensajes en una sola carpeta**. Dado que algunos de los resultados pueden ser de elementos originados en el buzón de otro usuario, esta opción simplemente enumera el elemento en una sola carpeta sin indicar el buzón actual y es la mejor opción para usar al desduplicar los resultados, tal y como se recomienda en el elemento siguiente. Esta opción también permite al interesado revisar los elementos en orden cronológico (los elementos se ordenan por fecha de envío) sin tener que navegar por la estructura de carpetas del buzón original para cada elemento.

    c. Seleccione la opción **Habilitar la desduplicación** para excluir mensajes de correo electrónico duplicados. Se recomienda esta opción, ya que la búsqueda integrada busca en todos los buzones de la organización. Por lo tanto, si se encuentran varias copias del mismo mensaje en los buzones en los que se buscaron, esta opción significa que solo se exportará una copia de un mensaje. Esta opción, al exportar conjuntamente los mensajes en un archivo PST en una sola carpeta, da como resultado la mejor experiencia de usuario para las solicitudes de exportación de DSR. El informe de exportación Results.csv enumera todas las ubicaciones en las que se encontraron mensajes duplicados.

    Opcionalmente, puede seleccionar la opción **Incluir versiones para los documentos de SharePoint** y exportar todas las versiones de documentos de SharePoint y OneDrive. Es necesario que el control de versiones esté activado para las bibliotecas de documentos. Esta opción ayuda a garantizar que se exportan todos los datos relevantes.

5. Después de elegir la configuración de exportación, haga clic en **Exportar**.

    Los resultados de búsqueda se preparan para su descarga, lo que significa que se han cargado en el área de almacenamiento de Azure para la organización en la nube de Microsoft. Los pasos siguientes muestran cómo descargar estos datos en el equipo local.

6. Haga clic en la pestaña **Exportar** para mostrar el trabajo de exportación que creó. Los trabajos de exportación tienen el mismo nombre que la búsqueda correspondiente con **_Export** anexado al final del nombre de la búsqueda.

7. Haga clic en el trabajo de exportación que acaba de crear para mostrar la página desplegable de exportación. En esta página se muestra información sobre la búsqueda, como el tamaño y el número total de elementos que se exportarán y el porcentaje de los elementos que se han transferido a un área de almacenamiento de Azure. Haga clic en **Actualizar** para actualizar la información de estado de carga. 

8. En **Clave de exportación**, haga clic en **Copiar al Portapapeles**. Esta clave se usa para descargar los resultados de la búsqueda en el paso 11.

9. Haga clic en el ![icono Exportar resultados de búsqueda.](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Descargar** resultados en la parte superior de la página desplegable de exportación. 

10. En la ventana emergente de la parte inferior de la página, haga clic en **Abrir** para abrir la **Herramienta de exportación de eDiscovery**. La **Herramienta de exportación de eDiscovery** se instalará la primera vez que descargue los resultados de búsqueda. 

11. En la **Herramienta de exportación de eDiscovery**, pegue la clave de exportación que ha copiado en el paso 8 en el cuadro correspondiente.

12. Haga clic en **Examinar** para especificar la ubicación en la que desea descargar los archivos de los resultados de la búsqueda. 

    > [!NOTE]
    > Debido a la gran cantidad de actividad de disco (lecturas y escrituras), debe descargar los resultados de búsqueda en una unidad de disco local; no las descargue en una unidad de red asignada o en otra ubicación de red. 
  
13. Haga clic en **Iniciar** para descargar los resultados de la búsqueda en el equipo. 

    La **Herramienta de exportación de exhibición de documentos electrónicos** muestra información del estado acerca del proceso de exportación, incluida una estimación del número (y tamaño) de los elementos restantes que se van a descargar. Cuando el proceso de exportación se completa, puede acceder a los archivos en la ubicación donde se descargaron. Para obtener más información sobre los informes que se incluyeron al descargar resultados de Búsqueda de contenido, vea la sección [Más información](/microsoft-365/compliance/export-search-results#more-information) en "Exportar resultados de búsqueda de contenido". 

Después de exportar los datos, los resultados de búsqueda y los informes de exportación se encuentran en una carpeta que tiene el mismo nombre que el caso de DSR. Los archivos PST que contienen los elementos del buzón se encuentran en una subcarpeta nombrada **Exchange**. Los documentos y otros elementos de los sitios se encuentran en una subcarpeta nombrada **SharePoint**.
  
## <a name="optional-step-5-revise-the-built-in-search-query"></a>(Opcional) Paso 5: Revisar la consulta de búsqueda integrada

Después de ejecutar la búsqueda integrada, puede revisarla para restringir el ámbito y devolver menos resultados de búsqueda. Para ello, puede agregar condiciones a la consulta. Una condición está conectada de forma lógica a la consulta de palabra clave por el operador **Y**. Eso significa que se van a devolver en los resultados de la búsqueda, los elementos deben satisfacer tanto la consulta de palabra clave como cualquier condición que añada. De esta manera, las condiciones permiten restringir los resultados. Si agrega dos o más condiciones únicas a una consulta de búsqueda (condiciones que especifican propiedades diferentes), dichas condiciones están conectadas lógicamente mediante el operador **Y**. Esto significa que solo se devuelven los elementos que satisfacen todas las condiciones (además de cualquier consulta de palabras clave). Si agrega varios valores (separados por comas o por punto y coma) a una única condición, esos valores se conectan mediante el operador **O**. Eso significa que se devuelven los elementos que contengan cualquiera de los valores especificados para la propiedad en la condición.
  
Estos son algunos ejemplos de las condiciones que puede agregar a la consulta de búsqueda integrada de un caso de DSR. El nombre de la propiedad real usada en una consulta de búsqueda se muestra entre paréntesis.
  
- **Tipo de archivo ( `filetype`)**: especifica la extensión de un documento o archivo. Use esta condición para buscar documentos y archivos creados por aplicaciones específicas de Office, como Word, Excel y OneNote. 

- **Tipo de mensaje ( `kind`)**: especifica el tipo de elemento de correo electrónico que se buscará. Por ejemplo, puede usar la sintaxis  `kind:email OR kind:im` para devolver solo los mensajes de correo electrónico y las conversaciones de Skype Empresarial o los chats uno a uno en Microsoft Teams.

- **Etiqueta de cumplimiento (`compliancetag`)**: especifica una etiqueta asignada a un mensaje de correo electrónico o a un documento. Esta condición devuelve los elementos clasificados con una etiqueta específica. Las etiquetas se usan para clasificar correos electrónicos y documentos para el gobierno de datos y para aplicar reglas de retención basadas en la clasificación definida por la etiqueta. Esta condición es útil para las investigaciones de solicitudes de interesado porque es posible que su organización utilice etiquetas para clasificar contenido relacionado con la privacidad de datos o que contenga datos personales o información confidencial. Para el valor de esta condición, use el nombre de la etiqueta completo o la primera parte del nombre de la etiqueta con un carácter comodín. Para obtener más información, vea [Información sobre las etiquetas y directivas de retención](/microsoft-365/compliance/retention).

Para obtener una lista y descripciones de todas las condiciones disponibles en la herramienta de caso de DSR, vea [Condiciones de búsqueda en el artículo](/microsoft-365/compliance/keyword-queries-and-search-conditions#search-conditions) en el artículo "Consultas de palabras clave y condiciones de búsqueda para la Búsqueda de contenido". 
  
### <a name="changing-the-content-locations-that-are-searched"></a>Cambiar las ubicaciones de contenido en las que se buscan

Además de revisar la búsqueda integrada de un caso de DSR, también puede cambiar las ubicaciones de contenido que se buscan. Como se ha explicado anteriormente, la búsqueda integrada busca en todos los buzones y sitios de la organización, así como en las carpetas públicas de Exchange Online. Por ejemplo, puede restringir la búsqueda para buscar solo en el buzón del asunto de los datos y en la cuenta de OneDrive y los sitios de SharePoint seleccionados. Si decide buscar sitios específicos, tendrá que agregar cada uno de los sitios que quiera buscar.
  
Para modificar las ubicaciones de contenido para buscar:
  
1. Abra la búsqueda integrada para las que quiera cambiar las ubicaciones de contenido.

2. En la consulta de búsqueda, en **Ubicaciones**, haga clic en **Modificar** junto a la opción **Ubicaciones específicas**. 

    ![Haga clic en Modificar para cambiar las ubicaciones de contenido de la consulta de búsqueda integrada.](../media/d66f7ba7-b71f-4ff5-a030-460ff02e3123.png)
  
    Se muestra la página desplegable **Modificar ubicaciones**. A continuación se ofrece una descripción de las ubicaciones de contenido de la búsqueda integrada e información sobre cómo modificar las ubicaciones en las que se buscan. 

    ![Modificar la página desplegable de ubicaciones.](../media/56c033f6-6735-46ba-abb2-a263a2b79836.png)
  
    a. El botón de alternancia en **Seleccionar todos** de la sección del buzón en la parte superior de la página desplegable está seleccionado, lo que indica que se buscan todos los buzones. Para restringir el ámbito de la búsqueda, haga clic en el botón de alternancia para anular la selección y, después, haga clic en **Elegir usuarios, grupos o equipos** y elija buzones específicos para buscar.

    b. El botón de alternancia en **Seleccionar todos** en la sección del sitio en la mitad de la página desplegable está seleccionado, lo que indica que se buscan todos los sitios. Para limitar la búsqueda a sitios seleccionados, anule la selección del botón de alternancia y, a continuación, haga clic en **Seleccionar sitios**. Tiene que agregar cada sitio específico que quiera buscar, incluida la cuenta del asunto de los datos de OneDrive.

    c. El botón de alternancia en la sección de carpetas públicas de Exchange está seleccionado, lo que significa que se buscan todas las carpetas públicas de Exchange. Solo puede buscar todas las carpetas públicas de Exchange o ninguna de ellas. No puede elegir búsquedas específicas.

3. Si modifica las ubicaciones de contenido en la búsqueda integrada, haga clic en **Guardar &amp; ejecutar** para reiniciar la búsqueda. 

> [!NOTE]
> Cuando busque en todas las ubicaciones del buzón o solo en buzones específicos, los datos de otras aplicaciones de Office 365 guardados en los buzones de usuario se incluirán en la exportación de resultados de la búsqueda. Estos datos no se incluyen en los resultados de búsqueda estimados y no aparecen en la vista previa. Pero se incluye cuando exporten y descarguen los resultados de búsqueda. Para obtener más información sobre las aplicaciones que almacenan datos en el buzón de un usuario, consulte [Contenido almacenado en buzones de Exchange Online](/microsoft-365/compliance/what-is-stored-in-exo-mailbox).
  
## <a name="more-information-about-using-the-dsr-case-tool"></a>Más información acerca del uso de la herramienta de casos de DSR

Las secciones siguientes contienen más información sobre el uso de la herramienta de casos de DSR para responder a las solicitudes de exportación de DSR.
  
[Exportar datos desde el Servicio de roaming de Office](#exporting-data-from-the-office-roaming-service)

[Exportar elementos indexados parcialmente](#exporting-partially-indexed-items)

[Buscar y exportar datos desde Microsoft Teams y grupos de Microsoft 365](#searching-and-exporting-data-from-microsoft-teams-and-microsoft-365-groups)

[Buscar carpetas públicas de Exchange](#searching-exchange-public-folders)
  
### <a name="exporting-data-from-the-office-roaming-service"></a>Exportar datos desde el Servicio de roaming de Office

Puede usar la herramienta de casos de DSR para buscar y exportar datos de uso generados por el Servicio de roaming de Office. Roaming es un servicio que almacena la configuración relacionada con Office como el tema de Office, el diccionario personalizado, la configuración del idioma, el modo de programador y la autocorrección.

Los datos del Servicio de roaming de Office se almacenan en el buzón de un asunto de datos en una carpeta oculta ubicada en un subárbol de mensajes no deseados (que no sea IPM) de buzones de Exchange Online. Esto significa que los datos están ocultos de la vista del usuario cuando usan Outlook u otros clientes de correo para acceder al buzón. Para obtener más información sobre las carpetas ocultas, vea [Carpetas ocultas de MAPI](https://go.microsoft.com/fwlink/?linkid=872758).
  
Puede crear una búsqueda de contenido independiente (y asociarla a un caso de DSR) que devuelva los datos de uso del Servicio de roaming de Office en el buzón del asunto de los datos. Estos datos no se incluyen en las estadísticas de búsqueda y no estarán disponibles para su vista previa. Pero puede exportarlos y, después, entregarlos al destinatario en respuesta a una solicitud de exportación de DSR.
  
Al exportar datos desde el Servicio de roaming de Office, los datos se guardan en una carpeta independiente que se encuentra en la carpeta **ApplicationDataRoot**, que está en una carpeta que tiene el nombre con la dirección de correo electrónico del asunto de los datos. Estos datos se exportan como archivos JSON, que son archivos de texto de lectura humana similares a archivos XML o TXT, que se adjuntan a mensajes de correo electrónico. Actualmente, esta carpeta se denomina con el identificador único global (GUID): **1caee58f-ab14-4a6b-9339-1fe2ddf6692b**. En futuras versiones de la herramienta de casos de DSR, el GUID se reemplazará por el nombre de la aplicación real. 

**Para buscar y exportar datos del Servicio de roaming de Office**:
  
1. En el Centro de cumplimiento de Microsoft 365, haga clic en **Solicitudes de los interesados** y, después, haga clic en **Abrir caso** al lado del caso de DSR para el interesado para el que quiere exportar los datos de uso. 

2. Haga clic en la pestaña **Buscar** en la parte superior de la página y, después, haga clic en ![el icono Agregar.](../media/ITPro-EAC-AddIcon.gif) **Búsqueda guiada**.

3. Haga clic en **Cancelar** en la página **Nombre de la búsqueda**. 

4. En **Consulta de búsqueda**, en la condición **Tipo**, seleccione la casilla junto a **Servicio de roaming de Office**. 

    ![Seleccione la casilla del Servicio de roaming de Office para exportar datos de uso.](../media/O365_DSRCase_SDSDataExport1.png)
  
    La condición **Tipo** (que son clases de mensajes de correo electrónico) debería ser el único elemento de la consulta de la búsqueda. Puede eliminar el cuadro de **Palabras clave** o dejarlo en blanco. 

5. En **Ubicación**, asegúrese de que **Ubicaciones específicas** está seleccionado y, después, haga clic en **Modificar**.

6. En la parte superior de la página desplegable **Modificar ubicaciones** (la sección buzón), haga clic en **Elegir usuarios, grupos o equipos**.

7. En la página **Editar ubicaciones**, haga clic en **Elegir usuarios, grupos o equipos**, elija el buzón del asunto de los datos y, después, guarde la selección. 

8. Haga clic en **Guardar y ejecutar** y, después, asigne un nombre a la búsqueda y guárdela.

    La búsqueda se ha iniciado.

 **Para exportar datos del Servicio de roaming de Office**:
  
1. Cuando la búsqueda que ha creado en el paso anterior esté completa, haga clic en la pestaña **Buscar** en la parte superior de la página y, después, haga clic en la casilla situada junto a la búsqueda. Es posible que tenga que hacer clic en ![Actualizar. ](../media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) **Actualizar** para mostrar la búsqueda.

2. En la página del control flotante, haga clic en **Exportar resultados**.

3. En la página **Opciones de exportación**, seleccione las siguientes opciones recomendadas para la exportación de datos de uso. 

    ![Opciones de exportación al exportar datos de uso del Servicio de roaming de Office.](../media/470a7d1e-eeae-4b42-95aa-15cb82ce2f68.png)
  
    a. En **Opciones de salida**, seleccione la primera opción (**Todos los elementos, excluidos los que tienen un formato no reconocido, están cifrados o no se han indexado por otras razones**) para exportar solo elementos indizados.

    b. En **Exportar contenido de Exchange como**, seleccione la segunda opción: **Un archivo PST que contenga todos los mensajes**.

    c. Deje las opciones de exportación restantes sin seleccionar.

4. Después de elegir la configuración de exportación, haga clic en **Exportar**.

    Los resultados de búsqueda se preparan para su descarga, lo que significa que se están cargando en el área de almacenamiento de Azure en la nube de Microsoft. Los pasos siguientes muestran cómo descargar estos datos en el equipo local.

5. Haga clic en la pestaña **Exportar** para mostrar el trabajo de exportación que creó. Los trabajos de exportación tienen el mismo nombre que la búsqueda correspondiente con **_Export** anexado al final del nombre de la búsqueda. 

6. Haga clic en el trabajo de exportación que acaba de crear para mostrar la página desplegable de exportación. 

7. En **Clave de exportación**, haga clic en **Copiar al Portapapeles**. Usará esta clave para descargar los resultados de la búsqueda en el paso 10.

8. Haga clic en el ![icono Exportar resultados de búsqueda.](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Descargar** resultados en la parte superior de la página desplegable de exportación. 

9. En la ventana emergente de la parte inferior de la página, haga clic en **Abrir** para abrir la **Herramienta de exportación de eDiscovery**. La **Herramienta de exportación de eDiscovery** se instalará la primera vez que descargue los resultados de búsqueda. 

10. En la **Herramienta de exportación de eDiscovery**, pegue la clave de exportación que ha copiado en el paso 7 en el cuadro correspondiente.

11. Haga clic en **Examinar** para especificar la ubicación en la que desea descargar los archivos de los resultados de la búsqueda. 

    > [!NOTE]
    > Debido a la gran cantidad de actividad de disco (lecturas y escrituras), debe descargar los resultados de búsqueda en una unidad de disco local; no las descargue en una unidad de red asignada o en otra ubicación de red. 
  
12. Haga clic en **Iniciar** para descargar los resultados de la búsqueda en el equipo. 

    La **Herramienta de exportación de exhibición de documentos electrónicos** muestra información del estado acerca del proceso de exportación, incluida una estimación del número (y tamaño) de los elementos restantes que se van a descargar. Una vez completado el proceso de exportación, puede abrir el archivo PST de Exchange en Outlook y, después, ir a la carpeta **ApplicationDataRoot** para obtener acceso a la subcarpeta del Servicio de roaming. 

    Como se ha explicado anteriormente, los archivos JSON que contienen datos de uso se adjuntan a mensajes. Para ver un archivo JSON, haga clic en un mensaje y, después, abra el archivo JSON adjunto.
  
### <a name="exporting-partially-indexed-items"></a>Investigación de elementos indexados parcialmente

Le recomendamos que no exporte elementos indizados parcialmente (también denominados elementos no indizados) de la búsqueda integrada que se crea al crear un caso de DSR. Esto se debe a que los resultados de búsqueda probablemente incluirán elementos parcialmente indizados para otros usuarios de la organización y no solo elementos parcialmente indizados para el interesado). En su lugar, le recomendamos que cree una Búsqueda de contenido independiente que esté asociada al caso de DSR que esté diseñada para exportar solo los elementos indexados parcialmente relacionados con el interesado.
  
Este es un proceso de alto nivel para exportar elementos parcialmente indexados. Después de exportarlos, puede revisarlos para determinar si un elemento responde a una solicitud de acceso o exportación de DSR.
  
1. Abra el caso de DSR y cree una búsqueda en la página de **Búsqueda**.

2. Use los siguientes criterios para configurar la consulta de búsqueda y las ubicaciones de contenido para buscar:

    - Use una consulta de palabra clave vacía o en blanco. Esto devuelve todos los elementos en las ubicaciones de contenido que se buscan.

    - Busque solo en el buzón de Exchange Online del asunto de los datos y en su cuenta de OneDrive.

3. Después de ejecutar la búsqueda y completarla, puede exportar y descargar los resultados de búsqueda (como se describe en [Paso 4](#step-4-export-the-data)). Use la siguiente configuración para exportar elementos indizados parcialmente.

    - En **Opciones de salida**, seleccione la tercera opción (**Solo los elementos que tienen un formato no reconocido, están cifrados o no se han indexado por otras razones**) para exportar solo elementos indizados parcialmente.

    - En **Exportar contenido de Exchange como**, puede seleccionar cualquier opción según sus preferencias.

    - Seleccionar la opción **Incluir versiones para los documentos de SharePoint** exporta versiones de los documentos si una versión está parcialmente indexada.

Para obtener más información acerca de los elementos parcialmente indizados, vea:
  
- [Elementos parcialmente indexados en la Búsqueda de contenido](/microsoft-365/compliance/partially-indexed-items-in-content-search)

- [Exportar elementos indexados parcialmente](/microsoft-365/compliance/export-search-results#exporting-partially-indexed-items)

### <a name="searching-and-exporting-data-from-microsoft-teams-and-microsoft-365-groups"></a>Buscar y exportar datos desde Microsoft Teams y grupos de Microsoft 365

Las conversaciones que forman parte de la lista de chat en Microsoft Teams (denominadas chats de Teams o chats uno a uno) se almacenan en el buzón de Exchange Online de los usuarios que participan en los chats. Además, los archivos que un usuario comparte en un chat uno a uno se almacenan en la cuenta de OneDrive de la persona que comparte el archivo. Dado que la búsqueda integrada busca en todos los buzones y cuentas de OneDrive de la organización, los chats de equipo y los documentos compartidos en una sesión de chat (que el asunto de los datos ha creado o cargado) se devuelven mediante la búsqueda integrada en un caso de DSR.
  
Como alternativa, las conversaciones de un canal de Teams (también denominadas mensajes de canal) se almacenan en el buzón de correo asociado a un equipo. Estos tipos de conversaciones en las que el interesado participó también son devueltos por la búsqueda integrada, ya que se buscan todos los buzones asociados con Teams. Además, los archivos que un interesado comparte en un canal de Teams se almacenan en el sitio de SharePoint del equipo. Los archivos creados o cargados por el interesado son devueltos por la búsqueda integrada en un caso de DSR porque los sitios asociados con Teams se incluyen en la búsqueda.
  
De forma similar, en la búsqueda integrada también se incluyen los buzones y sitios de SharePoint que se correspondan con un grupo de Microsoft 365. Esto significa que los mensajes de correo electrónico enviados o recibidos por el interesado y los archivos creados o cargados por el interesado se devuelven. 
  
Para obtener más información sobre el uso de la búsqueda de contenido para buscar elementos en Microsoft Teams y grupos de Microsoft 365, o para ver cómo obtener una lista de miembros, consulte la sección "Búsqueda de Microsoft Teams y grupos de Microsoft 365" en [Búsqueda de contenido en Microsoft 365](/microsoft-365/compliance/content-search-reference#searching-microsoft-teams-and-microsoft-365-groups).
  
### <a name="searching-exchange-public-folders"></a>Carpetas públicas de Exchange

La búsqueda integrada en un caso de DSR solo devolverá los mensajes de correo electrónico en los que el asunto de los datos se envió a una carpeta pública habilitada para correo o mensajes que otro usuario envió a una carpeta pública y que también copió el destinatario. No devuelve los mensajes que el destinatario publicó en una carpeta pública. Para buscar elementos que el destinatario ha publicado en una carpeta pública, puede crear una búsqueda de contenido independiente que busque todos los elementos publicados en una carpeta pública por el destinatario.
  
Aquí tiene un proceso de alto nivel para buscar elementos que el destinatario publicó en una carpeta pública. 
  
1. Abra el caso de DSR y cree una búsqueda en la página de **Búsqueda**. 

2. Use los siguientes criterios para configurar la consulta de búsqueda y las ubicaciones de contenido para buscar:

   - En el cuadro **Palabras clave**, utilice la siguiente consulta de búsqueda: 

     ```powershell
     itemclass:ipm.post AND "<email address of the data subject>"
     ```

   - Buscar todas las carpetas públicas

   - Después de ejecutar la búsqueda y completarla, puede exportar y descargar los resultados de búsqueda (como se describe en [Paso 4](#step-4-export-the-data)). Use la siguiente configuración para exportar elementos indizados parcialmente.
