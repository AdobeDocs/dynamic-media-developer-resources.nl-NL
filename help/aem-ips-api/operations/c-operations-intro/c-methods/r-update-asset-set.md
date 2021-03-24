---
description: Hiermee werkt u een elementenset bij.
solution: Experience Manager
title: updateAssetSet
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# updateAssetSet{#updateassetset}

Hiermee werkt u een elementenset bij.

Syntaxis

## Parameters {#section-d7080ccd97334c94860eb107a3e132b2}

**Input (updateAssetSetParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep naar het bedrijf dat de afbeeldingsset bevat die u wilt wijzigen. |
| `*`assetHandle`*` | `xsd:string` | Ja | De handgreep van de afbeeldingsset die u wilt wijzigen. |
| `*`setDefinition`*` | `xsd:string` | Nee | Hiermee worden de leden van de afbeeldingsset opnieuw ingesteld. |
| `*`thumbAssetHandle`*` | `xsd:string` | Nee | De handgreep van het element dat fungeert als miniatuur voor de afbeeldingsset. |

**Uitvoer (updateAssetSetReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
|  |  |  |  |

## Voorbeelden {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Verzoek**

```java
<updateAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|535</assetHandle> 
  <setDefinition>${getCatalogId([a|202])};${getCatalogId([a|202])};advanced_image;,${getCatalogId([a|935])};${getCatalogId([a|935])};advanced_image;,${getCatalogId([a|933])};${getCatalogId([a|933])};advanced_image;</setDefinition> 
  <thumbAssetHandle>a|202</thumbAssetHandle> 
</updateAssetSetParam>
```

**Antwoord**

```java
<updateAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```

