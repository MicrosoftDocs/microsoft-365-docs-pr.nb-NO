---
title: Få tilgang til lokale ressurser fra en Azure AD-tilknyttet enhet i Microsoft 365 Business
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
ms.collection: M365-subscription-management
localization_priority: Normal
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
ms.assetid: b0f4d010-9fd1-44d0-9d20-fabad2cdbab5
description: Lær hvordan du får tilgang til lokale ressurser, for eksempel bransje programmer, delte fil ressurser og skrivere fra en Azure Active Directory-enhet som er koblet til Windows 10.
ms.openlocfilehash: 2144268f5cbab67c39d5902622c61c0c35e6481c
ms.sourcegitcommit: 15be7822220041c25fc52565f1c64d252e442d89
ms.translationtype: MT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "48295314"
---
# <a name="access-on-premises-resources-from-an-azure-ad-joined-device-in-microsoft-365-business-premium"></a><span data-ttu-id="00df6-103">Få tilgang til lokale ressurser fra en Azure AD-tilknyttet enhet i Microsoft 365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="00df6-103">Access on-premises resources from an Azure AD-joined device in Microsoft 365 Business Premium</span></span>

<span data-ttu-id="00df6-104">Denne artikkelen gjelder for Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="00df6-104">This article applies to Microsoft 365 Business Premium.</span></span>

<span data-ttu-id="00df6-105">Alle Windows 10-enheter som er koblet til Azure Active Directory, har tilgang til alle Sky BAS ert ressurser, for eksempel Microsoft 365-appene, og kan beskyttes av Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="00df6-105">Any Windows 10 device that is Azure Active Directory joined has access to all cloud-based resources, such as your Microsoft 365 apps, and can be protected by Microsoft 365 Business Premium.</span></span> <span data-ttu-id="00df6-106">Du kan også tillate tilgang til lokale ressurser, for eksempel bransje programmer (LOB), delte fil ressurser og skrivere.</span><span class="sxs-lookup"><span data-stu-id="00df6-106">You can also allow access to on-premises resources like line of business (LOB) apps, file shares, and printers.</span></span> <span data-ttu-id="00df6-107">Hvis du vil tillate tilgang, bruker du [Azure ad Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect) til å synkronisere den lokale Active Directory-katalogen med Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="00df6-107">To allow access, use [Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect) to synchronize your on-premises Active Directory with Azure Active Directory.</span></span> 

<span data-ttu-id="00df6-108">Hvis du vil ha mer informasjon, kan du se [innføring i enhets behandling i Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).</span><span class="sxs-lookup"><span data-stu-id="00df6-108">To learn more, see [Introduction to device management in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).</span></span>
<span data-ttu-id="00df6-109">Fremgangs måten er også oppsummert i de følgende avsnittene.</span><span class="sxs-lookup"><span data-stu-id="00df6-109">The steps are also summarized in the following sections.</span></span>
 
## <a name="run-azure-ad-connect"></a><span data-ttu-id="00df6-110">Kjøre Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="00df6-110">Run Azure AD Connect</span></span>

<span data-ttu-id="00df6-111">Følg Fremgangs måten nedenfor for å aktivere organisasjonens Azure AD-tilknyttede enheter for å få tilgang til lokale ressurser.</span><span class="sxs-lookup"><span data-stu-id="00df6-111">Complete the following steps to enable your organization's Azure AD joined devices to access on-premises resources.</span></span>
  
1. <span data-ttu-id="00df6-112">Hvis du vil synkronisere brukere, grupper og kontakter fra lokal Active Directory til Azure Active Directory, kan du kjøre vei viseren for katalog synkronisering og Azure AD Connect som beskrevet i [konfigurere katalog synkronisering for Office 365](https://docs.microsoft.com/microsoft-365/enterprise/set-up-directory-synchronization).</span><span class="sxs-lookup"><span data-stu-id="00df6-112">To synchronize your users, groups, and contacts from local Active Directory into Azure Active Directory, run the Directory synchronization wizard and Azure AD Connect as described in [Set up directory synchronization for Office 365](https://docs.microsoft.com/microsoft-365/enterprise/set-up-directory-synchronization).</span></span>
    
2. <span data-ttu-id="00df6-113">Når katalog synkroniseringen er fullført, må du kontrollere at organisasjonens Windows 10-enheter er Azure-AD-koblet.</span><span class="sxs-lookup"><span data-stu-id="00df6-113">After the directory synchronization is complete, make sure your organization's Windows 10 devices are Azure AD joined.</span></span> <span data-ttu-id="00df6-114">Dette trinnet gjøres individuelt på hver Windows 10-enhet.</span><span class="sxs-lookup"><span data-stu-id="00df6-114">This step is done individually on each Windows 10 device.</span></span> <span data-ttu-id="00df6-115">Se [konfigurere Windows-enheter for Microsoft 365 Business Premium-brukere](set-up-windows-devices.md) hvis du vil ha mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="00df6-115">See [Set up Windows devices for Microsoft 365 Business Premium users](set-up-windows-devices.md) for details.</span></span> 
    
3. <span data-ttu-id="00df6-116">Når Windows 10-enhetene er Azure-AD-koblet, må hver bruker starte enhetene sine og logge på med Microsoft 365 Business Premium-legitimasjonen.</span><span class="sxs-lookup"><span data-stu-id="00df6-116">Once the Windows 10 devices are Azure AD joined, each user must reboot their devices and sign in with their Microsoft 365 Business Premium credentials.</span></span> <span data-ttu-id="00df6-117">Alle enheter har nå tilgang til lokale ressurser også.</span><span class="sxs-lookup"><span data-stu-id="00df6-117">All devices now have access to on-premises resources as well.</span></span>
    
<span data-ttu-id="00df6-118">Ingen flere trinn kreves for å få tilgang til lokale ressurser for Azure AD-tilknyttede enheter.</span><span class="sxs-lookup"><span data-stu-id="00df6-118">No additional steps are required to get access to on-premises resources for Azure AD joined devices.</span></span> <span data-ttu-id="00df6-119">Denne funksjonen er innebygd i Windows 10.</span><span class="sxs-lookup"><span data-stu-id="00df6-119">This functionality is built into Windows 10.</span></span> 

<span data-ttu-id="00df6-120">Hvis du har planer om å logge på en annen AADJ-enhet enn passord metode, for eksempel PIN/bio-metrikk via WHFB legitimasjons pålogging og deretter få tilgang til lokale ressurser (aksjer, skrivere.. så videre), kom i gang https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-hybrid-aadj-sso-base</span><span class="sxs-lookup"><span data-stu-id="00df6-120">If you have plans to login to the AADJ device other than password method Like PIN/Bio-metric via WHFB credential login and then access on-premise resources (shares,printers..etc), please follow https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-hybrid-aadj-sso-base</span></span>
  
<span data-ttu-id="00df6-121">Hvis organisasjonen ikke er klar til å distribuere i den Azure-AD-tilknyttede enhets konfigurasjonen som er beskrevet ovenfor, kan du vurdere å konfigurere [hybrid Azure ad-tilkoblet enhets konfigurasjon](manage-windows-devices.md).</span><span class="sxs-lookup"><span data-stu-id="00df6-121">If your organization isn't ready to deploy in the Azure AD joined device configuration described above, consider setting up [Hybrid Azure AD Joined device configuration](manage-windows-devices.md).</span></span>
  
### <a name="considerations-when-you-join-windows-devices-to-azure-ad"></a><span data-ttu-id="00df6-122">Betraktninger når du blir med i Windows-enheter til Azure AD</span><span class="sxs-lookup"><span data-stu-id="00df6-122">Considerations when you join Windows devices to Azure AD</span></span>

<span data-ttu-id="00df6-123">Hvis Windows-enheten du har koblet til Azure-AD, tidligere ble domene tilknyttet eller i en arbeids gruppe, bør du vurdere følgende begrensninger:</span><span class="sxs-lookup"><span data-stu-id="00df6-123">If the Windows device that you Azure-AD joined was previously domain-joined or in a workgroup, consider the following limitations:</span></span>
  
- <span data-ttu-id="00df6-124">Når en enhet Azure AD kobles sammen, oppretter den en ny bruker uten å referere til en eksisterende profil.</span><span class="sxs-lookup"><span data-stu-id="00df6-124">When a device Azure AD joins, it creates a new user without referencing an existing profile.</span></span> <span data-ttu-id="00df6-125">Profiler må overføres manuelt.</span><span class="sxs-lookup"><span data-stu-id="00df6-125">Profiles must be manually migrated.</span></span> <span data-ttu-id="00df6-126">En bruker profil inneholder informasjon som favoritter, lokale filer, nett leser innstillinger og innstillinger for Start-menyen.</span><span class="sxs-lookup"><span data-stu-id="00df6-126">A user profile contains information like favorites, local files, browser settings, and Start menu settings.</span></span> <span data-ttu-id="00df6-127">En beste Fremgangs måte er å finne et tredje parts verktøy for å tilordne eksisterende filer og innstillinger til den nye profilen.</span><span class="sxs-lookup"><span data-stu-id="00df6-127">A best approach is to find a third-party tool to map existing files and settings to the new profile.</span></span>

- <span data-ttu-id="00df6-128">Hvis enheten bruker gruppe policy objekter (GPO), kan det hende at enkelte GPOer ikke har en leverandør av tilsvarende [konfigurasjons tjeneste](https://docs.microsoft.com/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers) (CSP) i Intune.</span><span class="sxs-lookup"><span data-stu-id="00df6-128">If the device is using Group Policy Objects (GPO), some GPOs may not have a comparable [Configuration Service Provider](https://docs.microsoft.com/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers) (CSP) in Intune.</span></span> <span data-ttu-id="00df6-129">Kjør [MMAT-verktøyet](https://www.microsoft.com/download/details.aspx?id=45520) for å finne sammenlignbare CSPer for eksisterende GPOer.</span><span class="sxs-lookup"><span data-stu-id="00df6-129">Run the [MMAT tool](https://www.microsoft.com/download/details.aspx?id=45520) to find comparable CSPs for existing GPOs.</span></span>

- <span data-ttu-id="00df6-130">Brukere kan ikke godkjenne seg for programmer som er avhengige av Active Directory-godkjenning.</span><span class="sxs-lookup"><span data-stu-id="00df6-130">Users won't be able to authenticate to applications that depend on Active Directory authentication.</span></span> <span data-ttu-id="00df6-131">Evaluer den eldre appen, og Vurder å oppdatere til en app som bruker moderne godkjenning, hvis mulig.</span><span class="sxs-lookup"><span data-stu-id="00df6-131">Evaluate the legacy app and consider updating to an app that uses modern Auth, if possible.</span></span>

- <span data-ttu-id="00df6-132">Søk i Active Directory-skriveren vil ikke fungere.</span><span class="sxs-lookup"><span data-stu-id="00df6-132">Active Directory printer discovery won't work.</span></span> <span data-ttu-id="00df6-133">Du kan angi direkte filbaner for alle brukere eller bruke [hybrid Sky utskrifter](https://docs.microsoft.com/windows-server/administration/hybrid-cloud-print/hybrid-cloud-print-deploy).</span><span class="sxs-lookup"><span data-stu-id="00df6-133">You can provide direct printer paths for all users or use [Hybrid Cloud Print](https://docs.microsoft.com/windows-server/administration/hybrid-cloud-print/hybrid-cloud-print-deploy).</span></span>
