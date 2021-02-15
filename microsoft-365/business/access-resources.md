---
title: Få tilgang til lokale ressurser fra en enhet med Azure AD-tilgang i Microsoft 365 Business
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
description: Lær hvordan du får tilgang til lokale ressurser som bransjeapper, delte filressurser og skrivere fra en Windows 10-enhet som er koblet til Azure Active Directory.
ms.openlocfilehash: fc02fd30f41f25f52e653e750a6bdfd1bd7f800e
ms.sourcegitcommit: a62ac3c01ba700a51b78a647e2301f27ac437c5a
ms.translationtype: MT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2021
ms.locfileid: "50233844"
---
# <a name="access-on-premises-resources-from-an-azure-ad-joined-device-in-microsoft-365-business-premium"></a><span data-ttu-id="cf299-103">Få tilgang til lokale ressurser fra en enhet med Azure AD-tilgang i Microsoft 365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="cf299-103">Access on-premises resources from an Azure AD-joined device in Microsoft 365 Business Premium</span></span>

<span data-ttu-id="cf299-104">Denne artikkelen gjelder for Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="cf299-104">This article applies to Microsoft 365 Business Premium.</span></span>

<span data-ttu-id="cf299-105">Alle Windows 10-enheter som er med i Azure Active Directory, har tilgang til alle skybaserte ressurser, for eksempel Microsoft 365-apper, og kan beskyttes av Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="cf299-105">Any Windows 10 device that is Azure Active Directory joined has access to all cloud-based resources, such as your Microsoft 365 apps, and can be protected by Microsoft 365 Business Premium.</span></span> <span data-ttu-id="cf299-106">Du kan også gi tilgang til lokale ressurser som bransjeapper (LOB), delte filressurser og skrivere.</span><span class="sxs-lookup"><span data-stu-id="cf299-106">You can also allow access to on-premises resources like line of business (LOB) apps, file shares, and printers.</span></span> <span data-ttu-id="cf299-107">Hvis du vil tillate tilgang, [kan du bruke Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect) til å synkronisere lokal Active Directory med Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cf299-107">To allow access, use [Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect) to synchronize your on-premises Active Directory with Azure Active Directory.</span></span> 

<span data-ttu-id="cf299-108">Hvis du vil ha mer informasjon, kan du [se Innføring i enhetsbehandling i Azure Active Directory.](https://docs.microsoft.com/azure/active-directory/device-management-introduction)</span><span class="sxs-lookup"><span data-stu-id="cf299-108">To learn more, see [Introduction to device management in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).</span></span>
<span data-ttu-id="cf299-109">Trinnene oppsummeres også i avsnittene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="cf299-109">The steps are also summarized in the following sections.</span></span>
 
## <a name="run-azure-ad-connect"></a><span data-ttu-id="cf299-110">Kjør Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="cf299-110">Run Azure AD Connect</span></span>

<span data-ttu-id="cf299-111">Fullfør følgende trinn for å aktivere organisasjonens Azure AD-koblede enheter for å få tilgang til lokale ressurser.</span><span class="sxs-lookup"><span data-stu-id="cf299-111">Complete the following steps to enable your organization's Azure AD joined devices to access on-premises resources.</span></span>
  
1. <span data-ttu-id="cf299-112">Hvis du vil synkronisere brukere, grupper og kontakter fra lokal Active Directory til Azure Active Directory, kan du kjøre veiviseren for katalogsynkronisering og Azure AD Connect som beskrevet i Konfigurere katalogsynkronisering [for Office 365.](https://docs.microsoft.com/microsoft-365/enterprise/set-up-directory-synchronization)</span><span class="sxs-lookup"><span data-stu-id="cf299-112">To synchronize your users, groups, and contacts from local Active Directory into Azure Active Directory, run the Directory synchronization wizard and Azure AD Connect as described in [Set up directory synchronization for Office 365](https://docs.microsoft.com/microsoft-365/enterprise/set-up-directory-synchronization).</span></span>
    
2. <span data-ttu-id="cf299-113">Når katalogsynkroniseringen er fullført, må du kontrollere at organisasjonens Windows 10-enheter er sammenføyd med Azure AD.</span><span class="sxs-lookup"><span data-stu-id="cf299-113">After the directory synchronization is complete, make sure your organization's Windows 10 devices are Azure AD joined.</span></span> <span data-ttu-id="cf299-114">Dette trinnet gjøres enkeltvis på hver Windows 10-enhet.</span><span class="sxs-lookup"><span data-stu-id="cf299-114">This step is done individually on each Windows 10 device.</span></span> <span data-ttu-id="cf299-115">Se [Konfigurere Windows-enheter for brukere av Microsoft 365 Business Premium](set-up-windows-devices.md) for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="cf299-115">See [Set up Windows devices for Microsoft 365 Business Premium users](set-up-windows-devices.md) for details.</span></span> 
    
3. <span data-ttu-id="cf299-116">Når Windows 10-enhetene er med i Azure AD, må hver bruker starte enhetene sine på nytt og logge på med Microsoft 365 Business Premium-legitimasjonen.</span><span class="sxs-lookup"><span data-stu-id="cf299-116">Once the Windows 10 devices are Azure AD joined, each user must reboot their devices and sign in with their Microsoft 365 Business Premium credentials.</span></span> <span data-ttu-id="cf299-117">Alle enheter har nå også tilgang til lokale ressurser.</span><span class="sxs-lookup"><span data-stu-id="cf299-117">All devices now have access to on-premises resources as well.</span></span>
    
<span data-ttu-id="cf299-118">Ingen flere trinn er nødvendig for å få tilgang til lokale ressurser for Azure AD-sammenføyde enheter.</span><span class="sxs-lookup"><span data-stu-id="cf299-118">No additional steps are required to get access to on-premises resources for Azure AD joined devices.</span></span> <span data-ttu-id="cf299-119">Denne funksjonaliteten er innebygd i Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf299-119">This functionality is built into Windows 10.</span></span> 

<span data-ttu-id="cf299-120">Hvis du har planer om å logge på AADJ-enheten annet enn passordmetoden, som for eksempel PIN/metrisk bio-metrisk via pålogging for WHFB-legitimasjon og deretter få tilgang til lokale ressurser (deler, skrivere). osv.), følg https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-hybrid-aadj-sso-base</span><span class="sxs-lookup"><span data-stu-id="cf299-120">If you have plans to login to the AADJ device other than password method Like PIN/Bio-metric via WHFB credential login and then access on-premise resources (shares,printers..etc), please follow https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-hybrid-aadj-sso-base</span></span>
  
<span data-ttu-id="cf299-121">Hvis organisasjonen ikke er klar til å distribuere i den azure AD-sammenføyde enhetskonfigurasjonen som er beskrevet ovenfor, kan du vurdere å konfigurere konfigurasjon for enheten [Hybrid Azure AD Joined.](manage-windows-devices.md)</span><span class="sxs-lookup"><span data-stu-id="cf299-121">If your organization isn't ready to deploy in the Azure AD joined device configuration described above, consider setting up [Hybrid Azure AD Joined device configuration](manage-windows-devices.md).</span></span>
  
### <a name="considerations-when-you-join-windows-devices-to-azure-ad"></a><span data-ttu-id="cf299-122">Hensyn som må tas når du slår sammen Windows-enheter med Azure AD</span><span class="sxs-lookup"><span data-stu-id="cf299-122">Considerations when you join Windows devices to Azure AD</span></span>

<span data-ttu-id="cf299-123">Hvis Windows-enheten du ble med i Azure-AD sammen med, tidligere var sammenføyd med domenet eller i en arbeidsgruppe, kan du vurdere følgende begrensninger:</span><span class="sxs-lookup"><span data-stu-id="cf299-123">If the Windows device that you Azure-AD joined was previously domain-joined or in a workgroup, consider the following limitations:</span></span>
  
- <span data-ttu-id="cf299-124">Når en enhet med Azure AD blir med, opprettes en ny bruker uten å referere til en eksisterende profil.</span><span class="sxs-lookup"><span data-stu-id="cf299-124">When a device Azure AD joins, it creates a new user without referencing an existing profile.</span></span> <span data-ttu-id="cf299-125">Profiler må overføres manuelt.</span><span class="sxs-lookup"><span data-stu-id="cf299-125">Profiles must be manually migrated.</span></span> <span data-ttu-id="cf299-126">En brukerprofil inneholder informasjon som favoritter, lokale filer, nettleserinnstillinger og Start-menyinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="cf299-126">A user profile contains information like favorites, local files, browser settings, and Start menu settings.</span></span> <span data-ttu-id="cf299-127">Den beste fremgangsmåten er å finne et tredjepartsverktøy til å tilordne eksisterende filer og innstillinger til den nye profilen.</span><span class="sxs-lookup"><span data-stu-id="cf299-127">A best approach is to find a third-party tool to map existing files and settings to the new profile.</span></span>

- <span data-ttu-id="cf299-128">Hvis enheten bruker gruppepolicyobjekter, kan det hende at enkelte [](https://docs.microsoft.com/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers) gruppepolicyobjekter ikke har en tilsvarende konfigurasjonstjenesteleverandør (CSP) i Intune.</span><span class="sxs-lookup"><span data-stu-id="cf299-128">If the device is using Group Policy Objects (GPO), some GPOs may not have a comparable [Configuration Service Provider](https://docs.microsoft.com/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers) (CSP) in Intune.</span></span> <span data-ttu-id="cf299-129">Kjør [MMAT-verktøyet for](https://www.microsoft.com/download/details.aspx?id=45520) å finne sammenlignbare CSP-er for eksisterende GPO-er.</span><span class="sxs-lookup"><span data-stu-id="cf299-129">Run the [MMAT tool](https://www.microsoft.com/download/details.aspx?id=45520) to find comparable CSPs for existing GPOs.</span></span>

- <span data-ttu-id="cf299-130">Det kan hende at brukere ikke kan godkjenne til programmer som er avhengige av Active Directory-godkjenning.</span><span class="sxs-lookup"><span data-stu-id="cf299-130">Users might not be able to authenticate to applications that depend on Active Directory authentication.</span></span> <span data-ttu-id="cf299-131">Evaluer den eldre appen, og vurder om mulig å oppdatere til en app som bruker moderne godkjapp.</span><span class="sxs-lookup"><span data-stu-id="cf299-131">Evaluate the legacy app and consider updating to an app that uses modern Auth, if possible.</span></span>

- <span data-ttu-id="cf299-132">Søk etter Active Directory-skrivere vil ikke fungere.</span><span class="sxs-lookup"><span data-stu-id="cf299-132">Active Directory printer discovery won't work.</span></span> <span data-ttu-id="cf299-133">Du kan angi baner for direkte skriver for alle brukere, eller bruke [Universal Print.](https://aka.ms/UPDocs)</span><span class="sxs-lookup"><span data-stu-id="cf299-133">You can provide direct printer paths for all users or use [Universal Print](https://aka.ms/UPDocs).</span></span>
