---
title: Konfigurere Microsoft 365 Business
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
f1_keywords:
- O365E_M365SetupBanner
- BCS365_M365SetupBanner
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
ms.custom: OKR_SMB_M365
search.appverid:
- BCS160
- MET150
ms.assetid: 6e7a2dfd-8ec4-4eb7-8390-3ee103e5fece
description: Lær hvordan du konfigurerer Microsoft 365 Business.
ms.openlocfilehash: 4f31af3fa63416d3b1bd7281f7712313252ad437
ms.sourcegitcommit: cbf117a4cd92a907115c9f10752f3c557361e586
ms.translationtype: MT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "37440605"
---
# <a name="set-up-microsoft-365-business-in-the-setup-wizard"></a><span data-ttu-id="d6c03-103">Konfigurere Microsoft 365 Business i installasjonsveiviseren</span><span class="sxs-lookup"><span data-stu-id="d6c03-103">Set up Microsoft 365 Business in the setup wizard</span></span>

## <a name="add-your-domain-users-and-set-up-policies"></a><span data-ttu-id="d6c03-104">Legg til domene, brukere og Konfigurer policyer</span><span class="sxs-lookup"><span data-stu-id="d6c03-104">Add your domain, users, and set up policies</span></span>

<span data-ttu-id="d6c03-105">[![Label å fortelle deg at Administrasjonssenteret er i endring, og du kan finne mer informasjon på aka.ms/aboutM365preview.](media/m365admincenterchanging.png)](https://docs.microsoft.com/office365/admin/microsoft-365-admin-center-preview)</span><span class="sxs-lookup"><span data-stu-id="d6c03-105">[![Label to let you know the admin center is changing and you can find more details at aka.ms/aboutM365preview.](media/m365admincenterchanging.png)](https://docs.microsoft.com/office365/admin/microsoft-365-admin-center-preview)</span></span>

<span data-ttu-id="d6c03-106">Når du kjøper Microsoft 365 Business, har du muligheten til å bruke et domene du eier, eller kjøpe et under [registreringen](sign-up.md).</span><span class="sxs-lookup"><span data-stu-id="d6c03-106">When you purchase Microsoft 365 Business, you have the option of using a domain you own, or buying one during the [sign-up](sign-up.md).</span></span>

- <span data-ttu-id="d6c03-107">Hvis du kjøpte et nytt domene da du registrerte deg, er domenet ditt konfigurert, og du kan gå videre til å [legge til brukere og tilordne lisenser](#add-users-and-assign-licenses).</span><span class="sxs-lookup"><span data-stu-id="d6c03-107">If you purchased a new domain when you signed up, your domain is all set up and you can move to [Add users and assign licenses](#add-users-and-assign-licenses).</span></span>

### <a name="add-your-domain-to-personalize-sign-in"></a><span data-ttu-id="d6c03-108">Legge til domenet for å tilpasse påloggingen</span><span class="sxs-lookup"><span data-stu-id="d6c03-108">Add your domain to personalize sign-in</span></span>

1. <span data-ttu-id="d6c03-109">Logg på [administrasjonssenteret for Microsoft 365](https://admin.microsoft.com) ved hjelp av legitimasjonen for global administrator.</span><span class="sxs-lookup"><span data-stu-id="d6c03-109">Sign in to [Microsoft 365 admin center](https://admin.microsoft.com) by using your global admin credentials.</span></span> 

2. <span data-ttu-id="d6c03-110">Velg **Legg til et domene** eller **Legg til brukere** for å starte veiviseren.</span><span class="sxs-lookup"><span data-stu-id="d6c03-110">Choose **Add a domain** or **Add users** to start the wizard.</span></span>
    > [!IMPORTANT]
    > <span data-ttu-id="d6c03-111">Hvis du har kjøpt et domene under registreringen, vil du ikke se **Legg til et domene** trinn her.</span><span class="sxs-lookup"><span data-stu-id="d6c03-111">If you purchased a domain during the sign-up, you will not see **Add a domain** step here.</span></span> <span data-ttu-id="d6c03-112">Gå til [Legg til brukere](#add-users-and-assign-licenses) i stedet.</span><span class="sxs-lookup"><span data-stu-id="d6c03-112">Go to [Add users ](#add-users-and-assign-licenses) instead.</span></span>

    ![Velg gå til oppsett.](media/gotosetupinadmincenter.png)
    
3. <span data-ttu-id="d6c03-114">I veiviseren skriver du inn domenenavnet du vil bruke (som contoso.com).</span><span class="sxs-lookup"><span data-stu-id="d6c03-114">In the wizard, enter the domain name you want to use (like contoso.com).</span></span>


    ![Skjermbilde av Tilpass påloggingssiden.](media/personalizesignin.png)

    
4. <span data-ttu-id="d6c03-116">Følg trinnene i veiviseren for å [opprette DNS-poster i en hvilken som helst DNS-webvert for Office 365](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider) som bekrefter at du eier domenet.</span><span class="sxs-lookup"><span data-stu-id="d6c03-116">Follow the steps in the wizard to [Create DNS records at any DNS hosting provider for Office 365](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider) that verifies you own the domain.</span></span> <span data-ttu-id="d6c03-117">Hvis du kjenner domeneverten, kan du også se de [spesifikke instruksjonene for verten](https://docs.microsoft.com/office365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions).</span><span class="sxs-lookup"><span data-stu-id="d6c03-117">If you know your domain host, see also the [host specific instructions](https://docs.microsoft.com/office365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions).</span></span>

    <span data-ttu-id="d6c03-118">Hvis vertsleverandøren er GoDaddy, eller en annen vert som er aktivert med [domene tilkobling](https://docs.microsoft.com/office365/admin/get-help-with-domains/domain-connect), er prosessen enkel, og du blir automatisk bedt om å logge på og la Microsoft godkjenne på dine vegne:</span><span class="sxs-lookup"><span data-stu-id="d6c03-118">If your hosting provider is GoDaddy, or another host enabled with [domain connect](https://docs.microsoft.com/office365/admin/get-help-with-domains/domain-connect), the process is easy and you will be automatically asked to sign in and let Microsoft authenticate on your behalf:</span></span>

    ![På GoDaddy Bekreft tilgang-siden velger du Godkjenn.](media/godaddyauth.png)

### <a name="add-users-and-assign-licenses"></a><span data-ttu-id="d6c03-120">Legge til brukere og tilordne lisenser</span><span class="sxs-lookup"><span data-stu-id="d6c03-120">Add users and assign licenses</span></span>

<span data-ttu-id="d6c03-121">Du kan legge til brukere i veiviseren, men du kan også [legge til brukere senere](add-users-m365b.md) i administrasjonssenteret.</span><span class="sxs-lookup"><span data-stu-id="d6c03-121">You can add users in the wizard, but you can also [add users later](add-users-m365b.md) in the admin center.</span></span> <span data-ttu-id="d6c03-122">I tillegg, hvis du har en lokal domenekontroller, kan du legge til brukere med [Azure ad-tilkobling](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express).</span><span class="sxs-lookup"><span data-stu-id="d6c03-122">Additionally, if you have a local domain controller, you can add users with [Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express).</span></span>

#### <a name="add-users-in-the-wizard"></a><span data-ttu-id="d6c03-123">Legg til brukere i veiviseren</span><span class="sxs-lookup"><span data-stu-id="d6c03-123">Add users in the wizard</span></span>

<span data-ttu-id="d6c03-124">Alle brukere du legger til i veiviseren, får automatisk tilordnet en Microsoft 365 business-lisens.</span><span class="sxs-lookup"><span data-stu-id="d6c03-124">Any users you add in the wizard get automatically assigned a Microsoft 365 Business license.</span></span>

![Skjermbilde av siden Legg til nye brukere i veiviseren](media/addnewuserspage.png)

1. <span data-ttu-id="d6c03-126">Hvis Microsoft 365 Business-abonnementet har eksisterende brukere (for eksempel hvis du brukte Azure AD-tilkobling), får du muligheten til å tilordne lisenser til dem nå.</span><span class="sxs-lookup"><span data-stu-id="d6c03-126">If your Microsoft 365 Business subscription has existing users (for example, if you used Azure AD Connect) , you get an option to assign licenses to them now.</span></span> <span data-ttu-id="d6c03-127">Gå videre og legg til lisenser for dem også.</span><span class="sxs-lookup"><span data-stu-id="d6c03-127">Go ahead and add licenses to them as well.</span></span>

2. <span data-ttu-id="d6c03-128">Når du har lagt til brukerne, vil du også få mulighet til å dele legitimasjonen med de nye brukerne du la til.</span><span class="sxs-lookup"><span data-stu-id="d6c03-128">After you have added the users, you will also get an option to share credentials with the new users you added.</span></span> <span data-ttu-id="d6c03-129">Du kan velge å skrive dem ut, sende dem via e-post eller laste dem ned.</span><span class="sxs-lookup"><span data-stu-id="d6c03-129">You can choose to print them out, email them, or download them.</span></span>

3. <span data-ttu-id="d6c03-130">På Opprett team for organisasjonen kan du velge å legge til team og legge til brukere i dem.</span><span class="sxs-lookup"><span data-stu-id="d6c03-130">On the Create Teams for your organization, you can choose to add Teams and add users to them.</span></span> <span data-ttu-id="d6c03-131">Du kan også gjøre dette senere.</span><span class="sxs-lookup"><span data-stu-id="d6c03-131">You can also do this later.</span></span> <span data-ttu-id="d6c03-132">Hvis du vil ha mer informasjon, kan du se [opprette et team på hele firmaet](https://support.office.com/article/037bb27a-bcc9-48fe-8d72-44d9482420a3).</span><span class="sxs-lookup"><span data-stu-id="d6c03-132">For more information, see [create a company-wide Team](https://support.office.com/article/037bb27a-bcc9-48fe-8d72-44d9482420a3).</span></span>

4. <span data-ttu-id="d6c03-133">Hopp over overføring av e-postmeldinger, og velg **Neste** på **Overfør e-postmeldinger**-siden.</span><span class="sxs-lookup"><span data-stu-id="d6c03-133">Skip migrating email messages and choose **Next** on **Migrate email messages** page.</span></span> 

    <span data-ttu-id="d6c03-134">Hvis du flytter fra en annen e-postleverandøren og vil kopiere dataene senere, kan du [overføre e-post og kontakter til Office 365](https://support.office.com/article/a3e3bddb-582e-4133-8670-e61b9f58627e).</span><span class="sxs-lookup"><span data-stu-id="d6c03-134">If you are moving from another email provider and want to copy your data later, you can [Migrate email and contacts to Office 365](https://support.office.com/article/a3e3bddb-582e-4133-8670-e61b9f58627e).</span></span>


### <a name="connect-your-domain"></a><span data-ttu-id="d6c03-135">Koble til domenet ditt</span><span class="sxs-lookup"><span data-stu-id="d6c03-135">Connect your domain</span></span>

> [!NOTE]
> <span data-ttu-id="d6c03-136">Hvis du velger å bruke. onmicrosoft-domenet, eller brukte Azure AD Connect til å konfigurere brukere, vil du ikke se dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="d6c03-136">If you chose to use the .onmicrosoft domain, or used Azure AD Connect to set up users, you will not see this step.</span></span>
  
<span data-ttu-id="d6c03-137">Hvis du vil konfigurere tjenester, må du oppdatere noen poster på DNS-verten eller domeneregistratoren.</span><span class="sxs-lookup"><span data-stu-id="d6c03-137">To set up services, you have to update some records at your DNS host or domain registrar.</span></span>
  
1. <span data-ttu-id="d6c03-138">Oppsettsveiviseren oppdager vanligvis registratoren og gir deg en kobling til trinnvise instruksjoner for hvordan du oppdaterer NS-postene på nettstedet til registratoren.</span><span class="sxs-lookup"><span data-stu-id="d6c03-138">The setup wizard typically detects your registrar and gives you a link to step-by-step instructions for updating your NS records at the registrar website.</span></span> <span data-ttu-id="d6c03-139">Hvis den ikke gjør det, [endrer du navneservere for å konfigurere Office 365 med en hvilken som helst domeneregistratoren](https://support.office.com/article/a8b487a9-2a45-4581-9dc4-5d28a47010a2).</span><span class="sxs-lookup"><span data-stu-id="d6c03-139">If it doesn't, [Change nameservers to set up Office 365 with any domain registrar](https://support.office.com/article/a8b487a9-2a45-4581-9dc4-5d28a47010a2).</span></span> 

    - <span data-ttu-id="d6c03-140">Hvis du har eksisterende DNS-poster, for eksempel et eksisterende webområde, men DNS-verten er aktivert for [domene tilkobling](https://docs.microsoft.com/office365/admin/get-help-with-domains/domain-connect), velger **du Legg til oppføringer for meg**.</span><span class="sxs-lookup"><span data-stu-id="d6c03-140">If you have existing DNS records, for example an existing web site, but your DNS host is enabled for [domain connect](https://docs.microsoft.com/office365/admin/get-help-with-domains/domain-connect), choose **Add records for me**.</span></span> <span data-ttu-id="d6c03-141">Godta alle standardene på siden **Velg dine elektroniske tjenester** , velg **neste**, og velg **Godkjenn** på DNS-vertens side.</span><span class="sxs-lookup"><span data-stu-id="d6c03-141">On the **Choose your online services** page, accept all the defaults, and choose **Next**,and choose **Authorize** on your DNS host's page.</span></span>
    - <span data-ttu-id="d6c03-142">Hvis du har eksisterende DNS-poster med andre DNS-verter (ikke aktivert for domene tilkobling), vil du administrere dine egne DNS-poster for å sikre at de eksisterende tjenestene forblir tilkoblet.</span><span class="sxs-lookup"><span data-stu-id="d6c03-142">If you have existing DNS records with other DNS hosts (not enabled for domain connect), you will want to manage your own DNS records to make sure the existing services stay connected.</span></span> <span data-ttu-id="d6c03-143">Se [grunnleggende om domenet](https://docs.microsoft.com/office365/admin/get-help-with-domains/dns-basics) for mer info.</span><span class="sxs-lookup"><span data-stu-id="d6c03-143">See [domain basics](https://docs.microsoft.com/office365/admin/get-help-with-domains/dns-basics) for more info.</span></span>

        ![Koble domenet siden med jeg skal administrere mine egne DNS-poster.](media/connectyourdomainpage.png)

2. <span data-ttu-id="d6c03-145">Følg trinnene i veiviseren, og e-post og andre tjenester vil bli satt opp for deg.</span><span class="sxs-lookup"><span data-stu-id="d6c03-145">Follow the steps in the wizard and email and other services will be set up for you.</span></span>

### <a name="protect-data-and-devices"></a><span data-ttu-id="d6c03-146">Beskytt data og enheter</span><span class="sxs-lookup"><span data-stu-id="d6c03-146">Protect data and devices</span></span> 

<span data-ttu-id="d6c03-147">Policyene du definerer i veiviseren, brukes automatisk på en [sikkerhetsgruppe](https://docs.microsoft.com/office365/admin/create-groups/compare-groups#security-groups) som kalles *alle brukere*.</span><span class="sxs-lookup"><span data-stu-id="d6c03-147">The policies you set up in the wizard are applied automatically to a [Security group](https://docs.microsoft.com/office365/admin/create-groups/compare-groups#security-groups) called *All Users*.</span></span> <span data-ttu-id="d6c03-148">Du kan også opprette flere grupper for å tilordne policyer til i administrasjonssenteret.</span><span class="sxs-lookup"><span data-stu-id="d6c03-148">You can also create additional groups to assign policies to in the admin center.</span></span>

1. <span data-ttu-id="d6c03-149">På **Beskytt arbeidet filer på mobile enheter** alternativet **Beskytt arbeidsfiler når enheter er tapt eller stjålet** er valgt som standard.</span><span class="sxs-lookup"><span data-stu-id="d6c03-149">On the **Protect your work files on mobile devices** the option **Protect work files when devices are lost or stolen** is selected by default.</span></span> <span data-ttu-id="d6c03-150">Du har muligheten til å aktivere **administrere hvordan brukere får tilgang til Office-filer på mobile enheter**, og dette anbefales.</span><span class="sxs-lookup"><span data-stu-id="d6c03-150">You have an option to turn on **Manage how users access Office files on mobile devices**, and this is recommended.</span></span>

    ![Skjermene av beskytte arbeide fil-størrelse opp på transportabel anordninger side.](media/protectworkfilesondevices.png)

     - <span data-ttu-id="d6c03-152">Utfolde **beskytte arbeide fil-størrelse når anordninger er bortkommet eller stjålet** å utfoldelse [uteblivelsen verdier](protect-work-files-on-lost-or-stolen-device.md):</span><span class="sxs-lookup"><span data-stu-id="d6c03-152">Expand **Protect work files when devices are lost or stolen** to display the [default values](protect-work-files-on-lost-or-stolen-device.md):</span></span>

        ![Skjermbilde av standardverdier for beskyttelse av filer på tapte enheter.](media/protectworkfilesondevicesdefault.png)

    - <span data-ttu-id="d6c03-154">Velg **Administrer hvordan brukere får tilgang til Office-filer på mobile enheter** , og Utvid dem for å vise [standardverdiene](manage-user-access-on-mobile-devices.md).</span><span class="sxs-lookup"><span data-stu-id="d6c03-154">Select **Manage how users access Office files on mobile devices** and expand it to display the [default values](manage-user-access-on-mobile-devices.md).</span></span> <span data-ttu-id="d6c03-155">Vi anbefaler at du godtar standardverdiene under installasjonen for å opprette programpolicyer for Android, iOS og Windows 10 som gjelder for alle brukere.</span><span class="sxs-lookup"><span data-stu-id="d6c03-155">We recommend that you accept the default values during setup to create application policies for Android, iOS, and Windows 10 that apply to all users.</span></span> <span data-ttu-id="d6c03-156">Du kan opprette flere policyer når konfigurasjonen er fullført.</span><span class="sxs-lookup"><span data-stu-id="d6c03-156">You can create more policies after setup completes.</span></span>

        ![Skjermbilde av beskyttelsesinnstillinger for Office-filer på mobilenheter.](media/useraccessonmobile.png)

2. <span data-ttu-id="d6c03-158">Det siste trinnet på beskyttelse av data og enheter gjør det mulig å konfigurere policyer for å sikre Windows 10-enheter.</span><span class="sxs-lookup"><span data-stu-id="d6c03-158">The last step on protect data and devices allows you to set up policies to secure Windows 10 devices.</span></span> <span data-ttu-id="d6c03-159">Disse innstillingene brukes automatisk når en brukers Windows 10 kobler til organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="d6c03-159">These settings are applied automatically when a user's Windows 10 connects to your organization.</span></span> <span data-ttu-id="d6c03-160">Du kan utvide **sikre Windows 10-enheter** for å se og endre [standardverdiene](secure-windows-10-devices.md).</span><span class="sxs-lookup"><span data-stu-id="d6c03-160">You can expand **Secure Windows 10 devices** to see and modify the [default values](secure-windows-10-devices.md).</span></span>
3. <span data-ttu-id="d6c03-161">Du kan også velge å [installere Office](install-office-on-windows-10-during-setup.md) på Windows 10-enheter automatisk.</span><span class="sxs-lookup"><span data-stu-id="d6c03-161">You can also choose to [automatically install Office](install-office-on-windows-10-during-setup.md) on Windows 10 devices.</span></span>

    ![Skjermbilde av angi konfigurasjonssiden for Windows 10-enheten.](media/setwin10config.png)


## <a name="deploy-office-365-client-apps"></a><span data-ttu-id="d6c03-163">Distribuere klientprogrammer for Office 365</span><span class="sxs-lookup"><span data-stu-id="d6c03-163">Deploy Office 365 client apps</span></span>

<span data-ttu-id="d6c03-164">Hvis du velger å installere Office-apper automatisk i løpet av oppsettet, installeres appene på Windows 10-enhetene når brukerne har logget på Azure AD fra Windows-enhetene sine med arbeids legitimasjonen sin.</span><span class="sxs-lookup"><span data-stu-id="d6c03-164">If you chose to automatically install Office apps in during the set up, the apps will install on the Windows 10 devices once the users have signed in to Azure AD from their Windows devices with their work credentials.</span></span>
<span data-ttu-id="d6c03-165">Hvis du vil installere Office på mobile iOS-eller Android-enheter, kan du se [konfigurere mobile enheter for Microsoft 365 Business-brukere](set-up-mobile-devices.md).</span><span class="sxs-lookup"><span data-stu-id="d6c03-165">To install Office on mobile iOS or Android devices, see [Set up mobile devices for Microsoft 365 Business users](set-up-mobile-devices.md).</span></span>

<span data-ttu-id="d6c03-166">Du kan også installere Office individuelt.</span><span class="sxs-lookup"><span data-stu-id="d6c03-166">You can also install Office individually.</span></span> <span data-ttu-id="d6c03-167">Se [installere Office på en PC eller Mac](https://support.office.com/article/4414eaaf-0478-48be-9c42-23adc4716658) for instruksjoner.</span><span class="sxs-lookup"><span data-stu-id="d6c03-167">See [install Office on a PC or Mac](https://support.office.com/article/4414eaaf-0478-48be-9c42-23adc4716658) for instructions.</span></span>
