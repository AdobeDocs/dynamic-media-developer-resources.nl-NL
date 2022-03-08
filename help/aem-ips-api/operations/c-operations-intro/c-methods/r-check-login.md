---
description: Controleert of een gebruiker met een specifiek bedrijf (geïdentificeerd door greep), e-mailadres, en wachtwoord zich kan aanmelden.
solution: Experience Manager
title: checkLogin
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f96f376-574c-464b-9c89-c215f6454b81
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# checkLogin{#checklogin}

Controleert of een gebruiker met een specifiek bedrijf (geïdentificeerd door greep), e-mailadres, en wachtwoord zich kan aanmelden.

>[!NOTE]
>
>Als het bedrijfshandvat wordt weggelaten, controleert deze methode login van de standaardgebruiker.

## Geautoriseerde gebruikerstypen {#section-df8b26b550854f899948276adaca083a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-1ad4c0b4803b4388aedd655030676cb3}

**Invoer (checkLoginParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Nee | De handgreep aan het bedrijf dat de gebruiker bevat. |
| email | `xsd:string` | Ja | Het e-mailadres van de gebruiker. |
| password | `xsd:string` | Ja | Het wachtwoord van de gebruiker. |

**Uitvoer (checkLoginParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| status | `xsd:string` | Ja | Aanmeldingsstatus van gebruiker. |

## Voorbeelden {#section-23f90100a9d94bc7b4045634cccd1b98}

Deze steekproefcode gebruikt een parameter van het bedrijfshandvat, e-mailadres, en een wachtwoord om te bepalen als een gebruiker aan IPS kan login. Als de gebruiker *kan* login, deze methode keert het koord terug, `ValidLogin`. Als de gebruiker *kan* login, deze methode keert het koord terug, `InvalidLogin`.

**Verzoek**

```java
<ns1:checkLoginParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>137</ns1:companyHandle>
   <ns1:email>juser3@scene7.com</ns1:email>
   <ns1:password>welcome</ns1:password>
</ns1:checkLoginParam>
```

**Antwoord**

```java
<ns1:checkLoginReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:status>InvalidLogin</ns1:status>
</ns1:checkLoginReturn>
```
