---
description: Verplaatst middelen naar een specifieke omslag.
seo-description: Verplaatst middelen naar een specifieke omslag.
seo-title: moveAsset
solution: Experience Manager
title: moveAsset
topic: Scene7 Image Production System API
uuid: cabeb7b7-ab0b-44d0-ad90-623f76e4323d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# moveAsset{#moveasset}

Verplaatst middelen naar een specifieke omslag.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-e4f2d2a58132450aa36da6377134211e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-dd0bbdf293aa4563af70a91f97c861f1}

**Input (moveAssetParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handgreep aan het bedrijf. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Verwerk het element dat u wilt verplaatsen. |
| ` *`folderHandle`*` | `xsd:string` | Ja | Handgreep aan de bestemmingsomslag. |

**Uitvoer (moveAssetReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-78333769f4f14e2886fdf06433c9d2ad}

In dit codevoorbeeld wordt een element naar een map verplaatst.

**Verzoek**

```java
<ns1:moveAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24266|1|17062</ns1:assetHandle>
   <ns1:folderHandle>MyCompany/My New Images/</ns1:folderHandle>
</ns1:moveAssetParam>
```

**Antwoord**

Geen.
