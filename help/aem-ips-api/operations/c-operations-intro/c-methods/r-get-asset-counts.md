---
description: Hiermee worden de activa en het aantal activa opgehaald die aan een bepaalde onderneming zijn gekoppeld.
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---


# getAssetCounts{#getassetcounts}

Hiermee worden de activa en het aantal activa opgehaald die aan een bepaalde onderneming zijn gekoppeld.

De geretourneerde `countArray` bestaat uit een array van `assetTypes` (gegevenstype `xsd:string`), elk met een eigen telveld (gegevenstype `xsd:int`), waardoor meerdere elementtypen per element van de array kunnen worden weergegeven.
Syntaxis

## Toegestane gebruikerstypen {#section-6234754722184e828352f10eb18fbce9}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-2a9581315eca427d8a3d26cc3fca7b1f}

**Input (getAssetCountsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep voor het bedrijf met elementen die u wilt tellen. |

**Output (getAssetCountsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`countArray`*` | `types:AssetCountArray` | Nee | Een array van elementtypen, elk met een eigen telveld, waarmee meerdere elementtypen per element van de array kunnen worden weergegeven. |

## Voorbeelden {#section-6052a503eb3843f6adb99e200fdba280}

Deze codesteekproef gebruikt het handvat van het bedrijf als gebied in `getAssetCountsParam` die naar de IPS de dienstenserver van het Web wordt verzonden om de activa tellingen te krijgen.

**Verzoek**

```java
<getAssetCountsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
</getAssetCountsParam>
```

**Antwoord**

```java
<getAssetCountsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <countArray>
      <items>
         <assetType>Image</assetType>
         <count>44</count>
      </items>
      <items>
         <assetType>Flash</assetType>
         <count>3</count>
      </items>
   </countArray>
</getAssetCountsReturn>
```

