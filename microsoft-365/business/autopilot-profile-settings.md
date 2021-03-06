---
title: Om innstillinger for AutoPilot-profil
f1.keywords:
- NOCSH
ms.author: efrene
author: efrene
manager: scotv
audience: Admin
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
- OKR_SMB_M365
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 99bfbf81-e719-4630-9b0f-c187edfa1f8a
description: AutoPilot-profiler hjelper deg med å kontrollere hvordan Windows blir installert på brukerenheter. Profilene inneholder standardinnstillinger og valgfrie innstillinger, for eksempel hopp over Cortana-installasjonen.
ms.openlocfilehash: 86f8718131f0a0b93e18e65e39e02e7d65aded1a
ms.sourcegitcommit: 53acc851abf68e2272e75df0856c0e16b0c7e48d
ms.translationtype: MT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2021
ms.locfileid: "51578511"
---
# <a name="about-autopilot-profile-settings"></a>Om innstillinger for AutoPilot-profil

## <a name="autopilot-profile-settings"></a>Innstillinger for AutoPilot-profil

Du kan bruke AutoPilot-profiler til å kontrollere hvordan Windows er installert på brukerenheter. Profilene inneholder følgende innstillinger.
  
 **AutoPilot-standardfunksjoner (obligatorisk) som angis automatisk:**
  
|**Innstilling**|**Beskrivelse**|
|:-----|:-----|
|Hopp over Cortana-, OneDrive- og OEM-registrering  <br/> |Hopper over installasjonen av forbrukerapper som Cortana og personlig OneDrive. Enhetsbrukeren kan installere disse senere så lenge brukeren er lokal administrator på enheten. Den opprinnelige produsentregistreringen hoppes over fordi enheten administreres av Microsoft 365 Business Premium.  <br/> |
|Logg på-opplevelsen med firmamerket ditt  <br/> |Hvis firmaet har siden Legg til firmamerking i [Påloggingsside for Microsoft 365,](../admin/setup/customize-sign-in-page.md)får enhetsbrukeren denne opplevelsen når du logger på.  <br/> |
|MDM automatisk registrering med konfigurerte AAD-kontoer.  <br/> |Brukeridentiteten administreres av Azure Active Directory, og brukere logger seg på Windows og Microsoft 365 med microsoft 365 Business Premium-legitimasjonen sin.  <br/> |
   
 **Valgfrie innstillinger:**
  
|**Innstilling**|**Beskrivelse**|
|:-----|:-----|
|Hopp over personverninnstillinger (av som standard)  <br/> |Hvis dette alternativet er satt til **På**, vil ikke enhetsbrukeren se lisensavtalen for enheten og Windows når han eller hun logger på for første gang.  <br/> |
|Ikke tillat brukeren å bli lokal administrator  <br/> |Hvis dette alternativet er satt til **På**, kan ikke enhetsbrukeren installere noen personlige apper, for eksempel Cortana.<br/> |
