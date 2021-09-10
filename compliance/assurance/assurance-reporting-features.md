---
title: Características de creación de informes de Microsoft 365
description: Obtenga información sobre varias características de informes dentro de Microsoft 365, incluidos Azure Active Directory y Exchange Online.
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
- M365-analytics
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: be05c96c725f8d0e05bc27f410d7f19e4e5d9a23
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947219"
---
# <a name="microsoft-365-reporting-features"></a>Características de creación de informes de Microsoft 365

Las características de informes de Microsoft 365 proporcionan varios informes de auditoría para Azure Active Directory (Azure AD), Exchange Online, administración de dispositivos, revisión de supervisión y prevención de pérdida de datos (DLP). Estos informes son diferentes y independientes de los Microsoft 365 de actividad.

## <a name="microsoft-365-reports-dashboard"></a>Microsoft 365 Panel de informes

El panel Informes de la vista Centro de administración de Microsoft 365 muestra la actividad de uso en Microsoft 365. Microsoft 365 administradores globales, o un administrador de Exchange Online, SharePoint Online o Skype Empresarial, pueden obtener información detallada sobre el uso de ese servicio. Por ejemplo, el número de usuarios de un servicio de Microsoft 365 determinado, el número de usuarios que han activado Aplicaciones Microsoft 365 para empresas (anteriormente denominado Office 365 ProPlus) y la cantidad de correo que fluye a través de la organización. Los informes están disponibles durante los últimos 7, 30, 90 y 180 días.

Los siguientes informes están disponibles:

- [Informe de actividad de correo electrónico](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44)
- [Microsoft Office activaciones](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Microsoft-Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60)
- [SharePoint Informe de uso del sitio en línea](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)
- [OneDrive para la Empresa de uso](https://support.office.com/article/Office-365-Reports-in-the-Admin-Center-Preview--OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)
- [Informe de actividad de Yammer](https://support.office.com/article/View-the-Yammer-Activity-report-in-the-Office-365-admin-center-preview-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a)
- [Skype Empresarial actividad](/SkypeForBusiness/skype-for-business-online-reporting/activity-report)
- [Skype Empresarial Informe de actividad punto a punto](/SkypeForBusiness/skype-for-business-online-reporting/peer-to-peer-activity-report)
- [Skype Empresarial Informe del organizador de conferencias](/SkypeForBusiness/skype-for-business-online-reporting/conference-organizer-activity-report)
- [Skype Empresarial Informe de actividad de participantes de conferencia](/SkypeForBusiness/skype-for-business-online-reporting/conference-participant-activity-report)

Para obtener más información, vea [Informes de actividad en el Centro de administración de Microsoft 365](https://support.office.com/article/activity-reports-in-the-office-365-admin-center-0d6dfb17-8582-4172-a9a9-aed798150263).

## <a name="azure-ad-reports"></a>Informes de Azure AD

Microsoft 365 usa Azure AD para la autenticación y la administración de identidades. Microsoft 365 administradores usan informes generados por Azure para identificar actividad inusual y acceso no autorizado a sus datos. Puede usar los informes de acceso y uso en Azure AD para obtener visibilidad de la integridad y seguridad del directorio para su organización. Con esta información, puede identificar y mitigar posibles riesgos de seguridad.

Los informes de Azure AD se pueden exportar a Microsoft Excel y correlacionarse con otros datos de Microsoft 365. Por ejemplo, los resultados de una búsqueda de registro de auditoría pueden proporcionar información sobre el acceso, la autenticación y las actividades de nivel de aplicación. Los informes avanzados de anomalías y uso de recursos están disponibles con Azure AD Premium. Estos informes avanzados ayudan a mejorar la posición de seguridad y te ayudan a responder a posibles amenazas mediante la aplicación de análisis sobre el acceso a dispositivos y el uso de aplicaciones. Para obtener más información, [vea Azure Active Directory reporting](/azure/active-directory/reports-monitoring/overview-reports/).

## <a name="exchange-online-audit-reports"></a>Exchange Online Informes de auditoría

Exchange Online informes de auditoría incluyen detalles sobre el acceso a buzones y los cambios realizados por los administradores en el Exchange Online inquilino. Con la auditoría de buzones, puede usar las tareas de la tabla siguiente para ejecutar informes y exportar Exchange Online registros de auditoría.

> [!NOTE]
> Debe habilitar el registro de auditoría de buzones para cada buzón para que los eventos auditados se guarden en el registro de auditoría de ese buzón. Si el registro de auditoría de buzones no está habilitado para un buzón, los eventos de ese buzón no se guardarán en el registro de auditoría y no aparecerán en los informes de auditoría de buzones. Para obtener más información, vea [enable mailbox auditing](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918).

| Tarea | Descripción |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ejecutar un informe de acceso al buzón de correo del que no se es propietario](/exchange/security-and-compliance/exchange-auditing-reports/non-owner-mailbox-access-report) | Muestra la lista de buzones a los que tiene acceso otra persona que no sea el propietario del buzón. El informe contiene información sobre quién tuvo acceso al buzón, las acciones que realizaron en el buzón y si las acciones se realizaron correctamente. |
| [Exportar registros de auditoría de buzones](/exchange/security-and-compliance/exchange-auditing-reports/export-mailbox-audit-logs) | Los registros de auditoría de buzones de correo contienen información sobre el acceso y las acciones de un buzón realizado por un usuario que no sea el propietario del buzón. Los administradores pueden especificar buzones junto con un intervalo de fechas para generar informes. Los registros se exportan en XML, se adjuntan a un mensaje y se envían a usuarios específicos según lo determine el administrador. |
| [Ejecutar un informe de grupo de roles de administrador](/Office365/SecurityCompliance/eop/run-an-administrator-role-group-report-in-eop-eop) | El grupo de roles de administrador asigna privilegios administrativos a los usuarios. Estos privilegios permiten a los usuarios realizar tareas administrativas como restablecer contraseñas, crear o modificar buzones y asignar privilegios de administrador a otros usuarios. El informe de grupo de roles de administración muestra los cambios en los grupos de roles, incluida la adición o eliminación de miembros. |
| [Ver el registro de auditoría de administrador](/exchange/security-and-compliance/exchange-auditing-reports/view-administrator-audit-log) | El informe de registro de auditoría de administración enumera todas las funciones de creación, actualización y eliminación realizadas por los administradores en Exchange Online. Las entradas de registro proporcionan información sobre qué cmdlet se ejecutó, qué parámetros se usaron, quién ejecutó el cmdlet y qué objetos se vieron afectados. |
| [Búsqueda y retención de contenido de buzones](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery) | Proporciona detalles de los cambios realizados In-Place la exhibición de documentos electrónicos o la In-Place de retención en los buzones. |
| [Exportar el registro de auditoría de administración](/exchange/security-and-compliance/exchange-auditing-reports/search-role-group-changes) | El registro de auditoría de administración registra acciones administrativas específicas, como crear, actualizar y eliminar en Exchange Online. Los resultados del registro se exportan a XML y los administradores pueden elegir enviar este registro a un conjunto de usuarios. |
| [Realización de un informe de suspensión por litigio por buzón](/exchange/security-and-compliance/exchange-auditing-reports/per-mailbox-litigation-hold-report) | Proporciona detalles de los cambios realizados en la configuración de retención por juicio en los buzones. |
| [Ver y exportar el registro de auditoría de administración externa](/exchange/security-and-compliance/exchange-auditing-reports/view-external-admin-audit-log) | Contiene detalles de las acciones realizadas por administradores externos. Las entradas proporcionan información sobre qué cmdlet se ha ejecutado, qué parámetros se usaron y las acciones que crean, modifican o eliminan objetos en Exchange Online. |

## <a name="device-compliance-reports"></a>Informes de cumplimiento de dispositivos

Puedes administrar y proteger los dispositivos móviles conectados a tu suscripción con Movilidad y seguridad básicas para Microsoft 365. Los dispositivos móviles que se usan para tener acceso al correo electrónico, el calendario, los contactos y los documentos de trabajo desempeñan un papel importante para asegurarse de que los empleados puedan trabajar en cualquier momento y desde cualquier lugar. Es fundamental que proteja la información de su organización. Usas movilidad y seguridad básicas para Microsoft 365 para establecer directivas de seguridad de dispositivos y reglas de acceso. Si se pierde o se roba, también se usa movilidad y seguridad básicas para Microsoft 365 borrar los dispositivos móviles.

Los informes de cumplimiento básico de movilidad y seguridad proporcionan una introducción a las directivas configuradas por una organización para proteger los dispositivos móviles que tienen acceso a Microsoft 365 datos. El informe permite filtrar los dispositivos por el estado de cumplimiento, las infracciones notificadas, los dispositivos bloqueados y el número de dispositivos eliminados como resultado de las directivas de seguridad. Para obtener más información, vea [Overview of Basic Mobility and Security for Microsoft 365](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a).

## <a name="data-loss-prevention"></a>Prevención de pérdida de datos

Las directivas DLP ayudan a administrar la seguridad y el flujo de información de una organización. Puede configurar directivas para bloquear el acceso al contenido, cifrar datos o notificar a los usuarios de infracciones de directivas y directivas mediante directivas DLP en la aplicación Sugerencias. Los informes DLP proporcionan información sobre el número de coincidencias de directivas y reglas, invalidaciones y falsos positivos.

Use el Centro de administración de Microsoft 365 para ver información sobre el número de mensajes detectados por las directivas DLP. Los informes DLP proporcionan información sobre las coincidencias de directivas y reglas para el correo enviado y recibido. También puede ver el número de coincidencias, invalidaciones y falsos positivos para cada directiva en las últimas 24 horas mediante el centro de administración Exchange de administración. Si descarga un informe Excel, puede ver aún más detalles, como quién envió el mensaje, en qué día y qué coincidencias de directiva se desencadenaron. Para obtener más información, vea [Ver informes sobre detecciones de directivas DLP](/previous-versions/exchange-server/exchange-150/jj889415(v=exchg.150)).

## <a name="auditing-in-yammer-enterprise"></a>Auditoría en Yammer Enterprise

Yammer Enterprise proporciona a los administradores la capacidad de exportar datos de actividad de usuario desde su red de Yammer a través de la API de exportación de datos de [Yammer](https://support.office.com/article/export-data-from-yammer-enterprise-b303d8f3-007d-4ad4-81f8-54fb1ecfb3f2)o manualmente a través de la página de administración de Yammer de red. La capacidad de exportar registros está restringida a los administradores de red en Yammer. (Todos Microsoft 365 administradores globales son Yammer de red).

Los siguientes datos son exportables:

| Filename | Descripción |
|----------------------------|-------------------------------------------------------------------------|
| Users.csv | Todos los usuarios nuevos, pendientes y suspendidos de la red |
| Messages.csv | Todos los mensajes de la red |
| Files.csv (metadatos) | Metadatos como nombre de archivo, dirección URL de api de archivos, id. de carga, cargado en, etc. |
| Files.csv (archivos originales) | Archivo zip de los archivos originales cargados por los usuarios en Yammer |
| Topics.csv | Temas creados en la red |
| Pages.csv | Páginas (notas) creadas por usuarios en la red |
| Admins.csv | Todos los administradores comprobados de la red |
| Networks.csv | Todas Yammer redes externas |

Yammer Enterprise datos también están disponibles a través de los Microsoft 365 de actividad. Además, Yammer está trabajando activamente en exponer registros adicionales a través de la API de actividad de administración de Microsoft 365 y en la capacidad de razonar los datos mediante Power BI. Consulta el [Office guía básica para](https://fasttrack.microsoft.com/roadmap?filters=yammer) obtener más información sobre estas características.
