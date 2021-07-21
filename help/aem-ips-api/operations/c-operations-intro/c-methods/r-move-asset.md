---
description: Verplaatst middelen naar een specifieke omslag.
solution: Experience Manager
title: moveAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c5357c1a-92ac-4f9c-957e-b62cb812796c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

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
| `*`companyHandle`*` | `xsd:string` | Ja | Handgreep aan het bedrijf. |
| `*`assetHandle`*` | `xsd:string` | Ja | Verwerk het element dat u wilt verplaatsen. |
| `*`folderHandle`*` | `xsd:string` | Ja | Handgreep aan de bestemmingsomslag. |

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
