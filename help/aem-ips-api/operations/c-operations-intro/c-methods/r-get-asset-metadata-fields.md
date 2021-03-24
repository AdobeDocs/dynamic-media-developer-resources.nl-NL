---
description: Retourneert alle metagegevensvelden, gegroepeerd op elementtype.
solution: Experience Manager
title: getAssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---


# getAssetMetadataFields{#getassetmetadatafields}

Retourneert alle metagegevensvelden, gegroepeerd op elementtype.

Syntaxis

## Toegestane gebruikerstypen {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

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
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep naar het bedrijf waarvan u de metagegevens wilt ophalen. |

**Output (getAssetMetadataFieldsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`assetFieldArray`*` | `types:AssetMetadataFieldsArray` | Ja | Array van metagegevensvelden, op elementtype. |

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

