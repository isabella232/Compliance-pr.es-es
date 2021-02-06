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
localization_priority: Normal
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
ms.openlocfilehash: 4cb9f68f2c5861905a4246582a3b4530c30988ca
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120710"
---
# <a name="auditing-and-reporting-in-microsoft-cloud-services"></a>Auditoría e informes en los servicios en la nube de Microsoft

Los servicios en la nube de Microsoft incluyen varias características de auditoría e informes que puede usar para realizar un seguimiento de la actividad administrativa y del usuario dentro de su espacio empresarial, algunos ejemplos son los cambios realizados en las opciones de configuración de inquilinos de Exchange Online y SharePoint Online, y los cambios realizados por los usuarios en documentos y otros elementos. Puede usar la información de auditoría y los informes disponibles en los servicios en la nube de Microsoft para administrar de forma más eficaz la experiencia del usuario, mitigar los riesgos y cumplir con las obligaciones de cumplimiento.

## <a name="security--compliance-centers"></a>Centros de & seguridad

El Centro de seguridad [y cumplimiento de Microsoft 365 &,](https://protection.office.com)el Centro de seguridad de Microsoft [365](https://security.microsoft.com)y el Centro de cumplimiento de [Microsoft 365](https://compliance.microsoft.com) son portales únicos para proteger los datos de su organización e incluyen muchas características de auditoría e informes. Estos centros le ayudarán con sus necesidades de protección de datos o cumplimiento y auditan la actividad de los usuarios y administradores. Puede acceder a estos centros con su cuenta de administrador de suscripción.

Estos centros incluyen paneles de navegación para obtener acceso a varias características:

- **Alertas:** Permite administrar alertas, ver alertas relacionadas con la seguridad y administrar alertas avanzadas con [Cloud App Security.](/cloud-app-security/what-is-cloud-app-security)
- **Permisos:** Permite asignar [permisos como](/microsoft-365/security/office-365-security/grant-access-to-the-security-and-compliance-center) administrador de cumplimiento, administrador de exhibición de documentos electrónicos y otros a personas de su organización para que puedan realizar tareas en estos centros. Se asignan permisos para la mayoría de las características de cada centro, pero se deben configurar otros permisos mediante el Centro de administración de Exchange y el Centro de administración de SharePoint.
- **Administración de amenazas:** Permite crear y aplicar directivas de administración de dispositivos con movilidad y seguridad básicas para [Microsoft 365,](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a)para configurar directivas de prevención de pérdida de datos (DLP) para su organización, para configurar el filtrado de correo electrónico, antimalware, domainKeys Identified Mail (DKIM), datos adjuntos seguros, [vínculos](/microsoft-365/compliance/data-loss-prevention-policies) seguros y aplicaciones de OAuth.
- **Gobierno de datos:** Permite importar correo electrónico o datos de SharePoint desde [](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce)otros sistemas a Microsoft [](/microsoft-365/compliance/retention-policies) [365,](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84)configurar buzones de archivo y establecer directivas de retención para el correo electrónico y otro contenido de la organización.
- **Búsqueda & investigación:** Proporciona [](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a)herramientas [](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c)de administración de casos de búsqueda de contenido, registro de auditoría, cuarentena y [exhibición](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da) de documentos electrónicos para explorar rápidamente la actividad en buzones, grupos y carpetas públicas de Exchange Online, SharePoint Online y OneDrive para la Empresa.
- **Informes:** Permite acceder rápidamente a informes [de](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a) SharePoint Online, OneDrive para la Empresa, Exchange Online y Azure AD.
- **Garantía de servicio:** Proporciona información sobre cómo Microsoft mantiene la seguridad, privacidad y cumplimiento con los estándares globales de Microsoft 365, Azure, Microsoft Dynamics CRM Online, Microsoft Intune y otros servicios en la nube. También incluye el acceso a iso de terceros, SOC y otros informes de auditoría, así como controles auditados, que proporcionan detalles sobre los distintos controles que han sido probados y comprobados por auditores externos de Microsoft 365.

## <a name="service-assurance"></a>Service Assurance

Muchas organizaciones de sectores regulados están sujetas a amplios requisitos de cumplimiento. Para realizar sus propias evaluaciones de riesgos, los clientes a menudo necesitan información detallada sobre cómo Microsoft 365 mantiene la seguridad y privacidad de sus datos. Microsoft se compromete a la seguridad y privacidad de los datos de los clientes en sus servicios en la nube y a ganar confianza en los clientes proporcionando una vista transparente de sus operaciones y un fácil acceso a evaluaciones y informes de cumplimiento independientes.

Service Assurance proporciona transparencia de operaciones e información sobre cómo Microsoft mantiene la seguridad, privacidad y cumplimiento de los datos de los clientes en Microsoft 365. Incluye informes de auditoría de terceros junto con una biblioteca de documentos técnicos, preguntas frecuentes y otros materiales sobre temas de Microsoft 365, como el cifrado de datos, la resistencia de datos, la administración de incidentes de seguridad y mucho más. Los clientes pueden usar esta información para realizar sus propias evaluaciones de riesgos normativos. Los responsables de cumplimiento normativo pueden asignar el rol "Usuario de Service Assurance" para proporcionar a los usuarios acceso a Service Assurance. El administrador de inquilinos también puede proporcionar a los usuarios externos, como auditores independientes, acceso a la información en el panel de Garantía de servicios a través del Portal de confianza del servicio en la nube (STP) de [Microsoft.](https://aka.ms/STP)

## <a name="onedrive-for-business-admin-center"></a>Centro de administración de OneDrive para la Empresa

El Centro de administración de Microsoft OneDrive le ayuda a administrar rápida y fácilmente la configuración de OneDrive para la Empresa de su organización en un solo lugar. Para usar el Centro de administración de OneDrive, se requiere acceso a onedrive.com de correo. También debe ser administrador global de su organización o administrador personalizado con el rol de administrador de SharePoint. Acceda al Centro de administración de OneDrive para la Empresa en [https://admin.onedrive.com](https://admin.onedrive.com/) .

Las características clave incluyen un área de cumplimiento que proporciona a los administradores vínculos al centro de administración adecuado para escenarios clave, como buscar en el registro de auditoría, trabajar con DLP, retención, exhibición de documentos electrónicos y alertas.

## <a name="related-links"></a>Vínculos relacionados

- [Características de informes de Microsoft 365](assurance-reporting-features.md)
- [Registro interno para la ingeniería de Microsoft 365](assurance-internal-logging.md)
