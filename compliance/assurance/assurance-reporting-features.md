---
title: Características de informes de Microsoft 365
description: Obtenga información sobre varias características de informes de Microsoft 365, como Azure Active Directory y Exchange Online.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-analytics
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: a745c470dc30703f438258985169431c1053e65d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120789"
---
# <a name="microsoft-365-reporting-features"></a>Características de informes de Microsoft 365

Las características de informes de Microsoft 365 proporcionan diversos informes de auditoría para Azure Active Directory (Azure AD), Exchange Online, administración de dispositivos, revisión de supervisión y prevención de pérdida de datos (DLP). Estos informes son diferentes e independientes de los informes de actividad de Microsoft 365.

## <a name="microsoft-365-reports-dashboard"></a>Panel informes de Microsoft 365

El panel Informes de la vista previa del Centro de administración de Microsoft 365 muestra la actividad de uso en Microsoft 365. Los administradores globales de Microsoft 365, o un administrador de Exchange Online, SharePoint Online o Skype Empresarial, pueden obtener información detallada sobre el uso de ese servicio. Por ejemplo, el número de usuarios de un servicio de Microsoft 365 concreto, el número de usuarios que han activado Aplicaciones de Microsoft 365 para empresas (anteriormente denominado Office 365 ProPlus) y la cantidad de correo que fluye por la organización. Los informes están disponibles durante los últimos 7, 30, 90 y 180 días.

Los siguientes informes están disponibles:

- [Informe de actividad de correo electrónico](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44)
- [Microsoft Office de activaciones](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Microsoft-Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60)
- [Informe de uso del sitio de SharePoint Online](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)
- [Informe de uso de OneDrive para la Empresa](https://support.office.com/article/Office-365-Reports-in-the-Admin-Center-Preview--OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)
- [Informe de actividad de Yammer](https://support.office.com/article/View-the-Yammer-Activity-report-in-the-Office-365-admin-center-preview-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a)
- [Informe de actividad de Skype Empresarial](/SkypeForBusiness/skype-for-business-online-reporting/activity-report)
- [Informe de actividad punto a punto de Skype Empresarial](/SkypeForBusiness/skype-for-business-online-reporting/peer-to-peer-activity-report)
- [Informe del organizador de conferencias de Skype Empresarial](/SkypeForBusiness/skype-for-business-online-reporting/conference-organizer-activity-report)
- [Informe de actividad de participantes de conferencias de Skype Empresarial](/SkypeForBusiness/skype-for-business-online-reporting/conference-participant-activity-report)

Para obtener más información, vea [Informes de actividades en el Centro de administración de Microsoft 365.](https://support.office.com/article/activity-reports-in-the-office-365-admin-center-0d6dfb17-8582-4172-a9a9-aed798150263)

## <a name="azure-ad-reports"></a>Informes de Azure AD

Microsoft 365 usa Azure AD para la autenticación y la administración de identidades. Los administradores de Microsoft 365 usan informes generados por Azure para identificar actividad inusual y acceso no autorizado a sus datos. Puedes usar los informes de acceso y uso en Azure AD para obtener visibilidad de la integridad de directorio y la seguridad de la organización. Con esta información, puede identificar y mitigar posibles riesgos de seguridad.

Los informes de Azure AD se pueden exportar a Microsoft Excel y correlacionarse con otros datos de Microsoft 365. Por ejemplo, los resultados de una búsqueda de registros de auditoría pueden proporcionar información sobre el acceso, la autenticación y las actividades de nivel de aplicación. Los informes avanzados de anomalías y uso de recursos están disponibles con Azure AD Premium. Estos informes avanzados ayudan a mejorar la posición de seguridad y a responder a posibles amenazas mediante la aplicación de análisis sobre el acceso a dispositivos y el uso de aplicaciones. Para obtener más información, [vea informes de Azure Active Directory.](/azure/active-directory/reports-monitoring/overview-reports/)

## <a name="exchange-online-audit-reports"></a>Informes de auditoría de Exchange Online

Los informes de auditoría de Exchange Online incluyen detalles sobre el acceso al buzón y los cambios realizados por los administradores en su inquilino de Exchange Online. Con la auditoría de buzones, puede usar las tareas de la tabla siguiente para ejecutar informes y exportar registros de auditoría de Exchange Online.

> [!NOTE]
> Debe habilitar el registro de auditoría de buzones para cada buzón de modo que los eventos auditados se guarden en el registro de auditoría de ese buzón. Si el registro de auditoría de buzones no está habilitado para un buzón, los eventos de ese buzón no se guardarán en el registro de auditoría y no aparecerán en los informes de auditoría de buzones. Para obtener más información, vea [habilitar la auditoría de buzones de correo.](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918)

| Task | Descripción |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ejecución de un informe de acceso al buzón de correo del que no se es propietario](/exchange/security-and-compliance/exchange-auditing-reports/non-owner-mailbox-access-report) | Muestra la lista de buzones a los que ha accedido otra persona que no sea el propietario del buzón. El informe contiene información sobre quién tuvo acceso al buzón, las acciones que realizó en el buzón y si las acciones se realizaron correctamente. |
| [Exportar registros de auditoría de buzones](/exchange/security-and-compliance/exchange-auditing-reports/export-mailbox-audit-logs) | Los registros de auditoría de buzones de correo contienen información sobre el acceso y las acciones realizadas en un buzón por un usuario que no es el propietario del buzón. Los administradores pueden especificar buzones junto con un intervalo de fechas para generar informes. Los registros se exportan en XML, se adjuntan a un mensaje y se envían a usuarios específicos según lo determinado por el administrador. |
| [Realización de un informe de grupo de roles de administrador](/Office365/SecurityCompliance/eop/run-an-administrator-role-group-report-in-eop-eop) | El grupo de roles de administrador asigna privilegios administrativos a los usuarios. Estos privilegios permiten a los usuarios realizar tareas administrativas como restablecer contraseñas, crear o modificar buzones y asignar privilegios de administrador a otros usuarios. El informe del grupo de roles de administración muestra los cambios en los grupos de roles, incluida la adición o eliminación de miembros. |
| [Ver el registro de auditoría de administración](/exchange/security-and-compliance/exchange-auditing-reports/view-administrator-audit-log) | El informe de registro de auditoría de administración enumera todas las funciones de creación, actualización y eliminación realizadas por los administradores en Exchange Online. Las entradas de registro proporcionan información sobre qué cmdlet se ejecutó, qué parámetros se usaron, quién ejecutó el cmdlet y qué objetos se vieron afectados. |
| [Búsqueda y retención de contenido de buzones](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery) | Proporciona detalles de los cambios realizados en In-Place de exhibición de documentos electrónicos o In-Place de retención local en los buzones. |
| [Exportar el registro de auditoría de administración](/exchange/security-and-compliance/exchange-auditing-reports/search-role-group-changes) | El registro de auditoría de administración registra acciones administrativas específicas, como crear, actualizar y eliminar en Exchange Online. Los resultados del registro se exportan a XML y los administradores pueden elegir enviar este registro a un conjunto de usuarios. |
| [Realización de un informe de retención por juicio por buzón](/exchange/security-and-compliance/exchange-auditing-reports/per-mailbox-litigation-hold-report) | Proporciona detalles de los cambios en la configuración de retención por juicio en los buzones. |
| [Ver y exportar el registro de auditoría de administrador externo](/exchange/security-and-compliance/exchange-auditing-reports/view-external-admin-audit-log) | Contiene detalles de las acciones realizadas por administradores externos. Las entradas proporcionan información sobre qué cmdlet se ha ejecutado, qué parámetros se usaron y las acciones que crean, modifican o eliminan objetos en Exchange Online. |

## <a name="device-compliance-reports"></a>Informes de cumplimiento de dispositivos

Los dispositivos móviles conectados a la suscripción se administran y protegen mediante movilidad y seguridad básicas para Microsoft 365. Los dispositivos móviles usados para acceder al correo electrónico, el calendario, los contactos y los documentos del trabajo desempeñan un papel importante a la hora de garantizar que los empleados puedan trabajar en cualquier momento y desde cualquier lugar. Es fundamental que proteja la información de su organización. Puede usar movilidad y seguridad básicas para Microsoft 365 para establecer directivas de seguridad de dispositivos y reglas de acceso. Si se pierde o se roba, también se usa la movilidad básica y la seguridad de Microsoft 365 para borrar los dispositivos móviles.

Los informes básicos de cumplimiento de movilidad y seguridad proporcionan información general sobre las directivas configuradas por una organización para proteger los dispositivos móviles que tienen acceso a los datos de Microsoft 365. El informe permite filtrar los dispositivos por estado de cumplimiento, infracciones notificadas, dispositivos bloqueados y cuántos dispositivos se borraron como resultado de las directivas de seguridad. Para obtener más información, vea Información general sobre movilidad y [seguridad básicas de Microsoft 365.](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a)

## <a name="data-loss-prevention"></a>Prevención de pérdida de datos

Las directivas DLP ayudan a administrar la seguridad y el flujo de información de una organización. Puede configurar directivas para bloquear el acceso al contenido, cifrar datos o notificar a los usuarios las infracciones de directivas y directivas mediante sugerencias de directiva DLP en la aplicación. Los informes DLP proporcionan información sobre el número de coincidencias de directivas y reglas, invalidaciones y falsos positivos.

Use el Centro de administración de Microsoft 365 para ver información sobre el número de mensajes detectados por las directivas DLP. Los informes DLP proporcionan información sobre las coincidencias de directivas y reglas para el correo enviado y recibido. También puede ver el número de coincidencias, invalidaciones y falsos positivos de cada directiva en las últimas 24 horas con el Centro de administración de Exchange. Si descarga un informe de Excel, puede ver aún más detalles, como quién envió el mensaje, en qué día y qué coincidencias de directiva se desencadenaron. Para obtener más información, vea [Ver informes sobre las detecciones de directivas DLP.](/previous-versions/exchange-server/exchange-150/jj889415(v=exchg.150))

## <a name="auditing-in-yammer-enterprise"></a>Auditoría en Yammer Enterprise

Yammer Enterprise proporciona a los administradores la capacidad de exportar datos de actividad de usuario desde su red de Yammer a través de la API de exportación de datos de [Yammer](https://support.office.com/article/export-data-from-yammer-enterprise-b303d8f3-007d-4ad4-81f8-54fb1ecfb3f2)o manualmente a través de la página de administración de red de Yammer. La capacidad de exportar registros está restringida a los administradores de red en Yammer. (Todos los administradores globales de Microsoft 365 son administradores de red de Yammer).

Los siguientes datos son exportables:

| Filename | Descripción |
|----------------------------|-------------------------------------------------------------------------|
| Users.csv | Todos los usuarios nuevos, pendientes y suspendidos de la red |
| Messages.csv | Todos los mensajes de la red |
| Files.csv (metadatos) | Metadatos como el nombre de archivo, la dirección URL de la API de archivos, el identificador del usuario de carga, los que se cargan, etc. |
| Files.csv (archivos originales) | Archivo zip de los archivos originales cargados por los usuarios en Yammer |
| Topics.csv | Temas creados en la red |
| Pages.csv | Páginas (notas) creadas por los usuarios de la red |
| Admins.csv | Todos los administradores comprobados de la red |
| Networks.csv | Todas las redes externas de Yammer |

Los datos de Yammer Enterprise también están disponibles a través de los informes de actividad de Microsoft 365. Además, Yammer está trabajando activamente en la exposición de registros adicionales a través de la API de actividad de administración de Microsoft 365 y en la capacidad de realizar una razón sobre los datos con Power BI. Vea el mapa [de ruta de Office](https://fasttrack.microsoft.com/roadmap?filters=yammer) para obtener más información sobre estas características.
