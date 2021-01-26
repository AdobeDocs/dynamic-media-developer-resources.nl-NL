---
description: Hiermee stelt u metagegevens van elementen in met de batchmodus.
seo-description: Hiermee stelt u metagegevens van elementen in met de batchmodus.
seo-title: batchSetAssetMetadata
solution: Experience Manager
title: batchSetAssetMetadata
topic: Dynamic Media Image Production System API
uuid: 88d8f279-988f-4956-b66f-60fa95cf511c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# batchSetAssetMetadata{#batchsetassetmetadata}

Hiermee stelt u metagegevens van elementen in met de batchmodus.

Syntaxis

## Toegestane gebruikerstypen {#section-5310d9fd00604cbf9756944900378855}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-7111ac93bc7747f69ba14db4ac3912b0}

**Input (batchSetAssetMetadataParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep naar het bedrijf waarvan u de metagegevens in een batchbewerking wilt instellen. |
| `*`updateArray`*` | `types:BatchMetadataUpdateArray` | Ja | De array met updates van metagegevens die worden toegepast op de elementen. |

**Output (batchSetAssetMetadataParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Ja | Het aantal metagegevens dat is ingesteld. |
| `*`warningCount`*` | `xsd:int` | Ja | Het aantal waarschuwingen dat wordt gegenereerd wanneer de bewerking heeft geprobeerd metagegevens in te stellen. |
| `*`errorCount`*` | `xsd:int` | Ja | Het aantal fouten dat wordt gegenereerd wanneer de bewerking heeft geprobeerd metagegevens in te stellen. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nee | De array met details die zijn gekoppeld aan de elementen die waarschuwingen genereren wanneer de bewerking heeft geprobeerd metagegevens voor de elementen in batches in te stellen. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nee | De array met details die zijn gekoppeld aan de elementen die fouten genereren wanneer de bewerking heeft geprobeerd metagegevens voor de elementen in batches in te stellen. |

## Voorbeelden {#section-2de798ac920e4b47b971b1729a64395b}

**Verzoek**

```java
<batchSetAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
<companyHandle>c|6</companyHandle>
<updateArray>
   <items>
      <assetHandleArray>
         <items>a|743|1|538</items>
         <items>a|744|1|539</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>400</value>
         </items>
      </updateArray>
   </items>
   <items>
      <assetHandleArray>
         <items>a|732|1|535</items>
         <items>a|739|1|537</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>300</value>
         </items>
      </updateArray>
   </items>
</updateArray>
</batchSetAssetMetadataParam>
```

**Antwoord**

```java
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```

