---
title: Få tilgang til lokale ressurser fra en Azure AD-sammenkoblet enhet i Microsoft 365 Business
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
description: Lær hvordan du får tilgang til lokale ressurser som bransjeapper, filressurser og skrivere fra en Azure Active Directory-tilknyttet Windows 10-enhet.
ms.openlocfilehash: 9615ecc9469992d3e5a7479f4799c610db11fb41
ms.sourcegitcommit: 2d664a95b9875f0775f0da44aca73b16a816e1c3
ms.translationtype: MT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/01/2020
ms.locfileid: "44471255"
---
# <a name="access-on-premises-resources-from-an-azure-ad-joined-device-in-microsoft-365-business-premium"></a><span data-ttu-id="15ba2-103">Få tilgang til lokale ressurser fra en Azure AD-tilknyttet enhet i Microsoft 365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="15ba2-103">Access on-premises resources from an Azure AD-joined device in Microsoft 365 Business Premium</span></span>

<span data-ttu-id="15ba2-104">Denne artikkelen gjelder for Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="15ba2-104">This article applies to Microsoft 365 Business Premium.</span></span>

<span data-ttu-id="15ba2-105">Alle Windows 10-enheter som er Azure Active Directory-koblet til, har tilgang til alle skybaserte ressurser, for eksempel Microsoft 365-appene dine, og kan beskyttes av Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="15ba2-105">Any Windows 10 device that is Azure Active Directory joined has access to all cloud-based resources, such as your Microsoft 365 apps, and can be protected by Microsoft 365 Business Premium.</span></span> <span data-ttu-id="15ba2-106">Du kan også gi tilgang til lokale ressurser som lob-apper, filressurser og skrivere.</span><span class="sxs-lookup"><span data-stu-id="15ba2-106">You can also allow access to on-premises resources like line of business (LOB) apps, file shares, and printers.</span></span> <span data-ttu-id="15ba2-107">Hvis du vil gi tilgang, kan du bruke [Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect) til å synkronisere den lokale Active Directory med Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="15ba2-107">To allow access, use [Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect) to synchronize your on-premises Active Directory with Azure Active Directory.</span></span> 

<span data-ttu-id="15ba2-108">Hvis du vil ha mer informasjon, kan du se [Innføring i enhetsbehandling i Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).</span><span class="sxs-lookup"><span data-stu-id="15ba2-108">To learn more, see [Introduction to device management in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).</span></span>
<span data-ttu-id="15ba2-109">Trinnene summeres også i avsnittene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="15ba2-109">The steps are also summarized in the following sections.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15ba2-110">Denne fremgangsmåten gjelder bare for OAuth og NTLM.</span><span class="sxs-lookup"><span data-stu-id="15ba2-110">This procedure is only applicable to OAuth and NTLM.</span></span> <span data-ttu-id="15ba2-111">Kerberos støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="15ba2-111">Kerberos is not supported.</span></span>
 
## <a name="run-azure-ad-connect"></a><span data-ttu-id="15ba2-112">Kjør Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="15ba2-112">Run Azure AD Connect</span></span>

<span data-ttu-id="15ba2-113">Fullfør følgende trinn for å aktivere organisasjonens Azure AD-sammenkoblede enheter for å få tilgang til lokale ressurser.</span><span class="sxs-lookup"><span data-stu-id="15ba2-113">Complete the following steps to enable your organization's Azure AD joined devices to access on-premises resources.</span></span>
  
1. <span data-ttu-id="15ba2-114">Hvis du vil synkronisere brukere, grupper og kontakter fra lokale Active Directory til Azure Active Directory, kjører du veiviseren for katalogsynkronisering og Azure AD Connect som beskrevet i [Konfigurere katalogsynkronisering for Office 365](https://docs.microsoft.com/office365/enterprise/set-up-directory-synchronization).</span><span class="sxs-lookup"><span data-stu-id="15ba2-114">To synchronize your users, groups, and contacts from local Active Directory into Azure Active Directory, run the Directory synchronization wizard and Azure AD Connect as described in [Set up directory synchronization for Office 365](https://docs.microsoft.com/office365/enterprise/set-up-directory-synchronization).</span></span>
    
2. <span data-ttu-id="15ba2-115">Når katalogsynkroniseringen er fullført, må du kontrollere at organisasjonens Windows 10-enheter er Azure AD som er koblet sammen.</span><span class="sxs-lookup"><span data-stu-id="15ba2-115">After the directory synchronization is complete, make sure your organization's Windows 10 devices are Azure AD joined.</span></span> <span data-ttu-id="15ba2-116">Dette trinnet gjøres individuelt på hver Windows 10-enhet.</span><span class="sxs-lookup"><span data-stu-id="15ba2-116">This step is done individually on each Windows 10 device.</span></span> <span data-ttu-id="15ba2-117">Se [Konfigurere Windows-enheter for Microsoft 365 Business Premium-brukere](set-up-windows-devices.md) hvis du vil ha mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="15ba2-117">See [Set up Windows devices for Microsoft 365 Business Premium users](set-up-windows-devices.md) for details.</span></span> 
    
3. <span data-ttu-id="15ba2-118">Når Windows 10-enhetene er Azure AD slått sammen, må hver bruker starte enhetene på nytt og logge på med Microsoft 365 Business Premium-legitimasjonen.</span><span class="sxs-lookup"><span data-stu-id="15ba2-118">Once the Windows 10 devices are Azure AD joined, each user must reboot their devices and sign in with their Microsoft 365 Business Premium credentials.</span></span> <span data-ttu-id="15ba2-119">Alle enheter har nå også tilgang til lokale ressurser.</span><span class="sxs-lookup"><span data-stu-id="15ba2-119">All devices now have access to on-premises resources as well.</span></span>
    
<span data-ttu-id="15ba2-120">Ingen flere trinn er nødvendig for å få tilgang til lokale ressurser for Azure AD sammenføyde enheter.</span><span class="sxs-lookup"><span data-stu-id="15ba2-120">No additional steps are required to get access to on-premises resources for Azure AD joined devices.</span></span> <span data-ttu-id="15ba2-121">Denne funksjonaliteten er innebygd i Windows 10.</span><span class="sxs-lookup"><span data-stu-id="15ba2-121">This functionality is built into Windows 10.</span></span> 

<span data-ttu-id="15ba2-122">Hvis du har planer om å logge inn på AADJ-enheten annet enn passordmetoden Som PIN /Bio-metrisk via WHFB-pålogging og deretter få tilgang til lokale ressurser (delinger, skrivere.. osv.), vennligst følghttps://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-hybrid-aadj-sso-base</span><span class="sxs-lookup"><span data-stu-id="15ba2-122">If you have plans to login to the AADJ device other than password method Like PIN/Bio-metric via WHFB credential login and then access on-premise resources (shares,printers..etc), please follow https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-hybrid-aadj-sso-base</span></span>
  
<span data-ttu-id="15ba2-123">Hvis organisasjonen ikke er klar til å distribueres i Azure AD-konfigurasjonen som er sammenkoblet, som er beskrevet ovenfor, kan du vurdere å konfigurere [konfigurasjonen for Hybrid Azure AD-sammenføyde enheter](manage-windows-devices.md).</span><span class="sxs-lookup"><span data-stu-id="15ba2-123">If your organization isn't ready to deploy in the Azure AD joined device configuration described above, consider setting up [Hybrid Azure AD Joined device configuration](manage-windows-devices.md).</span></span>
  
### <a name="considerations-when-you-join-windows-devices-to-azure-ad"></a><span data-ttu-id="15ba2-124">Vurderinger når du blir med Windows-enheter til Azure AD</span><span class="sxs-lookup"><span data-stu-id="15ba2-124">Considerations when you join Windows devices to Azure AD</span></span>

<span data-ttu-id="15ba2-125">Hvis Windows-enheten du azure-AD ble med i, tidligere var domenet til eller i en arbeidsgruppe, bør du vurdere følgende begrensninger:</span><span class="sxs-lookup"><span data-stu-id="15ba2-125">If the Windows device that you Azure-AD joined was previously domain-joined or in a workgroup, consider the following limitations:</span></span>
  
- <span data-ttu-id="15ba2-126">Når en enhet Azure AD blir med, oppretter den en ny bruker uten å referere til en eksisterende profil.</span><span class="sxs-lookup"><span data-stu-id="15ba2-126">When a device Azure AD joins, it creates a new user without referencing an existing profile.</span></span> <span data-ttu-id="15ba2-127">Profiler må overføres manuelt.</span><span class="sxs-lookup"><span data-stu-id="15ba2-127">Profiles must be manually migrated.</span></span> <span data-ttu-id="15ba2-128">En brukerprofil inneholder informasjon som favoritter, lokale filer, nettleserinnstillinger og Innstillinger for Start-menyen.</span><span class="sxs-lookup"><span data-stu-id="15ba2-128">A user profile contains information like favorites, local files, browser settings, and Start menu settings.</span></span> <span data-ttu-id="15ba2-129">En best tilnærming er å finne et tredjepartsverktøy for å tilordne eksisterende filer og innstillinger til den nye profilen.</span><span class="sxs-lookup"><span data-stu-id="15ba2-129">A best approach is to find a third-party tool to map existing files and settings to the new profile.</span></span>

- <span data-ttu-id="15ba2-130">Hvis enheten bruker gruppepolicyobjekter (GPO), kan det hende at noen gruppepolicyobjekter ikke har en sammenlignbar [konfigurasjonstjenesteleverandør](https://docs.microsoft.com/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers) (CSP) i Intune.</span><span class="sxs-lookup"><span data-stu-id="15ba2-130">If the device is using Group Policy Objects (GPO), some GPOs may not have a comparable [Configuration Service Provider](https://docs.microsoft.com/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers) (CSP) in Intune.</span></span> <span data-ttu-id="15ba2-131">Kjør [MMAT-verktøyet](https://www.microsoft.com/download/details.aspx?id=45520) for å finne sammenlignbare CSPer for eksisterende gruppepolicyobjekter.</span><span class="sxs-lookup"><span data-stu-id="15ba2-131">Run the [MMAT tool](https://www.microsoft.com/download/details.aspx?id=45520) to find comparable CSPs for existing GPOs.</span></span>

- <span data-ttu-id="15ba2-132">Brukere kan ikke godkjenne til programmer som er avhengige av Active Directory-godkjenning.</span><span class="sxs-lookup"><span data-stu-id="15ba2-132">Users won't be able to authenticate to applications that depend on Active Directory authentication.</span></span> <span data-ttu-id="15ba2-133">Evaluer den eldre appen og vurder å oppdatere til en app som bruker moderne Auth, hvis mulig.</span><span class="sxs-lookup"><span data-stu-id="15ba2-133">Evaluate the legacy app and consider updating to an app that uses modern Auth, if possible.</span></span>

- <span data-ttu-id="15ba2-134">Active Directory-skrivergjenkjenning fungerer ikke.</span><span class="sxs-lookup"><span data-stu-id="15ba2-134">Active Directory printer discovery won't work.</span></span> <span data-ttu-id="15ba2-135">Du kan angi direkte skriverbaner for alle brukere eller bruke [Hybrid Cloud Print](https://docs.microsoft.com/windows-server/administration/hybrid-cloud-print/hybrid-cloud-print-deploy).</span><span class="sxs-lookup"><span data-stu-id="15ba2-135">You can provide direct printer paths for all users or use [Hybrid Cloud Print](https://docs.microsoft.com/windows-server/administration/hybrid-cloud-print/hybrid-cloud-print-deploy).</span></span>
