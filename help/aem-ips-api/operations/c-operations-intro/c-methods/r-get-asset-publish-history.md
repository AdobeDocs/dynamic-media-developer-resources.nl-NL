---
description: Retourneert de publicatiegeschiedenis voor een element.
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---


# getAssetPublishHistory{#getassetpublishhistory}

Retourneert de publicatiegeschiedenis voor een element.

Syntaxis

## Toegestane gebruikerstypen {#section-3b9d6a129093458fa8890139a2718912}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-3541bd9914a44b89acfc1d419b560ee6}

**Input (getAssetPublishHistoryParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf met de activa publicatiegeschiedenis. |
| `*`assetHandle`*` | `xsd:string` | Ja | Het element met de publicatiegeschiedenis die u wilt onderzoeken. |

**Output (getAssetPublishHistoryReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`pubHistoryArray`*` | `types:PublishHistoryArray` | Ja | De publicatiegeschiedenis van het element. |

## Voorbeelden {#section-53897c51e5a047c5bd5ea5a6efb2d114}

Dit codevoorbeeld retourneert de publicatiegeschiedenis van een element. Er is nooit een element gepubliceerd als de server een lege array retourneert.

**Verzoek**

```java
<getAssetPublishHistoryParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetPublishHistoryParam>
```

**Antwoord**

```java
<getAssetPublishHistoryReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <pubHistoryArray/>
</getAssetPublishHistoryReturn>
```

