---
description: Retourneert alle metagegevensvelden, gegroepeerd op elementtype.
seo-description: Retourneert alle metagegevensvelden, gegroepeerd op elementtype.
seo-title: getAssetMetadataFields
solution: Experience Manager
title: getAssetMetadataFields
topic: Scene7 Image Production System API
uuid: 01d5076f-f187-4069-b2f2-806fb1d8be84
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getAssetMetadataFields{#getassetmetadatafields}

Retourneert alle metagegevensvelden, gegroepeerd op elementtype.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-5dd58970d61d4d4a928e36ffceca6f5e}

**Input (getAssetMetadataFieldsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep naar het bedrijf waarvan u de metagegevens wilt ophalen. |

**Output (getAssetMetadataFieldsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`assetFieldArray`*` | `types:AssetMetadataFieldsArray` | Ja | Array van metagegevensvelden, op elementtype. |

## Voorbeelden {#section-d79ab85f29144635b0b61416e52f4f3f}

**Verzoek**

```java
<getAssetMetadataFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
</getAssetMetadataFieldsParam>
```

**Antwoord**

>[!NOTE]
>
>Afgekort voor bondigheid.

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```

