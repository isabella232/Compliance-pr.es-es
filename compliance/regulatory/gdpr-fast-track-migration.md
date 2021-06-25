---
title: RGPD
description: 'Guía técnica de Microsoft: CONJUNTO DE HERRAMIENTAS DE MIGRACIONES DE FASTTRACK PARA ENVIAR SOLICITUDES DE ELIMINACIÓN'
keywords: Migración de FastTrack, Microsoft 365 Educación, documentación de Microsoft 365, RGPD
localization_priority: Priority
Robots: NOFOLLOW,NOINDEX
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: mohitku
author: MohitKumar
manager: laurawi
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft GDPR
hideEdit: true
ms.openlocfilehash: d3429d3fb35317146e32fddc71bae2f12c40269d
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/23/2021
ms.locfileid: "53089513"
---
# <a name="fasttrack-migration-toolset-for-submitting-delete-request"></a><span data-ttu-id="9d9f7-104">Conjunto de herramientas de migración de FastTrack para cursar solicitudes de eliminación</span><span class="sxs-lookup"><span data-stu-id="9d9f7-104">FastTrack Migration Toolset for Submitting Delete Request</span></span>

## <a name="toolset-purpose"></a><span data-ttu-id="9d9f7-105">Finalidad del conjunto de herramientas</span><span class="sxs-lookup"><span data-stu-id="9d9f7-105">Toolset purpose</span></span>

<span data-ttu-id="9d9f7-p101">Si es un cliente que actualmente está realizando una migración de FastTrack, eliminar la cuenta de usuario no hará que se elimine la copia de datos que el equipo de FastTrack de Microsoft conserva, cosa que hace con el único propósito de completar la migración. Si quiere que el equipo de Microsoft FastTrack elimine también esa copia de datos durante la migración, curse una solicitud a través de este conjunto de herramientas. En el transcurso habitual de las actividades, Microsoft FastTrack eliminará todas las copias de datos cuando la migración finalice.</span><span class="sxs-lookup"><span data-stu-id="9d9f7-p101">In the event that you are a customer currently engaged in FastTrack migrations, deleting the user account will not delete the data copy held by the Microsoft FastTrack team, which is held for the sole purpose of completing the migration. If during the migration you would like the Microsoft FastTrack team to also delete the data copy, submit a request via this tool set. In the ordinary course of business, Microsoft FastTrack will delete all data copies once the migration is complete.</span></span>

### <a name="supported-platforms"></a><span data-ttu-id="9d9f7-109">Plataformas compatibles</span><span class="sxs-lookup"><span data-stu-id="9d9f7-109">Supported platforms</span></span>

<span data-ttu-id="9d9f7-p102">Microsoft admite la versión inicial de este conjunto de herramientas en la plataforma de Windows y en la consola de PowerShell. Este conjunto de herramientas admite las siguientes plataformas conocidas:</span><span class="sxs-lookup"><span data-stu-id="9d9f7-p102">Microsoft supports the initial release of this  toolset in the Windows platform and PowerShell console. The following known platforms are supported by this toolset:</span></span>

<span data-ttu-id="9d9f7-112">\***Tabla 1: plataformas admitidas por este conjunto de herramientas** _</span><span class="sxs-lookup"><span data-stu-id="9d9f7-112">\***Table 1 — Platforms supported by this toolset** _</span></span>

<span data-ttu-id="9d9f7-113">_\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9d9f7-113">_\*\*\*</span></span>

|<span data-ttu-id="9d9f7-114">Versión de PowerShell</span><span class="sxs-lookup"><span data-stu-id="9d9f7-114">PowerShell version</span></span>|<span data-ttu-id="9d9f7-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9d9f7-115">Windows 7</span></span>|<span data-ttu-id="9d9f7-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9d9f7-116">Windows 8</span></span>|<span data-ttu-id="9d9f7-117">Windows 10</span><span class="sxs-lookup"><span data-stu-id="9d9f7-117">Windows 10</span></span>|<span data-ttu-id="9d9f7-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9d9f7-118">Windows Server 2012</span></span>|<span data-ttu-id="9d9f7-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9d9f7-119">Windows Server 2016</span></span>|
|:---:|:---:|:---:|:---:|:---:|:---:|
|<span data-ttu-id="9d9f7-120">5.0</span><span class="sxs-lookup"><span data-stu-id="9d9f7-120">5.0</span></span>|<span data-ttu-id="9d9f7-121">No compatible</span><span class="sxs-lookup"><span data-stu-id="9d9f7-121">Not Supported</span></span>|<span data-ttu-id="9d9f7-122">Compatible</span><span class="sxs-lookup"><span data-stu-id="9d9f7-122">Supported</span></span>|<span data-ttu-id="9d9f7-123">Compatible</span><span class="sxs-lookup"><span data-stu-id="9d9f7-123">Supported</span></span>|<span data-ttu-id="9d9f7-124">Compatible</span><span class="sxs-lookup"><span data-stu-id="9d9f7-124">Supported</span></span>|<span data-ttu-id="9d9f7-125">Compatible</span><span class="sxs-lookup"><span data-stu-id="9d9f7-125">Supported</span></span>|
|<span data-ttu-id="9d9f7-126">5.1</span><span class="sxs-lookup"><span data-stu-id="9d9f7-126">5.1</span></span>|<span data-ttu-id="9d9f7-127">No compatible</span><span class="sxs-lookup"><span data-stu-id="9d9f7-127">Not Supported</span></span>|<span data-ttu-id="9d9f7-128">Compatible</span><span class="sxs-lookup"><span data-stu-id="9d9f7-128">Supported</span></span>|<span data-ttu-id="9d9f7-129">Compatible</span><span class="sxs-lookup"><span data-stu-id="9d9f7-129">Supported</span></span>|<span data-ttu-id="9d9f7-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="9d9f7-130">Supported</span></span>|<span data-ttu-id="9d9f7-131">Compatible.</span><span class="sxs-lookup"><span data-stu-id="9d9f7-131">Supported</span></span>|
|

### <a name="obtaining-the-toolset"></a><span data-ttu-id="9d9f7-132">Obtener el conjunto de herramientas</span><span class="sxs-lookup"><span data-stu-id="9d9f7-132">Obtaining the toolset</span></span>

<span data-ttu-id="9d9f7-p103">Este conjunto de herramientas está disponible en la Galería de PowerShell de la aplicación de consola de PowerShell. Para encontrar y cargar este módulo de cmdlet, abra primero PowerShell en el modo de administrador para, así, contar con los permisos adecuados para instalar el módulo. Si no ha usado PowerShell anteriormente, vaya a la barra de tareas de Windows y, en el cuadro de búsqueda, escriba "PowerShell". Seleccione la aplicación de consola haciendo clic con el botón derecho, elija **Ejecutar como administrador** y haga clic en **Sí** para ejecutar Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d9f7-p103">This toolset is available in the PowerShell Gallery on the PowerShell console application.  To locate and load this cmdlet module, first open PowerShell in administrator mode so it has the appropriate permissions to install the module. If you have not used PowerShell previously go to your Windows Task Bar and in the search box type 'PowerShell”. Select the console app using right-click and choose **Run as administrator**, then click **Yes** to run Windows PowerShell.</span></span>

![PowerShell: ejecutar como administrador](../media/fasttrack-powershell_image.png)

![PowerShell: permitir que la aplicación haga cambios](../media/fasttrack-run-powershell_image.png)

<span data-ttu-id="9d9f7-p104">Con la consola ya abierta, es necesario configurar los permisos que permitan ejecutar scripts. Para ello, escriba el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="9d9f7-p104">Now that the console is open, you need to set permissions for script execution. Type the following command to allow the scripts to run:</span></span>

```powershell
Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process
```

<span data-ttu-id="9d9f7-141">Se le pedirá que confirme esta acción, dado que el administrador puede cambiar el ámbito a su conveniencia.</span><span class="sxs-lookup"><span data-stu-id="9d9f7-141">You will be prompted to confirm this action, as the administrator can change the scope at their discretion.</span></span>

<span data-ttu-id="9d9f7-142">\**_Definir la directiva de ejecución_* _</span><span class="sxs-lookup"><span data-stu-id="9d9f7-142">\**_Set Execution Policy_* _</span></span>

![Cambio de establecimiento de la directiva de ejecución en PowerShell](../media/powershell-set-execution-policy_image.png)

<span data-ttu-id="9d9f7-144">Ahora que la consola está configurada para permitir la ejecución de scripts, ejecute el siguiente comando para instalar el módulo:</span><span class="sxs-lookup"><span data-stu-id="9d9f7-144">Now that the console is set to allow the script, run this next command to install the module:</span></span>

```powershell
Install-Module -Name Microsoft.FastTrack -Repository PSGallery -WarningAction SilentlyContinue -Force
```

### <a name="prerequisites-for-module"></a><span data-ttu-id="9d9f7-145">Requisitos previos del módulo</span><span class="sxs-lookup"><span data-stu-id="9d9f7-145">Prerequisites for module</span></span>

<span data-ttu-id="9d9f7-p105">Para ejecutar correctamente este módulo, puede que sea necesario instalar módulos dependientes para usarlos si aún no están instalados. Posiblemente deba reiniciar PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d9f7-p105">To successfully execute this module, you may need to install dependent modules for use if they are not already installed. You may need to restart PowerShell.</span></span>

<span data-ttu-id="9d9f7-p106">Para enviar una solicitud de interesado, antes tiene que iniciar sesión con sus credenciales de Office 365. Cuando especifique las credenciales apropiadas, se validará el estado de su cuenta de administrador global y se recopilará información del espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="9d9f7-p106">In order to submit a DSR, you must first log in using your Office 365 credentials. Entering the proper credentials will validate your global administrator status and collect tenant information.</span></span>

```powershell
Login-FastTrackAccount -ApiKey <API Key provided by FastTrack MVM>
```

<span data-ttu-id="9d9f7-150">Tras haber iniciado sesión correctamente, la clave y las credenciales se almacenarán para su uso con módulos FastTrack durante lo que quede de la sesión actual de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d9f7-150">Once successfully logged in, the credentials and key will be stored for use with FastTrack modules for the remainder of the current PowerShell session.</span></span>

<span data-ttu-id="9d9f7-151">Si necesita conectarse a un entorno de nube que no sea comercial, deberá agregar _-Environment\* al comando de *Inicio de sesión* con uno de los siguientes entornos válidos:</span><span class="sxs-lookup"><span data-stu-id="9d9f7-151">If you need to connect to a cloud environment, other than commercial, _-Environment\* will need to be added to *Log in* command with one of the following valid environments:</span></span>

- <span data-ttu-id="9d9f7-152">AzureCloud</span><span class="sxs-lookup"><span data-stu-id="9d9f7-152">AzureCloud</span></span>
- <span data-ttu-id="9d9f7-153">AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="9d9f7-153">AzureChinaCloud</span></span>
- <span data-ttu-id="9d9f7-154">AzureGermanCloud</span><span class="sxs-lookup"><span data-stu-id="9d9f7-154">AzureGermanCloud</span></span>
- <span data-ttu-id="9d9f7-155">AzureUSGovernmentCloud</span><span class="sxs-lookup"><span data-stu-id="9d9f7-155">AzureUSGovernmentCloud</span></span>

```powershell
Login-FastTrackAccount -ApiKey <API Key provided by FastTrack MVM> -Environment <cloud environment>
```

<span data-ttu-id="9d9f7-156">Para enviar una solicitud DSR, ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="9d9f7-156">To submit a DSR request, run the following command:</span></span>

```powershell
Submit-FastTrackGdprDsrRequest -DsrRequestUserEmail SubjectUserEmail@mycompany.com
```

<span data-ttu-id="9d9f7-p107">Si el cmdlet se ejecuta correctamente, devolverá un objeto de Id. de transacción. Guárdelo.</span><span class="sxs-lookup"><span data-stu-id="9d9f7-p107">On success, the cmdlet will return a Transaction ID object. Please retain the Transaction ID.</span></span>

#### <a name="checking-the-status-of-a-request-transaction"></a><span data-ttu-id="9d9f7-159">Comprobar el estado de una transacción de solicitud</span><span class="sxs-lookup"><span data-stu-id="9d9f7-159">Checking the status of a request transaction</span></span>

<span data-ttu-id="9d9f7-160">Ejecute la siguiente función con el Id. de la transacción que consiguió previamente:</span><span class="sxs-lookup"><span data-stu-id="9d9f7-160">Run the following function using the previously obtained Transaction ID:</span></span>

```powershell
Get-FastTrackGdprDsrRequest -TransactionID "YourTransactionID"
```

#### <a name="transaction-status-codes"></a><span data-ttu-id="9d9f7-161">Códigos de estado de la transacción</span><span class="sxs-lookup"><span data-stu-id="9d9f7-161">Transaction Status Codes</span></span>

|<span data-ttu-id="9d9f7-162">Transacción</span><span class="sxs-lookup"><span data-stu-id="9d9f7-162">Transaction</span></span>|<span data-ttu-id="9d9f7-163">Estado</span><span class="sxs-lookup"><span data-stu-id="9d9f7-163">Status</span></span>|
|---|---|
|<span data-ttu-id="9d9f7-164">**Created**</span><span class="sxs-lookup"><span data-stu-id="9d9f7-164">**Created**</span></span>|<span data-ttu-id="9d9f7-165">La solicitud se ha creado.</span><span class="sxs-lookup"><span data-stu-id="9d9f7-165">Request has been created.</span></span>|
|<span data-ttu-id="9d9f7-166">**Failed**</span><span class="sxs-lookup"><span data-stu-id="9d9f7-166">**Failed**</span></span>|<span data-ttu-id="9d9f7-167">La solicitud no se ha podido crear. Vuelva a enviarla o póngase en contacto con el equipo de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="9d9f7-167">Request failed to create, please resubmit, or contact support.</span></span>|
|<span data-ttu-id="9d9f7-168">**Completed**</span><span class="sxs-lookup"><span data-stu-id="9d9f7-168">**Completed**</span></span>|<span data-ttu-id="9d9f7-169">La solicitud se ha completado y saneado.</span><span class="sxs-lookup"><span data-stu-id="9d9f7-169">Request has been completed and sanitized.</span></span>|
|

<!-- original version: **Created**  Request has been created<br/>**Failed** Request failed to create, please resubmit, or contact support<br/>**Completed** Request has been completed and sanitized -->

## <a name="learn-more"></a><span data-ttu-id="9d9f7-170">Obtén más información</span><span class="sxs-lookup"><span data-stu-id="9d9f7-170">Learn more</span></span>

[<span data-ttu-id="9d9f7-171">Centro de confianza de Microsoft</span><span class="sxs-lookup"><span data-stu-id="9d9f7-171">Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
