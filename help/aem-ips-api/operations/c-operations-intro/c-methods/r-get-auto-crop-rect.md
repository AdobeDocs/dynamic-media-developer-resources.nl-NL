---
description: Hiermee wordt een uitgesneden gebied voor een afbeelding geretourneerd op basis van de achtergrondkleur of -transparantie.
solution: Experience Manager
title: getAutoCropRect
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---


# getAutoCropRect{#getautocroprect}

Hiermee wordt een uitgesneden gebied voor een afbeelding geretourneerd op basis van de achtergrondkleur of -transparantie.

Syntaxis

## Toegestane gebruikerstypen {#section-32dfe7bb68764b93ae01e05ff7a7bdd0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-965d5973b8344d43a74b3e07cf0b7eb3}

**Input (getAutoCropRectParam)**

>[!NOTE]
>
>Geef `*`autoColorCropOptions`*` of `*`autoTransparentCropOptions`*` op wanneer u deze methode aanroept.

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf met de activa u wilt werken met. |
| `*`assetHandle`*` | `xsd:string` | Ja | De handgreep naar het element waarmee u wilt werken. |
| `*`autoColorCropOptions`*` | `types:AutoColorCropOptions` | Nee | De snijrechthoek berekenen op basis van kleur. Zie [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6). |
| `*`autoTransparentCropOptions`*` | `types:AutoTransparentCropOptions` | Nee | Snijrechthoek berekenen op basis van transparantie. Zie [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b). |

**Output (getAutoCropRectReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`xOffset`*` | `xsd:int` | Ja | De coördinaat van de beginpixels van het berekende uitsnijdgebied. |
| `*`yOffset`*` | `xsd:int` | Ja | De eerste pixelcoördinaat van het berekende uitsnijdgebied. |
| `*`width`*` | `xsd:int` | Ja | Breedte van het berekende uitsnijdgebied (in pixels). |
| `*`height`*` | `xsd:int` | Ja | Hoogte van het berekende uitsnijdgebied (in pixels). |

## Voorbeelden {#section-ba65bd66086d491cad1cea535954ee1f}

**Verzoek**

```java
<getAutoCropRectParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <companyHandle>c|3578</companyHandle>
  <assetHandle>a|3192146</assetHandle>
  <autoColorCropOptions>
    <corner>UpperLeft</corner>
    <tolerance>0.5</tolerance>
  </autoColorCropOptions>
</getAutoCropRectParam>
```

**Antwoord**

```java
<getAutoCropRectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <xOffset>452</xOffset>
  <yOffset>66</yOffset>
  <width>1271</width>
  <height>1874</height>
</getAutoCropRectReturn>
```

>[!MORELIKETHIS]
>
>* [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)
>* [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)

