---
title: Få tilgang til lokale ressurser fra en Azure AD-sammenkoblet enhet i Microsoft 365 Business
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
search.appverid:
- BCS160
- MET150
ms.assetid: b0f4d010-9fd1-44d0-9d20-fabad2cdbab5
description: Finn ut hvordan du får tilgang til lokale ressurser, for eksempel bransjeprogrammer, delte filer og skrivere fra en Azure Active Directory som er koblet til Windows 10-enheten.
ms.openlocfilehash: 89ac38f3da9cbdd3ff1a5eb33dc129d2e83521c7
ms.sourcegitcommit: 8c244b38c43dd00c4ef0102f8bed02ab36639a6b
ms.translationtype: MT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/10/2019
ms.locfileid: "39967167"
---
# <a name="access-on-premises-resources-from-an-azure-ad-joined-device-in-microsoft-365-business"></a><span data-ttu-id="d22b7-103">Få tilgang til lokale ressurser fra en Azure AD-sammenkoblet enhet i Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="d22b7-103">Access on-premises resources from an Azure AD-joined device in Microsoft 365 Business</span></span>

<span data-ttu-id="d22b7-104">Alle Windows 10-enheter som Azure Active Directory ble med i, har tilgang til alle skybaserte ressurser, for eksempel Office 365-appene dine, og kan beskyttes av Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="d22b7-104">Any Windows 10 device that is Azure Active Directory joined has access to all cloud-based resources, such as your Office 365 apps, and can be protected by Microsoft 365 Business.</span></span> <span data-ttu-id="d22b7-105">Du kan også gi tilgang til lokale ressurser som bransjeprogrammer (LOB), fildelinger og skrivere.</span><span class="sxs-lookup"><span data-stu-id="d22b7-105">You can also allow access to on-premises resources like line of business (LOB) apps, file shares, and printers.</span></span> <span data-ttu-id="d22b7-106">Hvis du vil tillate tilgang, bruker du [Azure ad-tilkobling](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect) til å synkronisere den lokale Active Directory med Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d22b7-106">To allow access, use [Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect) to synchronize your on-premises Active Directory with Azure Active Directory.</span></span> 

<span data-ttu-id="d22b7-107">Hvis du vil vite mer, kan du se [innføring i Enhetsbehandling i Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).</span><span class="sxs-lookup"><span data-stu-id="d22b7-107">To learn more, see [Introduction to device management in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).</span></span>
<span data-ttu-id="d22b7-108">Trinnene oppsummeres også i avsnittene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="d22b7-108">The steps are also summarized in the following sections.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d22b7-109">Denne fremgangsmåten gjelder bare for OAuth og NTLM.</span><span class="sxs-lookup"><span data-stu-id="d22b7-109">This procedure is only applicable to OAuth and NTLM.</span></span> <span data-ttu-id="d22b7-110">Kerberos støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="d22b7-110">Kerberos is not supported.</span></span>
 
## <a name="run-azure-ad-connect"></a><span data-ttu-id="d22b7-111">Kjør Azure AD-tilkobling</span><span class="sxs-lookup"><span data-stu-id="d22b7-111">Run Azure AD Connect</span></span>

<span data-ttu-id="d22b7-112">Fullfør fremgangsmåten nedenfor for å aktivere organisasjonens Azure AD ble enheter for å få tilgang til lokale ressurser.</span><span class="sxs-lookup"><span data-stu-id="d22b7-112">Complete the following steps to enable your organization's Azure AD joined devices to access on-premises resources.</span></span>
  
1. <span data-ttu-id="d22b7-113">Hvis du vil synkronisere brukere, grupper og kontakter fra lokal Active Directory til Azure Active Directory, kjører du veiviseren for katalogsynkronisering og koble til Azure AD som beskrevet i [Konfigurere katalogsynkronisering for Office 365](https://support.office.com/article/1b3b5318-6977-42ed-b5c7-96fa74b08846).</span><span class="sxs-lookup"><span data-stu-id="d22b7-113">To synchronize your users, groups, and contacts from local Active Directory into Azure Active Directory, run the Directory synchronization wizard and Azure AD Connect as described in [Set up directory synchronization for Office 365](https://support.office.com/article/1b3b5318-6977-42ed-b5c7-96fa74b08846).</span></span>
    
2. <span data-ttu-id="d22b7-114">Når katalogsynkroniseringen er fullført, må du kontrollere at organisasjonens Windows 10-enheter er Azure AD-tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="d22b7-114">After the directory synchronization is complete, make sure your organization's Windows 10 devices are Azure AD joined.</span></span> <span data-ttu-id="d22b7-115">Dette trinnet gjøres individuelt på hver Windows 10-enhet.</span><span class="sxs-lookup"><span data-stu-id="d22b7-115">This step is done individually on each Windows 10 device.</span></span> <span data-ttu-id="d22b7-116">Se [konfigurere Windows-enheter for Microsoft 365 Business-brukere](set-up-windows-devices.md) for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="d22b7-116">See [Set up Windows devices for Microsoft 365 Business users](set-up-windows-devices.md) for details.</span></span> 
    
3. <span data-ttu-id="d22b7-117">Når Windows 10-enhetene er Azure AD-tilknyttet, må hver bruker starte enhetene sine på nytt og logge på med Microsoft 365-legitimasjonen for bedriften.</span><span class="sxs-lookup"><span data-stu-id="d22b7-117">Once the Windows 10 devices are Azure AD joined, each user must reboot their devices and sign in with their Microsoft 365 Business credentials.</span></span> <span data-ttu-id="d22b7-118">Alle enheter har nå også tilgang til lokale ressurser.</span><span class="sxs-lookup"><span data-stu-id="d22b7-118">All devices now have access to on-premises resources as well.</span></span>
    
<span data-ttu-id="d22b7-119">Ingen flere trinn er nødvendig for å få tilgang til lokale ressurser for Azure AD koblet enheter.</span><span class="sxs-lookup"><span data-stu-id="d22b7-119">No additional steps are required to get access to on-premises resources for Azure AD joined devices.</span></span> <span data-ttu-id="d22b7-120">Denne funksjonaliteten er innebygd i Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d22b7-120">This functionality is built into Windows 10.</span></span> 

<span data-ttu-id="d22b7-121">Hvis du har planer å logikk å det AADJ apparat annet enn passord metoden like knappenål/bio-metrisk via WHFB legitimasjonen logikk og så adgang opp på-premiss ressursene (aksjer, Printer.. osv.), må du følgehttps://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-hybrid-aadj-sso-base</span><span class="sxs-lookup"><span data-stu-id="d22b7-121">If you have plans to login to the AADJ device other than password method Like PIN/Bio-metric via WHFB credential login and then access on-premise resources (shares,printers..etc), please follow https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-hybrid-aadj-sso-base</span></span>
  
<span data-ttu-id="d22b7-122">Hvis organisasjonen ikke er klar til å distribuere i Azure AD sammenkoblet enhetskonfigurasjonen som er beskrevet ovenfor, kan du vurdere å konfigurere [hybrid Azure ad sammenkoblet enhetskonfigurasjon](manage-windows-devices.md).</span><span class="sxs-lookup"><span data-stu-id="d22b7-122">If your organization isn't ready to deploy in the Azure AD joined device configuration described above, consider setting up [Hybrid Azure AD Joined device configuration](manage-windows-devices.md).</span></span>
  
### <a name="considerations-when-you-join-windows-devices-to-azure-ad"></a><span data-ttu-id="d22b7-123">Betraktninger når du blir med Windows-enheter til Azure AD</span><span class="sxs-lookup"><span data-stu-id="d22b7-123">Considerations when you join Windows devices to Azure AD</span></span>

<span data-ttu-id="d22b7-124">Hvis Windows-enheten du Azure-AD ble med i, tidligere var tilknyttet et domene eller i en arbeidsgruppe, bør du vurdere følgende begrensninger:</span><span class="sxs-lookup"><span data-stu-id="d22b7-124">If the Windows device that you Azure-AD joined was previously domain-joined or in a workgroup, consider the following limitations:</span></span>
  
- <span data-ttu-id="d22b7-125">Når en enhet Azure AD blir med, oppretter den en ny bruker uten å referere til en eksisterende profil.</span><span class="sxs-lookup"><span data-stu-id="d22b7-125">When a device Azure AD joins, it creates a new user without referencing an existing profile.</span></span> <span data-ttu-id="d22b7-126">Profiler må migreres manuelt.</span><span class="sxs-lookup"><span data-stu-id="d22b7-126">Profiles must be manually migrated.</span></span> <span data-ttu-id="d22b7-127">En brukerprofil inneholder informasjon som favoritter, lokale filer, nettleserinnstillinger og innstillinger for Start-menyen.</span><span class="sxs-lookup"><span data-stu-id="d22b7-127">A user profile contains information like favorites, local files, browser settings, and Start menu settings.</span></span> <span data-ttu-id="d22b7-128">En beste fremgangsmåte er å finne et tredjepartsverktøy for å tilordne eksisterende filer og innstillinger til den nye profilen.</span><span class="sxs-lookup"><span data-stu-id="d22b7-128">A best approach is to find a third-party tool to map existing files and settings to the new profile.</span></span>

- <span data-ttu-id="d22b7-129">Hvis enheten brukergruppe policy objekter (GPO), kan noen GPOer ikke ha en sammenlignbar [Konfigurasjonstjeneste leverandør](https://docs.microsoft.com/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers) (CSP) i Intune.</span><span class="sxs-lookup"><span data-stu-id="d22b7-129">If the device is using Group Policy Objects (GPO), some GPOs may not have a comparable [Configuration Service Provider](https://docs.microsoft.com/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers) (CSP) in Intune.</span></span> <span data-ttu-id="d22b7-130">Kjør [MMAT-verktøyet](https://www.microsoft.com/download/details.aspx?id=45520) for å finne sammenlignbare CSPer for eksisterende gruppepolicyobjekter.</span><span class="sxs-lookup"><span data-stu-id="d22b7-130">Run the [MMAT tool](https://www.microsoft.com/download/details.aspx?id=45520) to find comparable CSPs for existing GPOs.</span></span>

- <span data-ttu-id="d22b7-131">Brukere vil ikke kunne godkjenne programmer som er avhengige av Active Directory-godkjenning.</span><span class="sxs-lookup"><span data-stu-id="d22b7-131">Users won't be able to authenticate to applications that depend on Active Directory authentication.</span></span> <span data-ttu-id="d22b7-132">Evaluer arven app og vurdere å oppdatere til en app som bruker moderne Auth, hvis mulig.</span><span class="sxs-lookup"><span data-stu-id="d22b7-132">Evaluate the legacy app and consider updating to an app that uses modern Auth, if possible.</span></span>

- <span data-ttu-id="d22b7-133">Discovery for Active Directory-skriveren fungerer ikke.</span><span class="sxs-lookup"><span data-stu-id="d22b7-133">Active Directory printer discovery won't work.</span></span> <span data-ttu-id="d22b7-134">Du kan angi direkte skriver baner for alle brukere eller bruke [hybrid Cloud print](https://docs.microsoft.com/windows-server/administration/hybrid-cloud-print/hybrid-cloud-print-deploy).</span><span class="sxs-lookup"><span data-stu-id="d22b7-134">You can provide direct printer paths for all users or use [Hybrid Cloud Print](https://docs.microsoft.com/windows-server/administration/hybrid-cloud-print/hybrid-cloud-print-deploy).</span></span>
