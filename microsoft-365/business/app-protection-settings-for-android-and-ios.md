---
title: Angi innstillinger for appbeskyttelse, for Android- eller iOS-enheter
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Adm_O365
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
ms.assetid: 6f2b80b4-81c3-4714-a7bc-ae69313e8a33
description: Lær hvordan du kan opprette, redigere, eller slette en policy for informasjonsbehandling av app og beskytte arbeidsfiler på Android eller iOS enheter.
ms.openlocfilehash: ed03227496120369b94bf2396974eebfd7798678
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2019
ms.locfileid: "26983666"
---
# <a name="set-app-protection-settings-for-android-or-ios-devices"></a><span data-ttu-id="2c750-103">Angi innstillinger for appbeskyttelse, for Android- eller iOS-enheter</span><span class="sxs-lookup"><span data-stu-id="2c750-103">Set app protection settings for Android or iOS devices</span></span>

## <a name="create-an-app-management-policy"></a><span data-ttu-id="2c750-104">Opprette en policy for appbehandling</span><span class="sxs-lookup"><span data-stu-id="2c750-104">Create an app management policy</span></span>

1. <span data-ttu-id="2c750-105">Logg deg på [Microsoft 365 Business](https://portal.office.com) med legitimasjon for globaladministrator.</span><span class="sxs-lookup"><span data-stu-id="2c750-105">Sign in to [Microsoft 365 Business](https://portal.office.com) with global admin credentials.</span></span> 
    
2. <span data-ttu-id="2c750-106">Velg **Legg til policy** på **Enhetspolicyer**-kortet i administratorportalen.</span><span class="sxs-lookup"><span data-stu-id="2c750-106">In the admin center, on the **Device policies** card, choose **Add policy**.</span></span>
    
    ![Device policies card in the admin center.](media/27c12b61-d112-4348-b557-4f3e46204797.png)
  
3. <span data-ttu-id="2c750-108">Angi et unikt navn for denne policyen på **Legg til policy**-ruten.</span><span class="sxs-lookup"><span data-stu-id="2c750-108">On the **Add policy** pane, enter a unique name for this policy.</span></span> 
    
4. <span data-ttu-id="2c750-109">Velg **Programbehandling for Android** eller **Programbehandling for iOS** under **Policytype**, avhengig av hvilke sett med policyer du vil opprette.</span><span class="sxs-lookup"><span data-stu-id="2c750-109">Under **Policy type**, choose **Application Management for Android** or **Application Management for iOS** depending on which set of policies you want to create.</span></span> 
    
5. <span data-ttu-id="2c750-p101">Utvid **Beskytt arbeidsfiler når enheter går tapt eller blir stjålet** og **Behandle hvordan brukere får tilgang til Office-filer på mobilenheter** \> konfigurer innstillingene slik du ønsker. **Administrer hvordan brukere får tilgang til Office-filer på mobilenheter** er slått **Av** som standard, men det anbefales at du slår den **På** og godtar standardverdiene. Du kan se [Tilgjengelige innstillinger](app-protection-settings-for-android-and-ios.md#bkmk_availablesettings) for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="2c750-p101">Expand **Protect work files when devices are lost or stolen** and **Manage how users access Office files on mobile devices** \> configure the settings how you would like. The **Manage how users access Office files on mobile devices** is **Off** by default, but it is recommended that you turn it **On** and accept the default values. See [Available settings](app-protection-settings-for-android-and-ios.md#bkmk_availablesettings) for more information.</span></span> 
    
    <span data-ttu-id="2c750-113">Du kan til enhver tid bruke **Tilbakestill standardinnstillinger**-koblingen for å gå tilbake til standardinnstillingen.</span><span class="sxs-lookup"><span data-stu-id="2c750-113">You can always use the **Reset default settings** link to return to the default setting.</span></span> 
    
    ![Screenshot of Create a policy with Application management for Android selected](media/eabbe06d-ac0a-4f3a-8630-68c808b1e662.png)
  
6. <span data-ttu-id="2c750-p102">Bestem deretter **Hvem får disse innstillingene?** Hvis du ikke vil bruke den standard sikkerhetsgruppen **Alle brukere**, velger du **Endre**, og velg så sikkerhetsgruppene som vil få disse innstillingene \> **Velg**.</span><span class="sxs-lookup"><span data-stu-id="2c750-p102">Next decide **Who will get these settings?** If you don't want to use the default **All Users** security group, choose **Change**, choose the security groups who will get these settings \> **Select**.</span></span>
    
7. <span data-ttu-id="2c750-117">Velg til slutt **Ferdig** for å lagre policyen og tilordne den til enhetene.</span><span class="sxs-lookup"><span data-stu-id="2c750-117">Finally, choose **Done** to save the policy, and assign it to devices.</span></span> 
    
## <a name="edit-an-app-management-policy"></a><span data-ttu-id="2c750-118">Endre en policy for appbehandling</span><span class="sxs-lookup"><span data-stu-id="2c750-118">Edit an app management policy</span></span>

1. <span data-ttu-id="2c750-119">Velg **Rediger policy**på kortet **policyer** .</span><span class="sxs-lookup"><span data-stu-id="2c750-119">On the **Policies** card, choose **Edit policy**.</span></span>
    
2. <span data-ttu-id="2c750-120">Velg policyen du vil endre, på **Rediger policy**-ruten</span><span class="sxs-lookup"><span data-stu-id="2c750-120">On the **Edit policy** pane, choose the policy you want to change</span></span> 
    
3. <span data-ttu-id="2c750-p103">Velg **Rediger** ved siden av hver innstilling for å endre verdiene i policyen. Når du endrer en verdi, lagres den automatisk i policyen</span><span class="sxs-lookup"><span data-stu-id="2c750-p103">Choose **Edit** next to each setting to change the values in the policy. When you change a value, it is automatically saved into the policy</span></span> 
    
4. <span data-ttu-id="2c750-123">Lukk **Rediger policy**-ruten når du er ferdig.</span><span class="sxs-lookup"><span data-stu-id="2c750-123">When you are finished, close the **Edit policy** pane.</span></span> 
    
## <a name="delete-an-app-management-policy"></a><span data-ttu-id="2c750-124">Slette en policy for appbehandling</span><span class="sxs-lookup"><span data-stu-id="2c750-124">Delete an app management policy</span></span>

1. <span data-ttu-id="2c750-125">Velg **Slette policy** på **Policyer**-kortet.</span><span class="sxs-lookup"><span data-stu-id="2c750-125">On the **Policies** card, choose **Delete policy**.</span></span>
    
2. <span data-ttu-id="2c750-126">Velg den policyen du ønsker å slette, på **Slett policy**-ruten \> **Velg**, deretter **Bekreft** for å slette policyen du valgte.</span><span class="sxs-lookup"><span data-stu-id="2c750-126">On the **Delete policy** pane, choose the policies you want to delete \> **Select**, then **Confirm** to delete the policy or policies you chose.</span></span> 
    
## <a name="available-settings"></a><span data-ttu-id="2c750-127">Tilgjengelige innstillinger</span><span class="sxs-lookup"><span data-stu-id="2c750-127">Available settings</span></span>

<span data-ttu-id="2c750-128">Tabellene nedenfor gir detaljert informasjon om de tilgjengelige innstillingene for å beskytte arbeidsfiler på enheter, samt innstillingene som kontrollerer hvordan brukere får tilgang til Office-filer fra de mobile enhetene.</span><span class="sxs-lookup"><span data-stu-id="2c750-128">The following tables give detailed information about the available settings to protect work files on devices and the settings that control how users access Office files from their mobile devices.</span></span>
  
 <span data-ttu-id="2c750-129">Se [Hvordan tilordnes beskyttelsesfunksjoner i Microsoft 365 Business til Intune-innstillinger](map-protection-features-to-intune-settings.md) for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="2c750-129">See [How do protection features in Microsoft 365 Business map to Intune settings](map-protection-features-to-intune-settings.md) for more information.</span></span> 
  
### <a name="settings-that-protect-work-files"></a><span data-ttu-id="2c750-130">Innstillinger som beskytter arbeidsfiler</span><span class="sxs-lookup"><span data-stu-id="2c750-130">Settings that protect work files</span></span>

<span data-ttu-id="2c750-131">Følgende innstillinger er tilgjengelig for å beskytte arbeidsfiler hvis en brukers enhet mistes eller stjeles:</span><span class="sxs-lookup"><span data-stu-id="2c750-131">The following settings are available to protect work files if a user's device is lost or stolen:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c750-132">Innstilling</span><span class="sxs-lookup"><span data-stu-id="2c750-132">Setting</span></span>  <br/> |<span data-ttu-id="2c750-133">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="2c750-133">Description</span></span>  <br/> |
|<span data-ttu-id="2c750-134">Slette arbeidsfiler fra en inaktiv enhet etter et visst antall dager</span><span class="sxs-lookup"><span data-stu-id="2c750-134">Delete work files from an inactive device after this many days</span></span>  <br/> |<span data-ttu-id="2c750-135">Hvis en enhet ikke er blitt brukt i løpet av det antallet dager som du spesifiserer her, vil eventuelle arbeidsfiler som er lagret på enheten automatisk bli slettet.</span><span class="sxs-lookup"><span data-stu-id="2c750-135">If a device is not used for the number of days that you specify here, any work files stored on the device will automatically be deleted.</span></span>  <br/> |
|<span data-ttu-id="2c750-136">Tvinge brukere til å lagre alle arbeidsfiler til OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="2c750-136">Force users to save all work files to OneDrive for Business</span></span>  <br/> |<span data-ttu-id="2c750-137">Hvis denne innstillingen er **på**, vil den eneste tilgjengelige lagringsplasseringen for arbeidsfiler være OneDrive for Business.</span><span class="sxs-lookup"><span data-stu-id="2c750-137">If this setting is **On**, the only available save location for work files will be OneDrive for Business.</span></span>  <br/> |
|<span data-ttu-id="2c750-138">Kryptere arbeidsfiler</span><span class="sxs-lookup"><span data-stu-id="2c750-138">Encrypt work files</span></span>  <br/> |<span data-ttu-id="2c750-p104">Behold denne innstillingen **på** slik at arbeidsfiler er beskyttet ved hjelp av kryptering. Selv om enheten mistes eller stjeles, vil ingen kunne lese firmadataene.  </span><span class="sxs-lookup"><span data-stu-id="2c750-p104">Keep this setting **On** so that work files are protected by encryption. Even if the device is lost or stolen, no one will be able to read your company data.  </span></span><br/> |
   
### <a name="settings-that-control-how-users-access-office-files-on-mobile-devices"></a><span data-ttu-id="2c750-141">Innstillinger som kontrollerer hvordan brukere får tilgang til Office-filer på mobile enheter</span><span class="sxs-lookup"><span data-stu-id="2c750-141">Settings that control how users access Office files on mobile devices</span></span>

<span data-ttu-id="2c750-142">Følgende innstillinger er tilgjengelig for å styre hvordan brukere får tilgang til Office-arbeidsfiler:</span><span class="sxs-lookup"><span data-stu-id="2c750-142">The following settings are available to manage how users access Office work files:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c750-143">Innstilling</span><span class="sxs-lookup"><span data-stu-id="2c750-143">Setting</span></span>  <br/> |<span data-ttu-id="2c750-144">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="2c750-144">Description</span></span>  <br/> |
|<span data-ttu-id="2c750-145">Kreve en PIN-kode eller et fingeravtrykk for å få tilgang til Office-apper</span><span class="sxs-lookup"><span data-stu-id="2c750-145">Require a PIN or fingerprint to access Office apps</span></span>  <br/> |<span data-ttu-id="2c750-146">Hvis disse innstillingene er **På**, må brukere gi en annen form for godkjenning, i tillegg til brukernavn og passord, før de kan bruke Office-apper på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="2c750-146">If this settings is **On** users have to provide another form of authentication, in addition to their username and password, before they can use Office apps on their mobile device.</span></span>  <br/> |
|<span data-ttu-id="2c750-147">Tilbakestille PIN-kode når påloggingen mislykkes et visst antall ganger</span><span class="sxs-lookup"><span data-stu-id="2c750-147">Reset PIN when login fails this many times</span></span>  <br/> |<span data-ttu-id="2c750-148">Hvis du vil forhindre at en uautorisert bruker tilfeldig gjetter en PIN-kode, tilbakestilles PIN-koden etter det antallet feiloppføringer du angir.</span><span class="sxs-lookup"><span data-stu-id="2c750-148">To prevent an unauthorized user from randomly guessing a PIN, the PIN will reset after the number of wrong entries that you specify.</span></span>  <br/> |
|<span data-ttu-id="2c750-149">Kreve at brukere logger seg på igjen etter at Office-apper har vært inaktive i</span><span class="sxs-lookup"><span data-stu-id="2c750-149">Require users to sign in again after Office apps have been idle for</span></span>  <br/> |<span data-ttu-id="2c750-150">Denne innstillingen bestemmer hvor lenge en bruker kan være inaktiv før de blir bedt om å logge seg på igjen.</span><span class="sxs-lookup"><span data-stu-id="2c750-150">This setting determines how long a user can be idle before they are prompted to sign in again.</span></span>  <br/> |
|<span data-ttu-id="2c750-151">Avslå tilgang til å arbeidsfiler på enheter der programvarebegrensningene er fjernet, eller enheter som har blitt utsatt for utiltenkt rottilgang</span><span class="sxs-lookup"><span data-stu-id="2c750-151">Deny access to work files on jailbroken or rooted devices</span></span>  <br/> |<span data-ttu-id="2c750-p105">Smarte brukere har kanskje en enhet der programvarebegrensningene er fjernet, eller en enhet som har blitt utsatt for utiltenkt rottilgang. Dette betyr at brukeren kan endre operativsystemet, noe som kan gjøre enheten mer utsatt for skadelig programvare. Disse enhetene blokkeres når denne innstillingen er **På**.  </span><span class="sxs-lookup"><span data-stu-id="2c750-p105">Clever users may have a device that is jailbroken or rooted. This means that the user can modify the operating system, which can make the device more subject to malware. These devices are blocked when this setting is **On**.  </span></span><br/> |
|<span data-ttu-id="2c750-155">Tillate brukere å kopiere innhold fra Office-apper til personlige apper</span><span class="sxs-lookup"><span data-stu-id="2c750-155">Allow users to copy content from Office apps into personal apps</span></span>  <br/> |<span data-ttu-id="2c750-p106">Vi tillater dette som standard, men hvis innstillingen er **aktivert**, brukeren kan kopiere informasjonen i en work-fil til en fil med personlige. Hvis innstillingen er **deaktivert**, vil brukeren ikke kunne kopiere informasjon fra en arbeidskonto til en personlig app eller personlig konto.</span><span class="sxs-lookup"><span data-stu-id="2c750-p106">We do allow this by default, but if the setting is **On**, the user could copy information in a work file to a personal file. If the setting is **Off**, the user will be unable to copy information from a work account into a personal app or personal account.  </span></span><br/> |
   

  

