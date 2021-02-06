---
title: Administrar solicitudes de interesados del RGPD con la herramienta de casoSR en el Centro de & cumplimiento
description: Obtenga información sobre cómo administrar las solicitudes de interesados del Reglamento general de protección de datos (RGPD) de la UE con la herramienta de casos de DSR.
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- SPO_Content
- MS-Compliance
ms.assetid: ce9eb942-3589-42cb-88fd-1576ecb09c5c
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 67aadb6e9ccda3a84a06b39570c680c8b30ce775
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121499"
---
# <a name="manage-gdpr-data-subject-requests-with-the-dsr-case-tool-in-the-security--compliance-center"></a>Administrar solicitudes de interesados del RGPD con la herramienta de casos DSR en el Centro de & cumplimiento

El Reglamento General de Protección de Datos (RGPD) de la UE trata de proteger y habilitar los derechos de privacidad de las personas dentro de la Unión Europea (UE). El RGPD concede a las personas de la Unión Europea (conocidas como interesados) el derecho de acceder, recuperar, corregir, borrar y restringir el procesamiento de sus datos personales. Según el RGPD, los datos personales se refieren a cualquier información relacionada con una persona física identificada o identificable. Una solicitud formal de una persona a su organización para realizar una acción sobre sus datos personales se denomina solicitud de interesado o DSR. Para obtener información detallada acerca de cómo responder a solicitudes de interesado de datos en Office 365, vea la Guía de solicitudes del interesado [de Office 365.](https://go.microsoft.com/fwlink/?linkid=871169 )
  
Para administrar investigaciones en respuesta a una solicitud de DSR enviada por una persona de su organización, puede usar la herramienta de casoSR en el Centro de seguridad & Cumplimiento para encontrar contenido almacenado en:
  
- Cualquier buzón de usuario de la organización. Esto incluye conversaciones de Skype Empresarial y chats uno a uno en Microsoft Teams
    
- Todos los buzones asociados a un grupo de Microsoft 365 y todos los buzones de equipo en Microsoft Teams
    
- Todos los sitios de SharePoint Online y OneDrive para la Empresa de la organización
    
- Todos los sitios de Teams y los sitios de grupo de Microsoft 365 de su organización
    
- Todas las carpetas públicas de Exchange Online
    
Con la herramienta de casos de DSR puede:
  
- Crear un caso independiente para cada investigación de DSR.
    
- Controlar quién tiene acceso al caso de DSR agregando personas como miembros del caso; solo los miembros pueden tener acceso al caso y solo pueden ver sus casos en la lista de casos en la página de casos de **DSR** en el Centro de seguridad & cumplimiento. Además, puede asignar permisos diferentes a diferentes miembros del mismo caso. Por ejemplo, puede permitir que algunos miembros solo puedan ver el caso y los resultados de la búsqueda, y permitir que otros miembros creen búsquedas y exportan los resultados de la búsqueda. 
    
- Use la búsqueda integrada para buscar todo el contenido creado o cargado por un interesado específico.
    
- Opcionalmente, revise la consulta de búsqueda integrada y vuelva a ejecutar la búsqueda para restringir los resultados de la búsqueda.
    
- Agregue otras búsquedas de contenido asociadas con el caso DSR. Esto incluye la creación de búsquedas que devuelven elementos parcialmente indizados y registros generados por el sistema desde el servicio de itinerancia de Office.
    
- Exportar datos en respuesta a una solicitud de acceso o exportación de DSR.
    
- Elimine los casos cuando se complete el proceso de investigación de DSR. Esto quita todas las búsquedas y los trabajos de exportación asociados con el caso.
    
Este es el proceso de alto nivel para usar la herramienta de casos de DSR para administrar investigaciones de DSR:
  
[Step 1: Assign eDiscovery permissions to potential case members](#step-1-assign-ediscovery-permissions-to-potential-case-members)

[Paso 2: Crear un caso de DSR y agregar miembros](#step-2-create-a-dsr-case-and-add-members)

[Paso 3: Ejecutar la consulta de búsqueda](#step-3-run-the-search-query)

[Paso 4: Exportar los datos](#step-4-export-the-data)

[(Opcional) Paso 5: Revisar la consulta de búsqueda integrada](#optional-step-5-revise-the-built-in-search-query)

[Más información sobre el uso de la herramienta de casos de DSR](#more-information-about-using-the-dsr-case-tool)
  
> [!IMPORTANT]
> Nuestras herramientas pueden ayudar a los administradores a realizar solicitudes de acceso o exportación de DSR al permitirles usar la funcionalidad integrada de búsqueda y exportación que se encuentra en la herramienta de casos de DSR. La herramienta ayuda a facilitar un método de mejor esfuerzo para exportar datos relevantes para una solicitud de DSR enviada por un interesado. Sin embargo, es importante tener en cuenta que los resultados de la búsqueda pueden variar en función del interesado o de las acciones de administración tomadas que pueden afectar a si un elemento se considera o no como "datos personales" con fines de exportación. Por ejemplo, si el interesado fue la última persona en modificar un archivo que no crearon, es posible que el archivo no se devuelva en los resultados de la búsqueda. De forma similar, un administrador podría exportar datos sin incluir elementos parcialmente indizados o todas las versiones de documentos de SharePoint. Por lo tanto, las herramientas proporcionadas pueden ayudar a facilitar el acceso y la exportación de solicitudes de datos; sin embargo, los resultados están sujetos a escenarios de uso específicos de administradores y interesados. 
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a>Paso 1: Asignar permisos de exhibición de documentos electrónicos a posibles miembros del caso

De forma predeterminada, un administrador global puede obtener acceso a la herramienta de caso de DSR en el Centro de seguridad & cumplimiento. Por diseño, otros usuarios como un responsable de la privacidad de datos, un administrador de recursos humanos u otras personas involucradas en investigaciones de DSR no tienen acceso a la herramienta de caso de DSR y tendrán que tener asignados los permisos adecuados para acceder a la herramienta. La forma más sencilla de hacerlo  es ir a la página Permisos en el Centro de seguridad y cumplimiento de & y agregar usuarios al grupo de roles administrador de exhibición de documentos electrónicos. También tiene que asignar estos permisos para poder agregarlos como miembros del caso de DSR que cree en el paso 2. 
  
Para obtener instrucciones paso a paso, vea Asignar permisos de exhibición de documentos electrónicos en el Centro de seguridad & [cumplimiento de Office 365.](/microsoft-365/compliance/assign-ediscovery-permissions)
  
> [!NOTE]
> De forma predeterminada, un administrador global (u otros miembros del grupo de roles Administración de la organización en el Centro de seguridad y cumplimiento de & no tiene los permisos necesarios para exportar los resultados de búsqueda de contenido (vea el paso 4 de este artículo). Para solucionar esto, un administrador puede agregarse a sí mismo como miembro del grupo de roles administrador de exhibición de documentos electrónicos. 
  
## <a name="step-2-create-a-dsr-case-and-add-members"></a>Paso 2: Crear un caso de DSR y agregar miembros

El siguiente paso es crear un caso de DSR. Al crear un caso, puede elegir iniciar la búsqueda integrada o puede crear el caso sin iniciar la búsqueda. El siguiente procedimiento le indica que cree el caso sin iniciar la búsqueda y, a continuación, le muestre cómo agregar miembros al caso.
  
1. Vaya e [https://protection.office.com](https://protection.office.com) inicie sesión con su cuenta de trabajo o escuela. 
    
2. En el Centro de seguridad &  cumplimiento, haga clic en Solicitudes del interesado de privacidad de datos y, a continuación, haga clic en Agregar icono \> nuevo caso de solicitud ![ de ](../media/ITPro-EAC-AddIcon.gif) **interesado.**
    
3. En la **página desplegable Nuevo caso de DSR,** asigne un nombre al caso, escriba una descripción opcional y, a continuación, haga clic en **Siguiente**. El nombre del caso debe ser exclusivo en la organización.
    
    > [!TIP]
    > Considere la posibilidad de agregar el nombre de la persona que envió la solicitud de DSR que está investigando en el nombre o la descripción del nuevo caso. Tenga en cuenta que solo los miembros de este caso (y los administradores de exhibición de documentos electrónicos) podrán ver el caso en la lista de **casos** en la página Solicitudes del interesado. 
  
4. En la **página** Detalles de la solicitud, en Interesado (la persona que presentó esta **solicitud),** seleccione la persona a la que desea buscar y exportar datos y, a continuación, haga clic en **Siguiente**.
    
5. En la **página Confirmar la configuración del** caso, puede cambiar el nombre y la descripción del caso y seleccionar otro interesado. De lo contrario, haga clic **en Guardar**.
    
    Se muestra una página que confirma que se ha creado el nuevo caso de DSR.
    
    ![Iniciar la búsqueda o cerrar la página nuevo caso de DSR](../media/b5e62c2c-cafe-4a8d-a38c-789ed9f9ccbd.png)
  
    En este punto, puede hacer una de estas dos cosas:
    
    a. Al **hacer clic en Mostrarme resultados de búsqueda,** se inicia la búsqueda. Ésa es la selección predeterminada. La búsqueda integrada que se ejecuta cuando selecciona esta opción y los resultados que se devuelven se de abordan en el paso 3.
    
    b. Al **hacer clic** en Finalizar, se cierra el nuevo caso de DSR sin iniciar la búsqueda integrada. Al seleccionar esta opción, el nuevo caso DSR se muestra en la **página Solicitudes del interesado.**
    
6. Haga **clic** en Finalizar para poder ir al nuevo caso de DSR y agregarle miembros. 
    
7. En la **página Solicitudes del interesado,** haga clic en el nombre del caso DSR que creó. 
    
8. En la **página desplegable Administrar este caso,** en Administrar **miembros,** haga clic **en Agregar**. 
    
    En **Usuarios,** se muestra una lista de las personas a las que se asignan los permisos de exhibición de documentos electrónicos adecuados. Las personas a las que asignó permisos de exhibición de documentos electrónicos en el paso 1 se mostrarán en esta lista. 
    
9. Seleccione las personas que desea agregar como miembros del caso DSR, haga clic en **Agregar** y, a continuación, guarde los cambios.
    
    También puede agregar grupos de roles como miembros del caso DSR haciendo clic en Agregar **en** Administrar grupos **de roles.** 
    
## <a name="step-3-run-the-search-query"></a>Paso 3: Ejecutar la consulta de búsqueda

Después de crear un caso de DSR y agregar miembros, el siguiente paso es ejecutar la búsqueda integrada asociada con el caso. Esta consulta de búsqueda predeterminada hace lo siguiente:
  
- Busca en todos los buzones de la organización todos los elementos de correo electrónico enviados o recibidos por el interesado. Esto se logra mediante el uso de la propiedad de correo electrónico  *Participantes,*  que busca el interesado en todos los campos de personas de un mensaje de correo electrónico. Esta propiedad devuelve elementos en los que el interesado está en los campos **De**, **Para**, **CC** y **CCO.** Las carpetas públicas en Exchange Online también se buscan mensajes enviados o recibidos por el interesado. 
    
- Busca documentos y elementos creados o cargados por el interesado en todos los sitios de la organización. Esto se logra mediante las siguientes propiedades de sitio:
    
  - La  *propiedad Author*  devuelve elementos en los que el interesado aparece en el campo autor de los documentos de Office. Este valor persiste, incluso si otra persona copia y carga el documento. 
    
  - La  *propiedad CreatedBy*  devuelve los elementos creados o cargados por el interesado. 
    
Este es el aspecto de la consulta de palabras clave para la búsqueda integrada que se crea automáticamente al crear un caso de solicitud de interesado.
  
```powershell
participants:"<email address>" OR author:"<display name>" OR createdby:"<display name>"
```

Por ejemplo, si el nombre del interesado es Ina Quete, la consulta de palabra clave tendría este aspecto:
  
```powershell
participants:"ina@contoso.com" OR author:"Ina Leonte" OR createdby:"Ina Leonte"
```

 **Para ejecutar la búsqueda integrada de un caso de DSR:**
  
1. En el Centro de seguridad  & cumplimiento, haga clic en Solicitudes del interesado de privacidad de datos y, a continuación, haga clic en Abrir junto al caso de DSR que creó en el \> paso 2.  
    
    Haga clic **en la** pestaña Buscar en la parte superior de la página y, a continuación, haga clic en la casilla situada junto a la búsqueda integrada que se creó al crear el caso de DSR. La búsqueda tiene el mismo nombre que el caso DSR. 
    
2. En la página desplegable de búsqueda, haga clic **en Abrir consulta.**
    
    Al abrir la consulta, la búsqueda se inicia y se completará en unos instantes. 
    
3. Una vez completada la búsqueda, haga clic en **Vista previa de los resultados** para obtener una vista previa de los resultados de la búsqueda. Para obtener más información, vea [Vista previa de los resultados de la búsqueda.](/microsoft-365/compliance/content-search#preview-search-results)
    
    > [!TIP]
    > También puede ver las estadísticas de consulta de búsqueda para ver el número de elementos de buzones y sitios que devuelve la búsqueda y las ubicaciones de contenido superiores que contienen elementos que coinciden con la consulta de búsqueda. Para obtener más información, vea [Ver información y estadísticas sobre una búsqueda.](/microsoft-365/compliance/content-search#view-information-and-statistics-about-a-search) 
  
Puede editar la consulta de búsqueda integrada, cambiar las ubicaciones de contenido que se buscan y, a continuación, volver a ejecutar la búsqueda. Vea [el paso 5](#optional-step-5-revise-the-built-in-search-query) para obtener más información. 
  
## <a name="step-4-export-the-data"></a>Paso 4: Exportar los datos

Después de ejecutar la búsqueda integrada, puede exportar los resultados de la búsqueda. Como alternativa, antes de exportar los datos, es posible que desee revisar la consulta para reducir el número de resultados de búsqueda. Vea el paso 5 para obtener más información sobre cómo restringir los resultados de la búsqueda.
  
Al exportar los resultados de la búsqueda, los elementos del buzón se pueden descargar en archivos PST o como mensajes individuales. Al exportar contenido de cuentas de SharePoint y OneDrive, se exportan copias de documentos nativos de Office y otros documentos. Se incluye un archivo de resultados que contiene información sobre cada elemento exportado con los resultados de la búsqueda. Para obtener información más detallada acerca de la exportación, vea [Exportar resultados de búsqueda de contenido.](/microsoft-365/compliance/export-search-results)
  
> [!NOTE]
> De forma predeterminada, un administrador global (u otros miembros del grupo de roles administración de la organización en el Centro de seguridad & cumplimiento) no tiene los permisos necesarios para exportar los resultados de la búsqueda de contenido. Para solucionar esto, un administrador puede agregarse a sí mismo como miembro del grupo de roles administrador de exhibición de documentos electrónicos. 
  
El equipo que use para exportar datos debe cumplir los siguientes requisitos del sistema:
  
- Versiones de 32 o 64 bits de Windows 7 y versiones posteriores
    
- Microsoft .NET Framework 4.7
    
- Un explorador compatible:
    
  - Microsoft Edge
    
    O bien
    
  - Microsoft Internet Explorer 10 y versiones posteriores
    
    > [!NOTE]
    > Microsoft no fabrica extensiones ni complementos de terceros para ClickOnce aplicaciones. No se admite la exportación de datos mediante un explorador no compatible con extensiones o complementos de terceros. 
  
 **Para exportar datos de la búsqueda integrada en un caso de DSR:**
  
1. En el Centro de seguridad &  cumplimiento, haga clic en Solicitudes del interesado de privacidad de datos y, a continuación, haga clic en Abrir junto al caso \> de DSR desde el que desea exportar  datos. 
    
2. Haga clic **en la** pestaña Buscar en la parte superior de la página y, a continuación, haga clic en la casilla situada junto a la búsqueda integrada que se creó al crear el caso de DSR. O haga clic en otra búsqueda para exportar datos de esa búsqueda. 
    
3. En la página desplegable de búsqueda, haga clic en el icono Exportar resultados de búsqueda Más y, a continuación, seleccione Exportar resultados ![ de la lista ](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) desplegable.  
    
4. En la **página Exportar resultados,** seleccione las siguientes opciones recomendadas para las solicitudes de exportación de DSR. 
    
    ![Configurar las opciones de exportación](../media/25416b79-57da-46a1-ae07-e640602a8fa4.png)
  
    a. En Opciones de salida, seleccione la primera opción (Todos los elementos, excepto los que tienen uno que tiene un formato no reconocido, están **cifrados** o no se indexaron por otros motivos) para exportar solo elementos indizados. La razón por la que no desea exportar elementos parcialmente indizados de la búsqueda integrada es porque también se exportarán elementos parcialmente indizados de otros usuarios. Para exportar solo los elementos parcialmente indizados para el interesado, se recomienda crear una búsqueda independiente. Para obtener más información, vea Exportar elementos parcialmente [indizados](#exporting-partially-indexed-items) en la sección "Más información sobre el uso de la herramienta de casos de DSR".
    
    b. En **Exportar contenido de Exchange como**, seleccione la tercera opción, un archivo PST que contiene todos los mensajes en una sola **carpeta.** Dado que algunos de los resultados pueden ser para elementos que se originaron en el buzón de otro usuario, esta opción solo muestra el elemento en una sola carpeta sin indicar el buzón real y es la mejor opción que se puede usar al desduplicar los resultados como se recomienda en el siguiente elemento. Esta opción también permite al interesado revisar los elementos en orden cronológico (los elementos se ordenan por fecha de envío) sin tener que navegar por la estructura de carpetas de buzón original de cada elemento.
    
    c. Seleccione **la opción Habilitar desduplicación** para excluir los mensajes de correo electrónico duplicados. Se recomienda esta opción porque la búsqueda integrada busca en todos los buzones de la organización. Por lo tanto, si se encuentran varias copias del mismo mensaje en los buzones en los que se ha buscado, esta opción significa que solo se exportará una copia de un mensaje. Esta opción, juntos exportará mensajes en un archivo PST en una sola carpeta, lo que da como resultado la mejor experiencia de usuario para solicitudes de exportación de DSR. El Results.csv de exportación enumera todas las ubicaciones donde se encontraron mensajes duplicados.
    
    Opcionalmente, puede seleccionar la opción Incluir versiones para documentos de **SharePoint** para exportar todas las versiones de documentos de SharePoint y OneDrive. Esto requiere que el control de versiones esté activado para las bibliotecas de documentos. Esta opción ayuda a garantizar que se exportan todos los datos relevantes.
    
5. Después de elegir la configuración de exportación, haga clic **en Exportar**.
    
    Los resultados de la búsqueda están preparados para su descarga, lo que significa que se cargan en el área de Azure Storage para su organización en la nube de Microsoft. Los pasos siguientes muestran cómo descargar estos datos en el equipo local.
    
6. Haga clic **en la pestaña** Exportar para mostrar el trabajo de exportación que ha creado. Los trabajos de exportación tienen el mismo nombre que la búsqueda correspondiente **con _Export** al final del nombre de búsqueda. 
    
7. Haga clic en el trabajo de exportación que acaba de crear para mostrar la página desplegable de exportación. Esta página muestra información sobre la búsqueda, como el tamaño y el número total de elementos que se exportarán y el porcentaje de los elementos que se han transferido a un área de almacenamiento de Azure. Haga **clic en Actualizar** para actualizar la información de estado de carga. 
    
8. En **Clave de exportación**, haga clic en **Copiar al Portapapeles**. Use esta clave en el paso 11 para descargar los resultados de la búsqueda.
    
9. Haga ![ clic en exportar el icono de resultados de búsqueda ](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Descargar** resultados en la parte superior de la página desplegable de exportación. 
    
10. En la ventana emergente en la parte inferior de la página, haga clic en Abrir **para** abrir la herramienta de exportación **de exhibición de documentos electrónicos.** La **herramienta de exportación de** exhibición de documentos electrónicos se instalará la primera vez que descargue los resultados de la búsqueda. 
    
11. En la **herramienta de exportación de** exhibición de documentos electrónicos, pegue la clave de exportación que copió en el paso 8 en el cuadro correspondiente.
    
12. Haga clic en **Examinar** para especificar la ubicación en la que desea descargar los archivos de los resultados de la búsqueda. 
    
    > [!NOTE]
    > Debido a la gran cantidad de actividad de disco (lecturas y escrituras), debes descargar los resultados de la búsqueda en una unidad de disco local; no los descargue en una unidad de red asignada u otra ubicación de red. 
  
13. Haga clic en **Iniciar** para descargar los resultados de la búsqueda en el equipo. 
    
    La **Herramienta de exportación de exhibición de documentos electrónicos** muestra información del estado acerca del proceso de exportación, incluida una estimación del número (y tamaño) de los elementos restantes que se van a descargar. Una vez completado el proceso de exportación, puede obtener acceso a los archivos en la ubicación donde se descargaron. Para obtener más información acerca de los informes que [](/microsoft-365/compliance/export-search-results#more-information) se incluyen al descargar los resultados de búsqueda de contenido, vea la sección Más información en "Exportar resultados de búsqueda de contenido". 
    
Después de exportar los datos, los resultados de la búsqueda y los informes de exportación se encuentran en una carpeta que tiene el mismo nombre que el caso DSR. Los archivos PST que contienen elementos de buzón se encuentran en una subcarpeta denominada **Exchange**. Los documentos y otros elementos de los sitios se encuentran en una subcarpeta denominada **SharePoint**. 
  
## <a name="optional-step-5-revise-the-built-in-search-query"></a>(Opcional) Paso 5: Revisar la consulta de búsqueda integrada

Después de ejecutar la búsqueda integrada, puede revisarla para restringir el ámbito y devolver menos resultados de búsqueda. Para ello, agregue condiciones a la consulta. Una condición está conectada lógicamente a la consulta de palabras clave por el **operador AND.** Esto significa que se devolverán en los resultados de la búsqueda, los elementos deben satisfacer tanto la consulta de palabras clave como las condiciones que agregue. Así es como las condiciones ayudan a restringir los resultados. Si agrega dos o más condiciones únicas a una consulta de búsqueda (condiciones que especifican propiedades diferentes), esas condiciones están conectadas lógicamente por el **operador AND.** Esto significa que solo se devuelven los elementos que cumplen todas las condiciones (además de la consulta de palabra clave). Si agrega varios valores (separados por comas o punto y coma) a una sola condición, dichos valores se conectan mediante el **operador OR.** Eso significa que se devuelven los elementos que contengan cualquiera de los valores especificados para la propiedad en la condición. 
  
Estos son algunos ejemplos de las condiciones que puede agregar a la consulta de búsqueda integrada de un caso de DSR. El nombre de la propiedad real usada en una consulta de búsqueda se muestra entre paréntesis.
  
- **Tipo de archivo ( `filetype` ):** especifica la extensión de un documento o archivo. Use esta condición para buscar documentos y archivos creados por aplicaciones específicas de Office, como Word, Excel y OneNote. 
    
- **Tipo de mensaje ( `kind` ):** especifica el tipo de elemento de correo electrónico que se debe buscar. Por ejemplo, puede usar la sintaxis para devolver solo mensajes de correo electrónico y conversaciones de Skype Empresarial o chats uno a  `kind:email OR kind:im` uno en Microsoft Teams. 
    
- **Etiqueta de cumplimiento ( `compliancetag` ):** especifica una etiqueta asignada a un mensaje de correo electrónico o un documento. Esta condición devuelve elementos clasificados con una etiqueta específica. Las etiquetas se usan para clasificar el correo electrónico y los documentos para el gobierno de datos y aplicar reglas de retención en función de la clasificación definida por la etiqueta. Esta condición es útil para las investigaciones de DSR porque su organización puede estar usando etiquetas para clasificar contenido relacionado con la privacidad de datos o que contiene datos personales o información confidencial. Para el valor de esta condición, use el nombre completo de la etiqueta o la primera parte del nombre de la etiqueta con un carácter comodín. Para obtener más información, vea Más información sobre las directivas de retención y las etiquetas de [retención en Office 365.](/microsoft-365/compliance/retention)
    
Para obtener una lista y una descripción de todas las [](/microsoft-365/compliance/keyword-queries-and-search-conditions#search-conditions) condiciones disponibles en la herramienta de casos de DSR, vea condiciones de búsqueda en el artículo "Consultas de palabras clave y condiciones de búsqueda para búsqueda de contenido". 
  
### <a name="changing-the-content-locations-that-are-searched"></a>Cambio de las ubicaciones de contenido que se buscan

Además de revisar la búsqueda integrada para un caso de DSR, también puede cambiar las ubicaciones de contenido que se buscan. Como se ha explicado anteriormente, la búsqueda integrada busca en todos los buzones y sitios de la organización, así como en las carpetas públicas de Exchange Online. Por ejemplo, puede restringir la búsqueda para que solo busque en el buzón del interesado, en la cuenta de OneDrive y en los sitios de SharePoint seleccionados. Si decide buscar sitios específicos, tiene que agregar cada sitio en el que desee buscar.
  
Para modificar las ubicaciones de contenido en las que se buscará:
  
1. Abra la búsqueda integrada para la que desea cambiar las ubicaciones de contenido.
    
2. En la consulta de búsqueda, en **Ubicaciones**, haga clic **en** Modificar junto a la **opción Ubicaciones** específicas. 
    
    ![Haga clic en Modificar para cambiar las ubicaciones de contenido de la consulta de búsqueda integrada](../media/d66f7ba7-b71f-4ff5-a030-460ff02e3123.png)
  
    Se **muestra la página** desplegable Modificar ubicaciones. Esta es una descripción de las ubicaciones de contenido en la búsqueda integrada y cierta información sobre cómo modificar las ubicaciones que se buscan. 
    
    ![Página desplegable Modificar ubicaciones](../media/56c033f6-6735-46ba-abb2-a263a2b79836.png)
  
    a. Se selecciona **el** botón de alternancia en Seleccionar todo en la sección de buzón en la parte superior de la página desplegable, lo que indica que se busca en todos los buzones. Para restringir el ámbito de la búsqueda, haga clic en el botón de alternancia para anular la selección y, a continuación, haga clic en Elegir **usuarios,** grupos o equipos y elija buzones específicos para buscar.
    
    b. Se selecciona **el** botón de alternancia en Seleccionar todo en la sección de sitios en medio de la página desplegable, lo que indica que se busca en todos los sitios. Para restringir la búsqueda a los sitios seleccionados, anule la selección del botón de alternancia y, a continuación, haga clic **en Elegir sitios.** Tiene que agregar cada sitio específico que desee buscar, incluida la cuenta de OneDrive del interesado.
    
    c. Se selecciona el botón de alternancia en la sección carpetas públicas de Exchange, lo que significa que se busca en todas las carpetas públicas de Exchange. Solo puede buscar en todas las carpetas públicas de Exchange o ninguna de ellas. No puede elegir los específicos en los que buscar.
    
3. Si modifica las ubicaciones de contenido en la búsqueda integrada, haga clic en Guardar **&amp; ejecución** para reiniciar la búsqueda. 

> [!NOTE]
> Al buscar en todas las ubicaciones de buzones o solo en buzones específicos, los datos de otras aplicaciones de Office 365 que se guardan en los buzones de usuario se incluyen al exportar los resultados de la búsqueda. Estos datos no se incluyen en los resultados de búsqueda estimados y no aparecen en la vista previa. Pero se incluye al exportar y descargar los resultados de la búsqueda. Para obtener más información sobre las aplicaciones que almacenan datos en el buzón de un usuario, consulte [Contenido almacenado en buzones de Exchange Online.](/microsoft-365/compliance/what-is-stored-in-exo-mailbox)
  
## <a name="more-information-about-using-the-dsr-case-tool"></a>Más información sobre el uso de la herramienta de casos de DSR

Las secciones siguientes contienen más información sobre el uso de la herramienta de casos DSR para responder a solicitudes de exportación de DSR.
  
[Exportación de datos desde el servicio de itinerancia de Office](#exporting-data-from-the-office-roaming-service)

[Exportar elementos parcialmente indizados](#exporting-partially-indexed-items)

[Búsqueda y exportación de datos de Microsoft Teams y Grupos de Microsoft 365](#searching-and-exporting-data-from-microsoft-teams-and-microsoft-365-groups)

[Buscar carpetas públicas de Exchange](#searching-exchange-public-folders)
  
### <a name="exporting-data-from-the-office-roaming-service"></a>Exportación de datos desde el servicio de itinerancia de Office

Puede usar la herramienta de caso de DSR para buscar y exportar datos de uso generados por el servicio de itinerancia de Office. La itinerancia es un servicio que almacena la configuración relacionada con Office, como el tema de Office, el diccionario personalizado, la configuración de idioma, el modo de desarrollador y la corrección automática. 
    
Los datos del servicio de itinerancia de Office se almacenan en el buzón de un interesado en una carpeta oculta ubicada en un subárbol de mensajes no interpersonales (no IPM) de buzones de Exchange Online. Esto significa que los datos se ocultan de la vista del usuario cuando usan Outlook u otros clientes de correo para obtener acceso a su buzón. Para obtener más información acerca de las carpetas ocultas, vea [Carpetas ocultas mapi](https://go.microsoft.com/fwlink/?linkid=872758).
  
Puede crear una búsqueda de contenido independiente (y asociarla con un caso de DSR) que devuelva los datos de uso del servicio de itinerancia de Office en el buzón del interesado. Estos datos no se incluyen en las estadísticas de búsqueda y no estarán disponibles para la versión preliminar. Pero puede exportarlo y, a continuación, dájelo al interesado en respuesta a una solicitud de exportación de DSR.
  
Al exportar datos desde el servicio de itinerancia de Office, los datos se guardan en una carpeta independiente que se encuentra en la carpeta **ApplicationDataRoot,** que se encuentra en una carpeta que es el nombre con la dirección de correo electrónico del interesado. Estos datos se exportan como archivos JSON, que son archivos de texto legibles para personas similares a los archivos XML o TXT, que se adjuntan a los mensajes de correo electrónico. Actualmente, esta carpeta tiene el nombre del identificador único global (GUID): **1caee58f-eb14-4a6b-9339-1fe2ddf6692b**. En versiones futuras de la herramienta de caso de DSR, el GUID se reemplazará por el nombre de la aplicación real. 

   
 **Para buscar y exportar datos del servicio de itinerancia de Office:**
  
1. En el Centro de seguridad  & cumplimiento, haga clic en Solicitudes del interesado de privacidad de datos y, a continuación, haga clic en Abrir junto al caso DSR del interesado del que desea exportar los datos de \> uso.  
    
2. Haga clic **en la pestaña** Buscar en la parte superior de la página y, a continuación, haga clic en Agregar búsqueda guiada por ![ ](../media/ITPro-EAC-AddIcon.gif) **iconos.**
    
3. Haga **clic en Cancelar** en la página Nombre de **la** búsqueda. 
    
4. En **Consulta de búsqueda,** en **la** condición Tipo, active la casilla junto al servicio **de itinerancia de Office.** 
    
    ![Activar la casilla servicio de itinerancia de Office para exportar los datos de uso](../media/O365_DSRCase_SDSDataExport1.png)
  
    La **condición Type** (que son clases de mensajes de correo electrónico) debe ser el único elemento de la consulta de búsqueda. Puede eliminar el cuadro **Palabras clave** o dejarlo en blanco. 
    
5. En **Ubicaciones,** asegúrese de que **las ubicaciones específicas** están seleccionadas y, a continuación, haga clic en **Modificar**.
    
6. En la parte superior de **la** página desplegable Modificar ubicaciones (sección buzón), haga clic en Elegir **usuarios, grupos o equipos.**
    
7. En la **página Editar ubicaciones,** haga clic en Elegir usuarios, grupos o **equipos,** elija el buzón del interesado y, a continuación, guarde la selección. 
    
8. Haga **clic en & ejecutar** y, a continuación, asigne un nombre a la búsqueda y guárdela.
    
    La búsqueda se inicia.
    
 **Para exportar datos del servicio de itinerancia de Office:**
  
1. Una vez completada la búsqueda que creó  en el paso anterior, haga clic en la pestaña Buscar en la parte superior de la página y, a continuación, haga clic en la casilla situada junto a la búsqueda. Es posible que tenga que hacer clic ![ en ](../media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) **Actualizar actualización** para mostrar la búsqueda. 
    
2. En la página desplegable de búsqueda, haga clic en el icono Exportar resultados de búsqueda Más y, a continuación, seleccione Exportar resultados ![ de la lista ](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) desplegable.  
    
3. En la **página Exportar resultados,** seleccione las opciones recomendadas para exportar datos de uso. 
    
    ![Opciones de exportación al exportar datos de uso del servicio de itinerancia de Office](../media/470a7d1e-eeae-4b42-95aa-15cb82ce2f68.png)
  
    a. En Opciones de salida, seleccione la primera opción (Todos los elementos, excepto los que tienen uno que tiene un formato no reconocido, están **cifrados** o no se indexaron por otros motivos) para exportar solo elementos indizados.
    
    b. En **Exportar contenido de Exchange como**, seleccione la segunda opción, un archivo PST que contiene todos los **mensajes.**
    
    c. Deje las opciones de exportación restantes sin elegir.
    
4. Después de elegir la configuración de exportación, haga clic **en Exportar**.
    
    Los resultados de la búsqueda están preparados para su descarga, lo que significa que se cargan en el área de almacenamiento de Azure para su organización en la nube de Microsoft. Los pasos siguientes muestran cómo descargar estos datos en el equipo local.
    
5. Haga clic **en la pestaña** Exportar para mostrar el trabajo de exportación que ha creado. Los trabajos de exportación tienen el mismo nombre que la búsqueda correspondiente **con _Export** al final del nombre de búsqueda. 
    
6. Haga clic en el trabajo de exportación que acaba de crear para mostrar la página desplegable de exportación. 
    
7. En **Clave de exportación**, haga clic en **Copiar al Portapapeles**. Use esta clave en el paso 10 para descargar los resultados de la búsqueda.
    
8. Haga ![ clic en exportar el icono de resultados de búsqueda ](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Descargar** resultados en la parte superior de la página desplegable de exportación. 
    
9. En la ventana emergente en la parte inferior de la página, haga clic en Abrir **para** abrir la herramienta de exportación **de exhibición de documentos electrónicos.** La **herramienta de exportación de** exhibición de documentos electrónicos se instalará la primera vez que descargue los resultados de la búsqueda. 
    
10. En la **Herramienta de exportación de eDiscovery**, pegue la clave de exportación que ha copiado en el paso 7 en el cuadro correspondiente.
    
11. Haga clic en **Examinar** para especificar la ubicación en la que desea descargar los archivos de los resultados de la búsqueda. 
    
    > [!NOTE]
    > Debido a la gran cantidad de actividad de disco (lecturas y escrituras), debes descargar los resultados de la búsqueda en una unidad de disco local; no los descargue en una unidad de red asignada u otra ubicación de red. 
  
12. Haga clic en **Iniciar** para descargar los resultados de la búsqueda en el equipo. 
    
    La **Herramienta de exportación de exhibición de documentos electrónicos** muestra información del estado acerca del proceso de exportación, incluida una estimación del número (y tamaño) de los elementos restantes que se van a descargar. Una vez completado el proceso de exportación, puede abrir el archivo PST de Exchange en Outlook y, a continuación, ir a la carpeta **ApplicationDataRoot** para obtener acceso a la subcarpeta del servicio de itinerancia. 
    
    Como se ha explicado anteriormente, los archivos JSON que contienen datos de uso se adjuntan a los mensajes. Para ver un archivo JSON, haga clic en un mensaje y, a continuación, abra el archivo JSON adjunto. 
  
### <a name="exporting-partially-indexed-items"></a>Exportar elementos parcialmente indizados

Se recomienda no exportar elementos parcialmente indizados (también denominados elementos no indexados) de la búsqueda integrada que se crea al crear un caso de DSR. Esto se debe a que es más probable que los resultados de la búsqueda incluyan elementos parcialmente indizados para otros usuarios de la organización y no solo elementos parcialmente indizados para el interesado. En su lugar, se recomienda crear una búsqueda de contenido independiente que esté asociada con el caso DSR diseñado para exportar solo los elementos parcialmente indizados relacionados con el interesado. 
  
Este es un proceso de alto nivel para exportar elementos parcialmente indizados. Después de exportarlos, puede revisarlos para determinar si un elemento responde a una solicitud de acceso o exportación de DSR.
  
1. Abra el caso de DSR y cree una búsqueda en la **página** de búsqueda. 
    
2. Use los siguientes criterios para configurar la consulta de búsqueda y las ubicaciones de contenido en las que buscar:
    
    - Use una consulta de palabra clave vacía o vacía. Esto devuelve todos los elementos de las ubicaciones de contenido en las que se busca.
    
    - Busque solo el buzón de Exchange Online del interesado y su cuenta de OneDrive.
    
3. Después de ejecutar la búsqueda y completarla, puede exportar y descargar los resultados de la búsqueda (como se describe en el [paso 4).](#step-4-export-the-data) Use la siguiente configuración para exportar elementos parcialmente indizados. 
    
    - En Opciones de salida, seleccione la tercera opción (solo los elementos que tengan un formato no **reconocido,** estén cifrados o no se indexen por otros motivos) para exportar solo elementos parcialmente indizados.
    
    - En **Exportar contenido de Exchange como**, puede seleccionar cualquier opción según sus preferencias. 
    
    - Al seleccionar la opción Incluir versiones para documentos de **SharePoint,** se exportan versiones de documentos si una versión está parcialmente indizada. 
    
Para obtener más información acerca de los elementos parcialmente indizados, vea: 
  
- [Elementos parcialmente indizados en la búsqueda de contenido en Office 365](/microsoft-365/compliance/partially-indexed-items-in-content-search)

- [Exportar elementos parcialmente indizados](/microsoft-365/compliance/export-search-results#exporting-partially-indexed-items)

### <a name="searching-and-exporting-data-from-microsoft-teams-and-microsoft-365-groups"></a>Búsqueda y exportación de datos de Microsoft Teams y Grupos de Microsoft 365

Las conversaciones que forman parte de la lista de chat en Microsoft Teams (denominadas chats de equipo o chats uno a uno) se almacenan en el buzón de Exchange Online de los usuarios que participan en los chats. Además, los archivos que comparte una persona en un chat de uno a uno se almacenan en la cuenta de OneDrive de la persona que comparte el archivo. Dado que la búsqueda integrada busca en todos los buzones y cuentas de OneDrive de la organización, los chats de equipo y los documentos compartidos en una sesión de chat (que el interesado creó o cartó) se devuelven mediante la búsqueda integrada en un caso de DSR.
  
Como alternativa, las conversaciones que forman parte de un canal de Teams (también denominados mensajes de canal) se almacenan en el buzón asociado con un equipo. La búsqueda integrada también devuelve estos tipos de conversaciones en las que participó el interesado, ya que se busca en todos los buzones asociados con Teams. Además, los archivos que comparte un interesado en un canal de Teams se almacenan en el sitio de SharePoint del equipo. Los archivos creados o cargados por el interesado son devueltos por la búsqueda integrada en un caso de DSR porque los sitios asociados con Teams se incluyen en la búsqueda.
  
De forma similar, los buzones y los sitios de SharePoint que corresponden a un grupo de Microsoft 365 también se incluyen en la búsqueda integrada. Esto significa que se devuelven los mensajes de correo electrónico enviados o recibidos por el interesado y los archivos creados o cargados por el interesado. 
  
Para obtener más información acerca del uso de la búsqueda de contenido para buscar elementos en Microsoft Teams y grupos de Microsoft 365 o para ver cómo obtener una lista de miembros, vea la sección "Búsqueda de Microsoft Teams y grupos de Microsoft 365" en Búsqueda de contenido en [Microsoft 365.](/microsoft-365/compliance/content-search#searching-microsoft-teams-and-microsoft-365-groups) 
  
### <a name="searching-exchange-public-folders"></a>Buscar carpetas públicas de Exchange

La búsqueda integrada en un caso de DSR solo devolverá mensajes de correo electrónico que el interesado envió a una carpeta pública habilitada para correo o mensajes que otra persona envió a una carpeta pública y también copió el interesado. No devuelve mensajes que el interesado publicó en una carpeta pública. Para buscar elementos que el interesado publicó en una carpeta pública, puede crear una búsqueda de contenido independiente que busque cualquier elemento publicado en una carpeta pública por el interesado.
  
Este es un proceso de alto nivel para buscar elementos que el interesado publicó en una carpeta pública. 
  
1. Abra el caso de DSR y cree una búsqueda en la **página** de búsqueda. 
    
2. Use los siguientes criterios para configurar la consulta de búsqueda y las ubicaciones de contenido en las que buscar:
    
  - En el **cuadro Palabras clave,** use la siguiente consulta de búsqueda: 
    
    ```powershell
    itemclass:ipm.post AND "<email address of the data subject>"
    ```

  - Buscar en todas las carpetas públicas de Exchange
    
  - Después de ejecutar la búsqueda y completarla, puede exportar y descargar los resultados de la búsqueda (como se describe en el [paso 4).](#step-4-export-the-data) Use la siguiente configuración para exportar elementos parcialmente indizados. 
