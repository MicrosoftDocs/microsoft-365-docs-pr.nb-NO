---
title: Sikre Windows 10-enheter
ms.author: sirkkuw
author: sirkkuw
manager: scotv
audience: Admin
ms.topic: conceptual
f1_keywords:
- O365E_BCSSetup4WindowsConfig
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 21e5551f-fa35-4f13-9418-f80d668b6a2b
description: 'Lær om standard og andre innstillinger for å sikre Windows 10-enheter. '
ms.openlocfilehash: 64f20433d5a4b78fc234a4ec3bec937ec30145c6
ms.sourcegitcommit: 0ad0092d9c5cb2d69fc70c990a9b7cc03140611b
ms.translationtype: MT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/19/2019
ms.locfileid: "40805647"
---
# <a name="secure-windows-10-devices"></a><span data-ttu-id="536ba-103">Sikre Windows 10-enheter</span><span class="sxs-lookup"><span data-stu-id="536ba-103">Secure Windows 10 devices</span></span>

<span data-ttu-id="536ba-104">Innstillingene du konfigurerer her er en del av standardpolicyen for enheter for Windows 10.</span><span class="sxs-lookup"><span data-stu-id="536ba-104">The settings that you configure here are part of the default device policy for Windows 10.</span></span> <span data-ttu-id="536ba-105">Alle brukere som kobler til en Windows 10-enhet, inkludert mobile enheter og PC-er, ved å logge på med arbeidskontoen, vil automatisk motta disse innstillingene.</span><span class="sxs-lookup"><span data-stu-id="536ba-105">All users who connect a Windows 10 device, including mobile devices and PCs, by signing in with their work account will automatically receive these settings.</span></span> <span data-ttu-id="536ba-106">Vi anbefaler at du godtar standardpolicyen under konfigurasjonen og legger til policyer senere som retter seg mot bestemte grupper av brukere.</span><span class="sxs-lookup"><span data-stu-id="536ba-106">We recommend that you accept the default policy during setup and add policies later that target specific groups of users.</span></span>
  
## <a name="settings-to-secure-windows-10-devices"></a><span data-ttu-id="536ba-107">Innstillinger for å sikre Windows 10-enheter</span><span class="sxs-lookup"><span data-stu-id="536ba-107">Settings to secure Windows 10 devices</span></span>

<span data-ttu-id="536ba-p102">Som standard er alle innstillingene **På**. Følgende innstillinger er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="536ba-p102">By default all settings are **On**. The following settings are available:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="536ba-110">Innstilling</span><span class="sxs-lookup"><span data-stu-id="536ba-110">Setting</span></span>  <br/> |<span data-ttu-id="536ba-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="536ba-111">Description</span></span>  <br/> |
|<span data-ttu-id="536ba-112">Beskytte PC mot virus og andre trusler ved hjelp av Windows Defender Antivirus</span><span class="sxs-lookup"><span data-stu-id="536ba-112">Help protect PCs from viruses and other threats using Windows Defender Antivirus</span></span>  <br/> |<span data-ttu-id="536ba-113">Krever at Windows Defender Antivirus er slått på for å beskytte PC-er fra farene ved å være koblet til Internett.</span><span class="sxs-lookup"><span data-stu-id="536ba-113">Requires that Windows Defender Antivirus is turned on to protect PCs from the dangers of being connected to the internet.</span></span>  <br/> |
|<span data-ttu-id="536ba-114">Beskytte PC-er fra nettbaserte trusler i Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="536ba-114">Help protect PCs from web-based threats in Microsoft Edge</span></span>  <br/> |<span data-ttu-id="536ba-115">Slår på innstillinger i Microsoft Edge som beskytter brukere mot skadelige nettsteder og nedlastinger.</span><span class="sxs-lookup"><span data-stu-id="536ba-115">Turns on settings in Edge that help protect users from malicious sites and downloads.</span></span>  <br/> |
|<span data-ttu-id="536ba-116">Slå av skjermen på enheten når den har vært inaktiv i en viss periode</span><span class="sxs-lookup"><span data-stu-id="536ba-116">Turn off device screen when idle for this amount of time</span></span>  <br/> |<span data-ttu-id="536ba-p103">Sørger for at bedriftsdata er beskyttet dersom en bruker er inaktiv. En bruker kan jobbe på et offentlig sted, som for eksempel en kaffebar, går bort eller blir distrahert i et øyeblikk, og lar enheten være sårbar for tilfeldig innsyn. Denne innstillingen lar deg bestemme hvor lenge en bruker kan være inaktiv før skjermen slås av.</span><span class="sxs-lookup"><span data-stu-id="536ba-p103">Makes sure that company data is protected if a user is idle. A user may be working in a public location, like a coffee shop, and step away or be distracted for just a moment, leaving their device vulnerable to random glances. This setting lets you control how long the user can be idle before the screen shuts off.</span></span>  <br/> |
|<span data-ttu-id="536ba-120">Tillat brukere å laste ned apper fra Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="536ba-120">Allow users to download apps from Microsoft Store</span></span>  <br/> |<span data-ttu-id="536ba-p104">Lar brukere laste ned og installere apper fra Microsoft Store. Apper inkluderer alt fra spill til produktivitetsverktøy, så vi lar denne innstillingen være **På**, men du kan slå den av for ekstra sikkerhet.  </span><span class="sxs-lookup"><span data-stu-id="536ba-p104">Lets users download and install apps from the Microsoft Store. Apps include everything from games to productivity tools, so we leave this setting **On**, but you can turn it off for extra security.  </span></span><br/> |
|<span data-ttu-id="536ba-123">Gi brukere tilgang til Cortana</span><span class="sxs-lookup"><span data-stu-id="536ba-123">Allow users to access Cortana</span></span>  <br/> |<span data-ttu-id="536ba-124">Cortana kan være svært nyttig!</span><span class="sxs-lookup"><span data-stu-id="536ba-124">Cortana can be very helpful!</span></span> <span data-ttu-id="536ba-125">Cortana kan slå innstillingene på eller av for deg, gi veibeskrivelser og sørge for at du er på tid for avtaler, så vi beholder denne **innstillingen som** standard.</span><span class="sxs-lookup"><span data-stu-id="536ba-125">Cortana can turn settings on or off for you, give directions, and make sure you're on time for appointments, so we keep this setting **On** by default.</span></span>  <br/> |
|<span data-ttu-id="536ba-126">Tillat brukere å motta Windows-tips og annonser fra Microsoft</span><span class="sxs-lookup"><span data-stu-id="536ba-126">Allow users to receive Windows tips and advertisements from Microsoft</span></span>  <br/> |<span data-ttu-id="536ba-127">Tips for Windows kan være praktisk, samt orientere brukere når nye funksjoner utgis.</span><span class="sxs-lookup"><span data-stu-id="536ba-127">Windows tips can be handy and help orient users when new features are released.</span></span>  <br/> |
|<span data-ttu-id="536ba-128">Holde Windows 10-enheter oppdatert automatisk</span><span class="sxs-lookup"><span data-stu-id="536ba-128">Keep Windows 10 devices up to date automatically</span></span>  <br/> |<span data-ttu-id="536ba-129">Sørger for at Windows 10-enheter automatisk mottar de nyeste oppdateringene.</span><span class="sxs-lookup"><span data-stu-id="536ba-129">Makes sure that Windows 10 devices automatically receive the latest updates.</span></span>  <br/> |
   

