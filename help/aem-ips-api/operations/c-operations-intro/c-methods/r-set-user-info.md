---
description: Hiermee stelt u gebruikerskenmerken in (bijvoorbeeld naam, e-mail, rol, enz.)
seo-description: Hiermee stelt u gebruikerskenmerken in (bijvoorbeeld naam, e-mail, rol, enz.)
seo-title: setUserInfo
solution: Experience Manager
title: setUserInfo
uuid: 52e3a21e-1dd5-4f9d-b460-506d280fff47
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# setUserInfo{#setuserinfo}

Hiermee stelt u gebruikerskenmerken in (bijvoorbeeld naam, e-mail, rol, enz.)

Syntaxis

## Toegestane gebruikerstypen {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-71b457921fe74acb862a1e112e550211}

**Input (setUserInfoParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Nee | Gebruikershandgreep. |
| `*`firstName`*` | `xsd:string` | Ja | Voornaam. |
| `*`lastName`*` | `xsd:string` | Ja | Achternaam. |
| `*`email`*` | `xsd:string` | Ja | E-mailadres gebruiker. |
| `*`defaultRole`*` | `xsd:string` | Ja | Plaatst de rol voor een gebruiker in elk bedrijf zij tot behoren. De rol `IpsAdmin` negeert echter andere instellingen per bedrijf. |
| `*`passwordExpires`*` | `xsd:dateTime` | Nee | Vervaldatum wachtwoord van set. |
| `*`isValid`*` | `xsd:boolean` | Ja | Hiermee wordt bepaald of de gebruiker een geldige IPS-gebruiker is. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Ja | Een array met bedrijfshandgrepen. |

**Output (setUserInfoReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-272c103076fb4de0a53729e2f6bfb895}

**Verzoek**

```java
<setUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <firstName>test</firstName>
   <lastName>test</lastName>
   <email>test@test.test</email>
   <defaultRole>IpsAdmin</defaultRole>
   <isValid>true</isValid>
</setUserInfoParam>
```

**Antwoord**

Geen.
