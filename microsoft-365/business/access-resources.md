---
title: Få tilgang til lokale ressurser fra en Azure AD-sammenføyd enhet i Microsoft 365 Business
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
description: Lær hvordan du får tilgang til lokale ressurser, for eksempel bransjeapper, delte filer og skrivere fra en Azure Active Directory-enhet som er med i Windows 10.
ms.openlocfilehash: b78509d72cbd9b3c121039c4965625bf5c21c7e0
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2021
ms.locfileid: "50913526"
---
# <a name="access-on-premises-resources-from-an-azure-ad-joined-device-in-microsoft-365-business-premium"></a>Få tilgang til lokale ressurser fra en Azure AD-sammenføyd enhet i Microsoft 365 Business Premium

Denne artikkelen gjelder for Microsoft 365 Business Premium.

Alle Windows 10-enheter som er med i Azure Active Directory, har tilgang til alle skybaserte ressurser, for eksempel Microsoft 365-appene dine, og kan beskyttes av Microsoft 365 Business Premium. Du kan også gi tilgang til lokale ressurser, for eksempel bransjeapper (LOB), delte filressurser og skrivere. Hvis du vil tillate tilgang, kan du [bruke Azure AD Connect](/azure/active-directory/connect/active-directory-aadconnect) til å synkronisere den lokale Active Directory med Azure Active Directory. 

Hvis du vil ha mer informasjon, kan du se [Innføring i enhetsbehandling i Azure Active Directory](/azure/active-directory/device-management-introduction).
Trinnene oppsummeres også i avsnittene nedenfor.
 
## <a name="run-azure-ad-connect"></a>Kjør Azure AD Connect

Fullfør følgende trinn for å aktivere organisasjonens Azure AD-sammenføyde enheter for å få tilgang til lokale ressurser.
  
1. Hvis du vil synkronisere brukere, grupper og kontakter fra lokal Active Directory til Azure Active Directory, kjører du veiviseren for katalogsynkronisering og Azure AD Connect som beskrevet i Konfigurere katalogsynkronisering [for Office 365.](../enterprise/set-up-directory-synchronization.md)
    
2. Når katalogsynkroniseringen er fullført, må du kontrollere at organisasjonens Windows 10-enheter er Azure AD sammenføyd. Dette trinnet gjøres enkeltvis på hver Windows 10-enhet. Se [Konfigurere Windows-enheter for Microsoft 365 Business Premium-brukere](set-up-windows-devices.md) for mer informasjon. 
    
3. Når Windows 10-enhetene er blitt med i Azure AD, må hver bruker starte enhetene på nytt og logge på med Microsoft 365 Business Premium-legitimasjonen. Alle enheter har nå også tilgang til lokale ressurser.
    
Ingen ekstra trinn er nødvendig for å få tilgang til lokale ressurser for Azure AD-sammenføyde enheter. Denne funksjonaliteten er innebygd i Windows 10. 

Hvis du har planer om å logge på AADJ-enheten annet enn passordmetoden, for eksempel PIN/Bio-metrisk via WHFB-påloggingspålogging og deretter få tilgang til lokale ressurser (delte ressurser, skrivere.). osv.), følg https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-hybrid-aadj-sso-base
  
Hvis organisasjonen ikke er klar til å distribuere i konfigurasjonen av azure AD-sammenføyde enheter som er beskrevet ovenfor, bør du vurdere å konfigurere konfigurasjon av [hybrid Azure AD-sammenføyd enhet.](manage-windows-devices.md)
  
### <a name="considerations-when-you-join-windows-devices-to-azure-ad"></a>Vurderinger når du blir med i Windows-enheter til Azure AD

Hvis Windows-enheten du ble med i Azure-AD, tidligere var domeneføyd eller i en arbeidsgruppe, bør du vurdere følgende begrensninger:
  
- Når en enhet Azure AD blir med, opprettes en ny bruker uten å referere til en eksisterende profil. Profiler må overføres manuelt. En brukerprofil inneholder informasjon som favoritter, lokale filer, nettleserinnstillinger og Start-menyinnstillinger. Den beste fremgangsmåten er å finne et tredjepartsverktøy for å tilordne eksisterende filer og innstillinger til den nye profilen.

- Hvis enheten bruker gruppepolicyobjekter (GPO), kan det hende [](/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers) at enkelte gruppepolicyobjekter ikke har en sammenlignbar konfigurasjonstjenesteleverandør (CSP) i Intune. Kjør [MMAT-verktøyet for](https://www.microsoft.com/download/details.aspx?id=45520) å finne sammenlignbare CSP-er for eksisterende gruppepolicyobjekter.

- Brukere kan kanskje ikke godkjenne til programmer som er avhengige av Active Directory-godkjenning. Evaluer den eldre appen, og vurder om mulig å oppdatere til en app som bruker moderne Auth.

- Active Directory-skriveroppdagelse fungerer ikke. Du kan angi direkte skriverbaner for alle brukere eller bruke [Universal Print](/universal-print/).