---
title: Aktivere domene-sammenføyde Windows 10-enheter som skal administreres av Microsoft 365 for bedrifter
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
- seo-marvel-mar
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
ms.assetid: 9b4de218-f1ad-41fa-a61b-e9e8ac0cf993
description: Lær hvordan du aktiverer Microsoft 365 til å beskytte lokale Active-Directory-tilkoblede Windows 10-enheter med bare noen få trinn.
ms.openlocfilehash: 7bfe5da8701a17712fa249eac99a22b8d5a1b2d1
ms.sourcegitcommit: 2d664a95b9875f0775f0da44aca73b16a816e1c3
ms.translationtype: MT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/01/2020
ms.locfileid: "44471051"
---
# <a name="enable-domain-joined-windows-10-devices-to-be-managed-by-microsoft-365-business-premium"></a><span data-ttu-id="139d6-103">Aktivere domeneblede Windows 10-enheter som skal administreres av Microsoft 365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="139d6-103">Enable domain-joined Windows 10 devices to be managed by Microsoft 365 Business Premium</span></span>

<span data-ttu-id="139d6-104">Hvis organisasjonen bruker lokal Windows Server Active Directory, kan du konfigurere Microsoft 365 Business Premium til å beskytte Windows 10-enhetene, samtidig som du opprettholder tilgangen til lokale ressurser som krever lokal godkjenning.</span><span class="sxs-lookup"><span data-stu-id="139d6-104">If your organization uses Windows Server Active Directory on-premises, you can set up Microsoft 365 Business Premium to protect your Windows 10 devices, while still maintaining access to on-premises resources that require local authentication.</span></span>
<span data-ttu-id="139d6-105">Hvis du vil konfigurere denne beskyttelsen, kan du implementere **Hybrid Azure AD sammenføyde enheter**.</span><span class="sxs-lookup"><span data-stu-id="139d6-105">To set up this protection, you can implement **Hybrid Azure AD joined devices**.</span></span> <span data-ttu-id="139d6-106">Disse enhetene er koblet til både den lokale Active Directory og Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="139d6-106">These devices are joined to both your on-premises Active Directory and your Azure Active Directory.</span></span>

<span data-ttu-id="139d6-107">Denne videoen beskriver fremgangsmåten for hvordan du konfigurerer dette for det vanligste scenariet, som også er beskrevet i trinnene som følger.</span><span class="sxs-lookup"><span data-stu-id="139d6-107">This video describes the steps for how to set this up for the most common scenario, which is also detailed in the steps that follow.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3C9hO]
  

## <a name="1-prepare-for-directory-synchronization"></a><span data-ttu-id="139d6-108">1. Klargjør for katalogsynkronisering</span><span class="sxs-lookup"><span data-stu-id="139d6-108">1. Prepare for Directory Synchronization</span></span> 

<span data-ttu-id="139d6-109">Før du synkroniserer brukere og datamaskiner fra det lokale Active Directory-domenet, kan du se [Klargjøre for katalogsynkronisering til Office 365](https://docs.microsoft.com/office365/enterprise/prepare-for-directory-synchronization).</span><span class="sxs-lookup"><span data-stu-id="139d6-109">Before you synchronize your users and computers from the local Active Directory Domain, review [Prepare for directory synchronization to Office 365](https://docs.microsoft.com/office365/enterprise/prepare-for-directory-synchronization).</span></span> <span data-ttu-id="139d6-110">Spesielt:</span><span class="sxs-lookup"><span data-stu-id="139d6-110">In particular:</span></span>

   - <span data-ttu-id="139d6-111">Kontroller at det ikke finnes noen duplikater i katalogen for følgende attributter: **e-post**, **proxyAddresses**og **userPrincipalName**.</span><span class="sxs-lookup"><span data-stu-id="139d6-111">Make sure that no duplicates exist in your directory for the following attributes: **mail**, **proxyAddresses**, and **userPrincipalName**.</span></span> <span data-ttu-id="139d6-112">Disse verdiene må være unike, og eventuelle duplikater må fjernes.</span><span class="sxs-lookup"><span data-stu-id="139d6-112">These values must be unique and any duplicates must be removed.</span></span>
   
   - <span data-ttu-id="139d6-113">Vi anbefaler at du konfigurerer **attributtet userPrincipalName** (UPN) for hver lokal brukerkonto slik at den samsvarer med den primære e-postadressen som tilsvarer den lisensierte Microsoft 365-brukeren.</span><span class="sxs-lookup"><span data-stu-id="139d6-113">We recommend that you configure the **userPrincipalName** (UPN) attribute for each local user account to match the primary email address that corresponds to the licensed Microsoft 365 user.</span></span> <span data-ttu-id="139d6-114">For eksempel: *mary.shelley@contoso.com* i stedet for *mary@contoso.local*</span><span class="sxs-lookup"><span data-stu-id="139d6-114">For example: *mary.shelley@contoso.com* rather than *mary@contoso.local*</span></span>
   
   - <span data-ttu-id="139d6-115">Hvis Active Directory-domenet slutter i et ikke-rutbart suffiks som *.local* eller *.lan*, i stedet for et Internett-rutbart suffiks, for eksempel *.com* eller *.org*, justerer du UPN-suffikset for de lokale brukerkontoene først som beskrevet i [Klargjør et ikke-rutbart domene for katalogsynkronisering](https://docs.microsoft.com/office365/enterprise/prepare-a-non-routable-domain-for-directory-synchronization).</span><span class="sxs-lookup"><span data-stu-id="139d6-115">If the Active Directory domain ends in a non-routable suffix like *.local* or *.lan*, instead of an internet routable suffix such as *.com* or *.org*, adjust the UPN suffix of the local user accounts first as described in [Prepare a non-routable domain for directory synchronization](https://docs.microsoft.com/office365/enterprise/prepare-a-non-routable-domain-for-directory-synchronization).</span></span> 

## <a name="2-install-and-configure-azure-ad-connect"></a><span data-ttu-id="139d6-116">2. Installere og konfigurere Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="139d6-116">2. Install and configure Azure AD Connect</span></span>

<span data-ttu-id="139d6-117">Hvis du vil synkronisere brukere, grupper og kontakter fra den lokale Active Directory til Azure Active Directory, installerer du Azure Active Directory Connect og konfigurerer katalogsynkronisering.</span><span class="sxs-lookup"><span data-stu-id="139d6-117">To synchronize your users, groups, and contacts from the local Active Directory into Azure Active Directory, install Azure Active Directory Connect and set up directory synchronization.</span></span> <span data-ttu-id="139d6-118">Se [Konfigurere katalogsynkronisering for Office 365 for](https://docs.microsoft.com/office365/enterprise/set-up-directory-synchronization) å finne ut mer.</span><span class="sxs-lookup"><span data-stu-id="139d6-118">See [Set up directory synchronization for Office 365](https://docs.microsoft.com/office365/enterprise/set-up-directory-synchronization) to learn more.</span></span>

> [!NOTE]
> <span data-ttu-id="139d6-119">Fremgangsmåten er nøyaktig den samme for Microsoft 365 for bedrifter.</span><span class="sxs-lookup"><span data-stu-id="139d6-119">The steps are exactly the same for Microsoft 365 for business.</span></span> 

<span data-ttu-id="139d6-120">Når du konfigurerer alternativene for Azure AD Connect, anbefaler vi at du aktiverer **synkronisering av passord**, **sømløs enkel pålogging**og funksjonen for **tilbakeskriving** av passord, som også støttes i Microsoft 365 for bedrifter.</span><span class="sxs-lookup"><span data-stu-id="139d6-120">As you configure your options for Azure AD Connect, we recommend that you enable **Password Synchronization**, **Seamless Single Sign-On**, and the **password writeback** feature, which is also supported in Microsoft 365 for business.</span></span>

> [!NOTE]
> <span data-ttu-id="139d6-121">Det er noen flere trinn for passord writeback utover avmerkingsboksen i Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="139d6-121">There are some additional steps for password writeback beyond the check box in Azure AD Connect.</span></span> <span data-ttu-id="139d6-122">Hvis du vil ha mer informasjon, kan du se [Slik gjør du det: konfigurere passord writeback](https://docs.microsoft.com/azure/active-directory/authentication/howto-sspr-writeback).</span><span class="sxs-lookup"><span data-stu-id="139d6-122">For more information, see [How-to: configure password writeback](https://docs.microsoft.com/azure/active-directory/authentication/howto-sspr-writeback).</span></span> 

## <a name="3-configure-hybrid-azure-ad-join"></a><span data-ttu-id="139d6-123">3. Konfigurer Hybrid Azure AD-sammenføyning</span><span class="sxs-lookup"><span data-stu-id="139d6-123">3. Configure Hybrid Azure AD Join</span></span>

<span data-ttu-id="139d6-124">Før du aktiverer At Windows 10-enheter skal være Hybrid Azure AD koblet til, må du kontrollere at du oppfyller følgende forutsetninger:</span><span class="sxs-lookup"><span data-stu-id="139d6-124">Before you enable Windows 10 devices to be Hybrid Azure AD joined, make sure that you meet the following prerequisites:</span></span>

   - <span data-ttu-id="139d6-125">Du kjører den nyeste versjonen av Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="139d6-125">You're running the latest version of Azure AD Connect.</span></span>

   - <span data-ttu-id="139d6-126">Azure AD connect har synkronisert alle datamaskinobjektene til enhetene du vil være hybrid Azure AD som er koblet sammen.</span><span class="sxs-lookup"><span data-stu-id="139d6-126">Azure AD connect has synchronized all the computer objects of the devices you want to be hybrid Azure AD joined.</span></span> <span data-ttu-id="139d6-127">Hvis datamaskinobjektene tilhører bestemte organisasjonsenheter (OU), må du kontrollere at disse OUene er angitt for synkronisering i Azure AD-tilkobling også.</span><span class="sxs-lookup"><span data-stu-id="139d6-127">If the computer objects belong to specific organizational units (OU), then make sure these OUs are set for synchronization in Azure AD connect as well.</span></span>

<span data-ttu-id="139d6-128">Hvis du vil registrere eksisterende domenetilknyttede Windows 10-enheter som Hybrid Azure AD ble med, følger du fremgangsmåten i [opplæringen: Konfigurere hybrid Azure Active Directory-sammenføyning for administrerte domener](https://docs.microsoft.com/azure/active-directory/devices/hybrid-azuread-join-managed-domains#configure-hybrid-azure-ad-join).</span><span class="sxs-lookup"><span data-stu-id="139d6-128">To register existing domain-joined Windows 10 devices as Hybrid Azure AD joined, follow the steps in the [Tutorial: Configure hybrid Azure Active Directory join for managed domains](https://docs.microsoft.com/azure/active-directory/devices/hybrid-azuread-join-managed-domains#configure-hybrid-azure-ad-join).</span></span> <span data-ttu-id="139d6-129">Denne hybrid-aktiverer eksisterende lokale Active Directory sammenføyde Windows 10-datamaskiner og gjør dem skyklare.</span><span class="sxs-lookup"><span data-stu-id="139d6-129">This hybrid-enables your existing on-premises Active Directory joined Windows 10 computers and make them cloud ready.</span></span>
    
## <a name="4-enable-automatic-enrollment-for-windows-10"></a><span data-ttu-id="139d6-130">4. Aktivere automatisk registrering for Windows 10</span><span class="sxs-lookup"><span data-stu-id="139d6-130">4. Enable automatic enrollment for Windows 10</span></span>

 <span data-ttu-id="139d6-131">Hvis du vil registrere Windows 10-enheter automatisk for administrasjon av mobilenheter i Intune, kan du se [Registrere en Windows 10-enhet automatisk ved hjelp av gruppepolicy](https://docs.microsoft.com/windows/client-management/mdm/enroll-a-windows-10-device-automatically-using-group-policy).</span><span class="sxs-lookup"><span data-stu-id="139d6-131">To automatically enroll Windows 10 devices for mobile device management in Intune, see [Enroll a Windows 10 device automatically using Group Policy](https://docs.microsoft.com/windows/client-management/mdm/enroll-a-windows-10-device-automatically-using-group-policy).</span></span> <span data-ttu-id="139d6-132">Du kan angi gruppepolicyen på lokalt datamaskinnivå, eller for masseoperasjoner, kan du bruke group Policy Management Console og ADMX-maler til å opprette denne gruppepolicyinnstillingen på domenekontrolleren.</span><span class="sxs-lookup"><span data-stu-id="139d6-132">You can set the Group Policy at a local computer level, or for bulk operations, you can use the Group Policy Management Console and ADMX templates to create this Group Policy setting on your Domain Controller.</span></span>

## <a name="5-configure-seamless-single-sign-on"></a><span data-ttu-id="139d6-133">5. Konfigurer sømløs enkel pålogging</span><span class="sxs-lookup"><span data-stu-id="139d6-133">5. Configure Seamless Single Sign-On</span></span>

  <span data-ttu-id="139d6-134">Sømløs SSO logger automatisk brukere inn i Microsoft 365-skyressursene når de bruker bedriftsdatamaskiner.</span><span class="sxs-lookup"><span data-stu-id="139d6-134">Seamless SSO automatically signs users into their Microsoft 365 cloud resources when they use corporate computers.</span></span> <span data-ttu-id="139d6-135">Bare distribuer ett av de to gruppepolicyalternativene som er beskrevet i [Azure Active Directory Seamless Single Sign-On: Hurtigstart](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sso-quick-start#step-2-enable-the-feature).</span><span class="sxs-lookup"><span data-stu-id="139d6-135">Simply deploy one of the two Group Policy options described in [Azure Active Directory Seamless Single Sign-On: Quick start](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sso-quick-start#step-2-enable-the-feature).</span></span> <span data-ttu-id="139d6-136">**Gruppepolicyalternativet** tillater ikke brukere å endre innstillingene sine, mens alternativet **Gruppepolicyinnstillinger** angir verdiene, men også lar dem konfigureres.</span><span class="sxs-lookup"><span data-stu-id="139d6-136">The **Group Policy** option doesn't allow users to change their settings, while the **Group Policy Preference** option sets the values but also leaves them user-configurable.</span></span>

## <a name="6-set-up-windows-hello-for-business"></a><span data-ttu-id="139d6-137">6. Konfigurere Windows Hello for bedrifter</span><span class="sxs-lookup"><span data-stu-id="139d6-137">6. Set up Windows Hello for Business</span></span>

 <span data-ttu-id="139d6-138">Windows Hello for Business erstatter passord med sterk tofaktorautentisering (2FA) for å logge på en lokal datamaskin.</span><span class="sxs-lookup"><span data-stu-id="139d6-138">Windows Hello for Business replaces passwords with strong two-factor authentication (2FA) for signing into a local computer.</span></span> <span data-ttu-id="139d6-139">En faktor er et asymmetrisk nøkkelpar, og det andre er en PIN-kode eller annen lokal bevegelse, for eksempel fingeravtrykk eller ansiktsgjenkjenning hvis enheten støtter den.</span><span class="sxs-lookup"><span data-stu-id="139d6-139">One factor is an asymmetric key pair, and the other is a PIN or other local gesture such as fingerprint or facial recognition if your device supports it.</span></span> <span data-ttu-id="139d6-140">Vi anbefaler at du erstatter passord med 2FA og Windows Hello for Business der det er mulig.</span><span class="sxs-lookup"><span data-stu-id="139d6-140">We recommend that you replace passwords with 2FA and Windows Hello for Business where possible.</span></span>

<span data-ttu-id="139d6-141">Hvis du vil konfigurere Hybrid Windows Hello for bedrifter, kan du se [gjennom Hybrid Nøkkel klarering Windows Hello for Business Forutsetninger](https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-hybrid-key-trust-prereqs).</span><span class="sxs-lookup"><span data-stu-id="139d6-141">To configure Hybrid Windows Hello for Business, review the [Hybrid Key trust Windows Hello for Business Prerequisites](https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-hybrid-key-trust-prereqs).</span></span> <span data-ttu-id="139d6-142">Følg deretter instruksjonene i [Konfigurere innstillinger for viktig klarering av Hybrid Windows Hello for Business](https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-hybrid-key-whfb-settings).</span><span class="sxs-lookup"><span data-stu-id="139d6-142">Then follow the instructions in [Configure Hybrid Windows Hello for Business key trust settings](https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-hybrid-key-whfb-settings).</span></span> 
