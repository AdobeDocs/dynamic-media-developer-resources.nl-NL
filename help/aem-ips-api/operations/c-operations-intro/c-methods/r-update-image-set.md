---
description: Hiermee werkt u een afbeeldingsset bij.
seo-description: Hiermee werkt u een afbeeldingsset bij.
seo-title: updateImageSet
solution: Experience Manager
title: updateImageSet
topic: Scene7 Image Production System API
uuid: df118ba3-d86f-4005-928e-76a5a9f899fc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateImageSet{#updateimageset}

Hiermee werkt u een afbeeldingsset bij.

Syntaxis

## Parameters {#section-3be47dbbce474ce78676b05e163492e3}

**Input (updateImageSetParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep naar het bedrijf dat de afbeeldingsset bevat die u wilt wijzigen. |
| ` *`assetHandle`*` | `xsd:string` | Ys | De handgreep van de afbeeldingsset die u wilt wijzigen. |
| ` *`memberArray`*` | `types:ImageSetMemberUpdateArray` | Nee | Hiermee worden de leden van de afbeeldingsset opnieuw ingesteld. |
| ` *`thumbAssetHandle`*` | `xsd:string` | Nee | De handgreep van het element dat fungeert als miniatuur voor de afbeeldingsset. |

**Output (updateImageSetReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`opeenvolging`*` |  |  |  |

## Voorbeelden {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Verzoek**

```java
<updateImageSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|381</assetHandle> 
  <memberArray> 
    <items> 
      <assetHandle>a|374</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|375</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|376</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
  </memberArray> 
  <thumbAssetHandle>a|376</thumbAssetHandle> 
</updateImageSetParam>
```

**Antwoord**

```java
<updateImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```

