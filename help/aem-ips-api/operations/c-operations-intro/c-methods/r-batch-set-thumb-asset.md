---
description: Hiermee stelt u de miniatuurafbeelding in voor een of meer elementen.
seo-description: Hiermee stelt u de miniatuurafbeelding in voor een of meer elementen.
seo-title: batchSetThumbAsset
solution: Experience Manager
title: batchSetThumbAsset
topic: Scene7 Image Production System API
uuid: 16c298a7-bb07-4643-824b-8f864d7f0290
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---


# batchSetThumbAsset{#batchsetthumbasset}

Hiermee stelt u de miniatuurafbeelding in voor een of meer elementen.

Syntaxis

## Miniatuurmiddeltypen {#section-4edc2a6a8f824213b0aaddb1d437268c}

Toegestane elementtypen voor miniaturen bestaan uit de volgende elementen:

* Afbeelding
* AdjustedView
* Masker
* Sjabloon
* PSDTemplate

## Toegestane gebruikerstypen {#section-5fc988e3d6384968b86fd9fe363658c0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>De gebruiker moet lees-/schrijftoegang tot het doelelement hebben en toegang tot het blokelement lezen.

## Parameters {#section-9c6efa000b384b3db6c013def20cf40b}

**Input (batchSetThumbAssetParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf dat de activa bevat. |
| ` *`updateArray`*` | `types:ThumbAssetUpdateArray` | Ja | De array met updates. |

**Output (batchSetThumbAssetParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Het aantal correct ingestelde miniaturen. |
| ` *`warningCount`*` | `xsd:int` | Ja | Het aantal waarschuwingen dat wordt gegenereerd wanneer de bewerking heeft geprobeerd de miniaturen in te stellen. |
| ` *`errorCount`*` | `xsd:int` | Ja | Het aantal fouten dat wordt gegenereerd toen de bewerking probeerde de miniaturen in te stellen. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nee | De array met details die zijn gekoppeld aan de elementen die waarschuwingen hebben gegenereerd toen de bewerking probeerde de updates toe te passen. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nee | De array met details die zijn gekoppeld aan de elementen die fouten genereerden toen de bewerking probeerde de updates toe te passen. |

## Voorbeelden {#section-6de69a8680c24c1486c5f01488393381}

**Verzoek**

```java
<batchSetThumbAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|234</assetHandle>
         <thumbAssetHandle>a|189</thumbAssetHandle>
      </items>
   </updateArray>
```

**Antwoord**

```java
<batchSetThumbAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetThumbAssetReturn>
```

