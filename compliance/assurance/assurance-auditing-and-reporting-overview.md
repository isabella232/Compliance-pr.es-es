---
title: Auditoría e informes en los servicios en la nube de Microsoft
description: Información general sobre las características de auditoría e informes de Office 365, Microsoft 365 y Service Assurance.
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
- M365-analytics
- SPO_Content
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: c1a2cc9e770678683fb3823da73ed667de6d1f2b
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482183"
---
# <a name="auditing-and-reporting-in-microsoft-cloud-services"></a>Auditoría e informes en los servicios en la nube de Microsoft

Los servicios en la nube de Microsoft incluyen varias características de auditoría e informes que puede usar para realizar un seguimiento de la actividad administrativa y del usuario en su inquilino, Entre los ejemplos se incluyen los cambios realizados en las opciones de configuración de inquilinos de Exchange Online y SharePoint Online, y los cambios realizados por los usuarios en documentos y otros elementos. Puede usar la información de auditoría y los informes disponibles en los servicios en la nube de Microsoft para administrar de forma más eficaz la experiencia del usuario, mitigar los riesgos y cumplir las obligaciones de cumplimiento.

## <a name="security--compliance-centers"></a>Centros de & seguridad

El Centro de cumplimiento de [Microsoft 365 Security &,](https://protection.office.com)el Centro de seguridad de [Microsoft 365](https://security.microsoft.com)y el Centro de cumplimiento de [Microsoft 365](https://compliance.microsoft.com) son portales únicos para proteger los datos de la organización e incluyen muchas características de auditoría e informes. Estos centros le ayudan con sus necesidades de protección de datos o cumplimiento y auditan la actividad de usuario y administrador. Puedes acceder a estos centros con tu cuenta de administrador de suscripción.

Estos centros incluyen paneles de navegación para obtener acceso a varias características:

- **Alertas:** Permite administrar alertas, ver alertas relacionadas con la seguridad y administrar alertas avanzadas mediante [Cloud App Security](/cloud-app-security/what-is-cloud-app-security).
- **Permisos:** Permite asignar permisos como administrador [de](/microsoft-365/security/office-365-security/grant-access-to-the-security-and-compliance-center) cumplimiento, administrador de exhibición de documentos electrónicos y otros a personas de la organización para que puedan realizar tareas en estos centros. Se asignan permisos para la mayoría de las características de cada centro, pero se deben configurar otros permisos mediante el centro de administración de Exchange y el SharePoint de administración.
- **Administración de amenazas:** Permite crear y aplicar directivas de administración de dispositivos con Movilidad y seguridad básicas para [Microsoft 365](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a), para configurar directivas de prevención de pérdida de datos (DLP) para su organización, para configurar el filtrado de correo electrónico, antimalware, DomainKeys Identified Mail (DKIM), datos adjuntos seguros, [vínculos](/microsoft-365/compliance/data-loss-prevention-policies) seguros y aplicaciones de OAuth.
- **Gobierno de datos:** Permite importar correo electrónico o SharePoint datos de otros sistemas [](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce) [en Microsoft 365,](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84)configurar [](/microsoft-365/compliance/retention-policies) buzones de archivo y establecer directivas de retención para correo electrónico y otro contenido dentro de la organización.
- **Búsqueda & investigación:** Proporciona [](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a)herramientas [](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c)de administración de casos de búsqueda de contenido, registro de auditoría, cuarentena y [exhibición](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da) de documentos electrónicos para profundizar rápidamente en la actividad en buzones de Exchange Online, grupos y carpetas públicas, SharePoint Online y OneDrive para la Empresa.
- **Informes:** Permite acceder rápidamente [](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a) a informes para SharePoint Online, OneDrive para la Empresa, Exchange Online y Azure AD.
- **Garantía de servicio:** Proporciona información sobre cómo Microsoft mantiene la seguridad, la privacidad y el cumplimiento de los estándares globales para Microsoft 365, Azure, Microsoft Dynamics CRM Online, Microsoft Intune y otros servicios en la nube. También incluye acceso a iso de terceros, SOC y otros informes de auditoría, así como controles auditados, que proporciona detalles sobre los distintos controles que han sido probados y comprobados por auditores de terceros de Microsoft 365.

## <a name="service-assurance"></a>Service Assurance

Muchas organizaciones de industrias reguladas están sujetas a amplios requisitos de cumplimiento. Para realizar sus propias evaluaciones de riesgos, los clientes a menudo necesitan información detallada sobre cómo Microsoft 365 la seguridad y privacidad de sus datos. Microsoft se compromete a la seguridad y privacidad de los datos de los clientes en sus servicios en la nube y a ganar la confianza del cliente proporcionando una vista transparente de sus operaciones y un fácil acceso a informes y evaluaciones de cumplimiento independientes.

Service Assurance proporciona transparencia de las operaciones e información sobre cómo Microsoft mantiene la seguridad, privacidad y cumplimiento de los datos de los clientes en Microsoft 365. Incluye informes de auditoría de terceros junto con una biblioteca de documentos técnicos, preguntas frecuentes y otros materiales sobre temas de Microsoft 365 como cifrado de datos, resistencia de datos, administración de incidentes de seguridad y mucho más. Los clientes pueden usar esta información para realizar sus propias evaluaciones de riesgos reglamentarios. Los responsables de cumplimiento pueden asignar el rol "Usuario de Service Assurance" para dar a los usuarios acceso a Service Assurance. El administrador de inquilinos también puede proporcionar a los usuarios externos, como auditores independientes, acceso a la información en el panel de Service Assurance a través del portal Microsoft Cloud Service [confianza](https://aka.ms/STP) (STP).

## <a name="onedrive-for-business-admin-center"></a>OneDrive para la Empresa de administración

El Microsoft OneDrive de administración le ayuda a administrar de forma rápida y sencilla la configuración de OneDrive para la Empresa de la organización en un solo lugar. Para usar el centro OneDrive administración, es necesario tener acceso a onedrive.com. También debe ser un administrador global de su organización o un administrador personalizado con el SharePoint de administrador. Acceda al centro OneDrive para la Empresa de administración en [https://admin.onedrive.com](https://admin.onedrive.com/) .

Las características clave incluyen un área de cumplimiento que proporciona a los administradores vínculos al centro de administración adecuado para escenarios clave, como buscar en el registro de auditoría, trabajar con DLP, retención, exhibición de documentos electrónicos y alertas.

## <a name="related-links"></a>Vínculos relacionados

- [Características de informes de Microsoft 365](assurance-reporting-features.md)
- [Registro interno para la ingeniería de Microsoft 365](assurance-internal-logging.md)
