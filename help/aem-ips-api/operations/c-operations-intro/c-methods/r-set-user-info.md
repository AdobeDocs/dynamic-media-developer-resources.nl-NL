---
description: Hiermee stelt u gebruikerskenmerken in (bijvoorbeeld naam, e-mail, rol, enzovoort.)
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# setUserInfo{#setuserinfo}

Hiermee stelt u gebruikerskenmerken in (bijvoorbeeld naam, e-mail, rol, enzovoort.)

Syntaxis

## Geautoriseerde gebruikerstypen {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-71b457921fe74acb862a1e112e550211}

**Input (setUserInfoParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| userHandle | `xsd:string` | Nee | Gebruikershandgreep. |
| firstName | `xsd:string` | Ja | Voornaam. |
| lastName | `xsd:string` | Ja | Achternaam. |
| email | `xsd:string` | Ja | E-mailadres van gebruiker. |
| defaultRole | `xsd:string` | Ja | Plaatst de rol voor een gebruiker in elk bedrijf zij tot behoren. Noteer echter de `IpsAdmin` de rol treedt andere per-bedrijfmontages met voeten. |
| passwordExpires | `xsd:dateTime` | Nee | Vervaldatum wachtwoord van set. |
| isValid | `xsd:boolean` | Ja | Bepaalt als de gebruiker een geldige IPS gebruiker is. |
| membershipArray | `types:CompanyMembershipUpdateArray` | Ja | Een array met bedrijfshandgrepen. |

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
