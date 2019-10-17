---
title: Validere innstillingene for appbeskyttelse på Windows 10-datamaskiner
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
- M365-identity-device-management
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
search.appverid:
- BCS160
- MET150
ms.assetid: fae8819d-7235-495f-9f07-d016f545887f
description: Lær hvordan du validerer innstillinger for Microsoft 365 for Business-app i Windows 10-enheter.
ms.openlocfilehash: 5fed2278856f40233b142d3c7c4bc623e3777799
ms.sourcegitcommit: bd52f7b662887f552f90c46f69d6a2a42fb66914
ms.translationtype: MT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/17/2019
ms.locfileid: "37575472"
---
# <a name="validate-device-protection-settings-on-windows-10-pcs"></a><span data-ttu-id="5b38b-103">Validere innstillinger for enhetsbeskyttelse på Windows 10-PCer</span><span class="sxs-lookup"><span data-stu-id="5b38b-103">Validate device protection settings on Windows 10 PCs</span></span>

## <a name="verify-that-windows-10-device-policies-are-set"></a><span data-ttu-id="5b38b-104">Kontroller at enhets policyene for Windows 10 er angitt</span><span class="sxs-lookup"><span data-stu-id="5b38b-104">Verify that Windows 10 device policies are set</span></span>

<span data-ttu-id="5b38b-105">Når du har [konfigurert retningslinjer for enheter](protection-settings-for-windows-10-pcs.md), kan det ta noen timer for policyen å tre i kraft på brukernes enheter.</span><span class="sxs-lookup"><span data-stu-id="5b38b-105">After you [set up devices policies](protection-settings-for-windows-10-pcs.md), it may take up to a few hours for the policy to take effect on users' devices.</span></span> <span data-ttu-id="5b38b-106">Du kan bekrefte at policyene trer i kraft ved å se på forskjellige Windows Settings-skjermer på brukernes enheter.</span><span class="sxs-lookup"><span data-stu-id="5b38b-106">You can confirm that the policies took effect by looking at various Windows Settings screens on the users' devices.</span></span> <span data-ttu-id="5b38b-107">Fordi det brukernes wont ' være i stand til endre det Vinduer oppdatere og Vinduer Forsvare antivirus innfatningene opp på deres Vinduer 10 anordninger, en masse dem valgmulighetene ville være grå ut.</span><span class="sxs-lookup"><span data-stu-id="5b38b-107">Because the users won't be able to modify the Windows Update and Windows Defender Antivirus settings on their Windows 10 devices, a lot of those options will be greyed out.</span></span>
  
1. <span data-ttu-id="5b38b-108">Gå til **innfatningene** \> **oppdatere &amp; garanti** \> **Vinduer oppdatere** \> **hvile valgmulighetene** og anerkjenne det alle innfatningene er grå ut.</span><span class="sxs-lookup"><span data-stu-id="5b38b-108">Go to **Settings** \> **Update &amp; security** \> **Windows Update** \> **Restart options** and confirm that all settings are greyed out.</span></span> 
    
    ![Alle hvile valgmulighetene er grå ut.](media/31308da9-18b0-47c5-bbf6-d5fa6747c376.png)
  
2. <span data-ttu-id="5b38b-110">Gå til **innfatningene** \> **oppdatere &amp; garanti** \> **Vinduer oppdatere** \> **Avansert Valgmulighetene** og anerkjenne det alle innfatningene er grå ut.</span><span class="sxs-lookup"><span data-stu-id="5b38b-110">Go to **Settings** \> **Update &amp; security** \> **Windows Update** \> **Advanced options** and confirm that all settings are greyed out.</span></span> 
    
    ![Vinduer avansert oppdaterer valgmulighetene er alle grå ut.](media/049cf281-d503-4be9-898b-c0a3286c7fc2.png)
  
3. <span data-ttu-id="5b38b-112">Gå til **Innstillinger** \> **Oppdater &amp; sikkerhet** \> **Windows Update** \> **Avanserte alternativer** \> **Velg hvordan oppdateringer skal leveres**.</span><span class="sxs-lookup"><span data-stu-id="5b38b-112">Go to **Settings** \> **Update &amp; security** \> **Windows Update** \> **Advanced options** \> **Choose how updates are delivered**.</span></span>
    
    <span data-ttu-id="5b38b-113">Bekreft at du kan se meldingen (i rødt) at noen innstillinger er skjult eller administrert av organisasjonen, og at alle alternativene er nedtonet.</span><span class="sxs-lookup"><span data-stu-id="5b38b-113">Confirm that you can see the message (in red) that some settings are hidden or managed by your organization, and all the options are greyed out.</span></span>
    
    ![Velg hvordan oppdateringer leveres siden, angir at innstillingene er skjult eller administrert av organisasjonen.](media/6b3e37c5-da41-4afd-9983-b4f406216b59.png)
  
4. <span data-ttu-id="5b38b-115">Hvis du vil åpne Windows Defender Sikkerhetssenter, gå **til innstillinger** \> \*\* &amp; oppdatere sikkerhet\*\* \> \> **Windows Defender** Klikk **åpne Windows Defender Sikkerhetssenter** \> \*\*virus &amp; tråd \*\* \> **Innstillinger for &amp; beskyttelse virus trusselbeskyttelse**.</span><span class="sxs-lookup"><span data-stu-id="5b38b-115">To open the Windows Defender Security Center, go to **Settings** \> **Update &amp; security** \> **Windows Defender** \> click **Open Windows Defender Security Center** \> **Virus &amp; thread protection** \> **Virus &amp; threat protection settings**.</span></span> 
    
5. <span data-ttu-id="5b38b-116">Kontroller at alle alternativene er nedtonet.</span><span class="sxs-lookup"><span data-stu-id="5b38b-116">Verify that all options are greyed out.</span></span> 
    
    ![Innstillingene for virus-og trusselbeskyttelse er nedtonet.](media/9ca68d40-a5d9-49d7-92a4-c581688b5926.png)
  
## <a name="related-topics"></a><span data-ttu-id="5b38b-118">Beslektede emner</span><span class="sxs-lookup"><span data-stu-id="5b38b-118">Related Topics</span></span>

[<span data-ttu-id="5b38b-119">Microsoft 365 Business dokumentasjon og ressurser</span><span class="sxs-lookup"><span data-stu-id="5b38b-119">Microsoft 365 Business documentation and resources</span></span>](https://go.microsoft.com/fwlink/p/?linkid=853701)
  
[<span data-ttu-id="5b38b-120">Komme i gang med Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="5b38b-120">Get started with Microsoft 365 Business</span></span>](microsoft-365-business-overview.md)
  
[<span data-ttu-id="5b38b-121">Administrere Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="5b38b-121">Manage Microsoft 365 Business</span></span>](manage.md)
  
[<span data-ttu-id="5b38b-122">Angi enhetskonfigurasjoner for PC-er med Windows 10</span><span class="sxs-lookup"><span data-stu-id="5b38b-122">Set device configurations for Windows 10 PCs</span></span>](protection-settings-for-windows-10-pcs.md)
  

