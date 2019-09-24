---
title: Automatisk installere eller avinstallere Office på Windows 10-enheter
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
ms.assetid: cbc6bfe5-565a-4fb8-95f0-b06e7b74ac46
description: 'Installer eller Avinstaller Office på Windows 10-enheter fra Microsoft 365 Business administrasjonssenteret. '
ms.openlocfilehash: 70fd2f1ded87e04f506b1ba415c820af5d535938
ms.sourcegitcommit: 7690c8bfdea6e6d245cfa7c5b09b913b092cde0a
ms.translationtype: MT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2019
ms.locfileid: "37121262"
---
# <a name="automatically-install-or-uninstall-office-on-windows-10-devices"></a><span data-ttu-id="7d102-103">Automatisk installere eller avinstallere Office på Windows 10-enheter</span><span class="sxs-lookup"><span data-stu-id="7d102-103">Automatically install or uninstall Office on Windows 10 devices</span></span>

<span data-ttu-id="7d102-104">[![Label å fortelle deg at Administrasjonssenteret er i endring, og du kan finne mer informasjon på aka.ms/aboutM365preview.](media/m365admincenterchanging.png)](https://docs.microsoft.com/office365/admin/microsoft-365-admin-center-preview)</span><span class="sxs-lookup"><span data-stu-id="7d102-104">[![Label to let you know the admin center is changing and you can find more details at aka.ms/aboutM365preview.](media/m365admincenterchanging.png)](https://docs.microsoft.com/office365/admin/microsoft-365-admin-center-preview)</span></span>

<span data-ttu-id="7d102-105">Du kan raskt og enkelt installere Office på Windows 10 PC-er fra Microsoft 365 Business-administrasjonssenteret.</span><span class="sxs-lookup"><span data-stu-id="7d102-105">You can quickly and easily install Office to Windows 10 PCs from the Microsoft 365 Business admin center.</span></span>
  
<span data-ttu-id="7d102-106">Hvis du vil forstå hvordan dette fungerer med tidligere installerte Office-apper, kan du lese [Klargjøre for installasjon av Office-klienten](prepare-for-office-client-deployment.md) før du begynner.</span><span class="sxs-lookup"><span data-stu-id="7d102-106">To understand how this works with previously installed Office apps, read [Prepare for Office client installation](prepare-for-office-client-deployment.md) before you get started.</span></span> 
  
## <a name="manage-office-deployments"></a><span data-ttu-id="7d102-107">Behandle Office-distribusjoner</span><span class="sxs-lookup"><span data-stu-id="7d102-107">Manage Office deployments</span></span>

1. <span data-ttu-id="7d102-108">Logg deg på [administrasjonssenteret](https://aka.ms/bcsportal) med global administratorlegitimasjon.</span><span class="sxs-lookup"><span data-stu-id="7d102-108">Sign in to the [admin center](https://aka.ms/bcsportal) with global admin credentials.</span></span> 
    
2. <span data-ttu-id="7d102-109">Velg **Behandle Office-distribusjon** på **Enhets**-kortet.</span><span class="sxs-lookup"><span data-stu-id="7d102-109">On the **Devices** card, choose **Manage Office Deployment**.</span></span>
      <span data-ttu-id="7d102-110">Hvis du ikke ser **enhets handlings** kortet på **Starts** IDen i administrasjonssenteret, klikker du på **Legg** til (+) for å legge det til i administrator hjemmet.</span><span class="sxs-lookup"><span data-stu-id="7d102-110">If you do not see the **Device actions** card, in the admin center **Home** page, click **Add** (+) to add it to your admin home.</span></span>
    
    ![Screenshot of the Devices card in the admin center](media/9982e784-dbf9-4a76-a159-bb3e2e5aa23f.png)
  
3. <span data-ttu-id="7d102-112">Velg **Legg til en gruppe** på **Behandle Office-distribusjon**-ruten, og velg gruppen du ønsker å bruke.</span><span class="sxs-lookup"><span data-stu-id="7d102-112">On the **Manage Office deployment** pane that opens, choose **Add a group**, then select the groups you want use.</span></span>
    
4. <span data-ttu-id="7d102-113">Når du har lagt til gruppen eller gruppene du vil bruke, fra **Distribusjonshandling**-rullegardinet, velger du enten **Installere Office så snart som mulig** eller **Avinstallere Office**.</span><span class="sxs-lookup"><span data-stu-id="7d102-113">After you have added the group or groups you want to use, from the **Deployment Action** drop-down, select either **Install Office as soon as possible** or **Uninstall Office**.</span></span>
    
    ![In the Manage Office deployment pane, choose either Install Office as soon as possible, or Uninstall Office.](media/00f24a61-1848-40c0-b037-78d726c7d757.png)
  
5. <span data-ttu-id="7d102-115">Velg **Neste** \> se gjennom innstillingene, og velg deretter **Bekreft**.</span><span class="sxs-lookup"><span data-stu-id="7d102-115">Choose **Next** \> review the settings and then choose **Confirm**.</span></span>
    
<span data-ttu-id="7d102-116">En 32-bitersversjon av Office installeres eller avinstalleres automatisk i de enhetene som eies av brukere som er angitt av gruppen, eller grupper du har brukt.</span><span class="sxs-lookup"><span data-stu-id="7d102-116">A 32-bit Office will be automatically installed, or uninstalled in the devices owned by users specified by the group or groups you used.</span></span>
  
<span data-ttu-id="7d102-117">Hvis du ønsker å bekrefte, kan du åpne oppgavebehandling på en datamaskin som ble valgt for en Office-installasjon og se etter Microsoft Office klikk og bruk-prosessen.</span><span class="sxs-lookup"><span data-stu-id="7d102-117">To verify you can open the Task Manager on a computer that was selected for an Office install and look for Microsoft Office Click-to-Run process.</span></span>
  


