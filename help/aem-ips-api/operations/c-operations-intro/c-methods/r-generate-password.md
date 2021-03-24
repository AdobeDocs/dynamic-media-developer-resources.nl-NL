---
description: Hiermee genereert u een nieuw wachtwoord.
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 0%

---


# generatePassword{#generatepassword}

Hiermee genereert u een nieuw wachtwoord.

Syntaxis

## Toegestane gebruikerstypen {#section-88f7dc11e5c74be281399d8f2e3c9555}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-d516615c906240819a284786efb19863}

**Input (generatePasswordParam)**

Geen.

**Output (generatePasswordParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`password`*` | `xsd:string` | Ja | Een nieuw wachtwoord. |

## Voorbeelden {#section-f580fefdccec46fe95359e3aef0ed17f}

In dit codevoorbeeld wordt een wachtwoord gegenereerd. Dit is ongebruikelijk omdat de aanvraag gewoon een parameter is zonder ingesloten elementen of waarden. IPS keert een sterk wachtwoord terug.

**Verzoek**

```java
<generatePasswordParam xmlns="http://www.scene7.com/IpsApi/xsd">
</generatePasswordParam>
```

**Antwoord**

```java
<generatePasswordReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <password>1\7aQRn]</password>
</generatePasswordReturn>
```

