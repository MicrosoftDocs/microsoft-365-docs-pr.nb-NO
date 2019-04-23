---
title: Om innstillinger for AutoPilot-profil
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: conceptual
f1_keywords:
- ZTDProfileSettings
- O365E_ZTDProfileSettings
- BCS365_ZTDProfileSettings
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
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 99bfbf81-e719-4630-9b0f-c187edfa1f8a
description: AutoPilot profiler hjelper deg med å styre hvordan Windows blir installert på Brukerenheter. Profilene inneholder standard og valgfrie innstillinger som hopper Cortana installasjon.
ms.openlocfilehash: d43a15e5f3dc83596b5c23dd0ceb416b24810298
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: MT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/23/2019
ms.locfileid: "32276945"
---
# <a name="about-autopilot-profile-settings"></a><span data-ttu-id="f570d-104">Om innstillinger for AutoPilot-profil</span><span class="sxs-lookup"><span data-stu-id="f570d-104">About AutoPilot Profile settings</span></span>

## <a name="autopilot-profile-settings"></a><span data-ttu-id="f570d-105">AutoPilot profilinnstillinger</span><span class="sxs-lookup"><span data-stu-id="f570d-105">AutoPilot profile settings</span></span>

<span data-ttu-id="f570d-106">Du kan styre hvordan Windows blir installert på Brukerenheter ved hjelp av AutoPilot-profiler.</span><span class="sxs-lookup"><span data-stu-id="f570d-106">You can control how Windows gets installed on user devices by using the AutoPilot profiles.</span></span> <span data-ttu-id="f570d-107">Profilene inneholder følgende innstillinger.</span><span class="sxs-lookup"><span data-stu-id="f570d-107">The profiles contain the following settings.</span></span>
  
 <span data-ttu-id="f570d-108">**AutoPilot standard funksjoner (obligatorisk) som er angitt automatisk:**</span><span class="sxs-lookup"><span data-stu-id="f570d-108">**AutoPilot default features (required) that are set automatically:**</span></span>
  
|<span data-ttu-id="f570d-109">**Innstilling**</span><span class="sxs-lookup"><span data-stu-id="f570d-109">**Setting**</span></span>|<span data-ttu-id="f570d-110">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="f570d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f570d-111">Hoppe over Cortana, OneDrive og OEM-registrering</span><span class="sxs-lookup"><span data-stu-id="f570d-111">Skip Cortana, OneDrive and OEM registration</span></span>  <br/> |<span data-ttu-id="f570d-112">Hopper over installasjonen av forbruker apps som Cortana og personlige OneDrive.</span><span class="sxs-lookup"><span data-stu-id="f570d-112">Skips the installation of consumer apps like Cortana and personal OneDrive.</span></span> <span data-ttu-id="f570d-113">Enhet-brukere kan installere disse senere så lenge han eller hun er en lokal administrator på enheten.</span><span class="sxs-lookup"><span data-stu-id="f570d-113">The device user can install these later as long as he or she is a local admin on the device.</span></span> <span data-ttu-id="f570d-114">Den opprinnelige produsent-registreringen er hoppet over fordi enheten blir administrert av Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="f570d-114">The original manufacturer registration is skipped because the device will be managed by Microsoft 365 Business.</span></span>  <br/> |
|<span data-ttu-id="f570d-115">Logg på erfaring med produsenten selskap</span><span class="sxs-lookup"><span data-stu-id="f570d-115">Sign in experience with your company brand</span></span>  <br/> |<span data-ttu-id="f570d-116">Hvis firmaet har en [legge til firmaets merking i Office 365 påloggingssiden](https://support.office.com/article/a1229cdb-ce19-4da5-90c7-2b9b146aef0a), får brukeren enheten problem når du logger på.</span><span class="sxs-lookup"><span data-stu-id="f570d-116">If your company has a [Add your company branding to Office 365 Sign In page](https://support.office.com/article/a1229cdb-ce19-4da5-90c7-2b9b146aef0a), the device user will get that experience when signing in.</span></span>  <br/> |
|<span data-ttu-id="f570d-117">MDM automatisk registrering med konfigurerte AAD kontoer.</span><span class="sxs-lookup"><span data-stu-id="f570d-117">MDM auto-enrollment with configured AAD accounts.</span></span>  <br/> |<span data-ttu-id="f570d-118">Brukeridentiteten blir administrert av Azure Active directory, og brukerne vil logge deg på Windows og Office 365 med legitimasjonen Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="f570d-118">The user identity will be managed by Azure Active directory, and the users will sign into Windows and Office 365 with their Microsoft 365 Business credentials.</span></span>  <br/> |
   
 <span data-ttu-id="f570d-119">**Valgfrie innstillinger:**</span><span class="sxs-lookup"><span data-stu-id="f570d-119">**Optional settings:**</span></span>
  
|<span data-ttu-id="f570d-120">**Innstilling**</span><span class="sxs-lookup"><span data-stu-id="f570d-120">**Setting**</span></span>|<span data-ttu-id="f570d-121">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="f570d-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f570d-122">Hoppe over personverninnstillingene (deaktivert som standard)</span><span class="sxs-lookup"><span data-stu-id="f570d-122">Skip privacy settings (Off by default)</span></span>  <br/> |<span data-ttu-id="f570d-123">Hvis dette alternativet er satt til **på**, vil enheten brukeren ikke se lisensavtalen for enheten og Windows når han eller hun først logger på.</span><span class="sxs-lookup"><span data-stu-id="f570d-123">If this option is set to **On**, the device user will not see the license agreement for the device and Windows when he or she first signs in.</span></span>  <br/> |
|<span data-ttu-id="f570d-124">Ikke Tillat brukeren å bli den lokale administratoren</span><span class="sxs-lookup"><span data-stu-id="f570d-124">Don't allow the user to become the local admin</span></span>  <br/> |<span data-ttu-id="f570d-125">Hvis dette alternativet er satt til **på**, er ikke enheten brukeren kan installere eventuelle personlige programmer, for eksempel Cortana.</span><span class="sxs-lookup"><span data-stu-id="f570d-125">If this option is set to **On**, the device user will not be able to install any personal apps, such as Cortana.</span></span>  <br/> |
   
