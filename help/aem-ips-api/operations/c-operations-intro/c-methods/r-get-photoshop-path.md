---
description: Retourneert coördinaten voor de vierhoek die het benoemde Photoshop-pad omsluit.
seo-description: Retourneert coördinaten voor de vierhoek die het benoemde Photoshop-pad omsluit.
seo-title: getPhotoshopPath
solution: Experience Manager
title: getPhotoshopPath
topic: Scene7 Image Production System API
uuid: e3ed4888-18db-40bc-a1db-f44a342d0293
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---


# getPhotoshopPath{#getphotoshoppath}

Retourneert coördinaten voor de vierhoek die het benoemde Photoshop-pad omsluit.

Syntaxis

## Toegestane gebruikerstypen {#section-c417a287612847cb98dd0aa9c67fd78a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## Parameters {#section-ebffe496284c4ced9f329f78127be199}

**Invoer (getPhotoshopPathParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Verwerk het bedrijf met de afbeelding waarmee u wilt werken. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Verwerk het afbeeldingselement. |
| ` *`pathName`*` | `xsd:string` | Ja | Naam van het Photoshop-pad dat u wilt retourneren. |

**Uitvoer (getPhotoshopPathReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`perspectiveQuad`*` | `types:PerspectiveQuad` | Ja | Retourneert afbeeldingscoördinaten op basis van het pad. Zie [PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204). |

## Voorbeelden {#section-1f0461cbdc184c8d8925336d5279db47}

**Verzoek**

```java
<getPhotoshopPathParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
  <pathName>Face Path</pathName>
</getPhotoshopPathParam>
```

**Antwoord**

```java
<getPhotoshopPathReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <perspectiveQuad>
    <x0>932.19</x0>
    <y0>296.592</y0>
    <x1>968.769</x1>
    <y1>320.16</y1>
    <x2>1119.56</x2>
    <y2>1200.0</y2>
    <x3>900.43</x3>
    <y3>1200.0</y3>
  </perspectiveQuad>
</getPhotoshopPathReturn>
```

>[!MORELIKETHIS]
>
>* [PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204)

