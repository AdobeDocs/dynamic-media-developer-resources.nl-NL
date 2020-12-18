---
description: Hiermee stelt u metagegevensvelden voor lettertypen in.
seo-description: Hiermee stelt u metagegevensvelden voor lettertypen in.
seo-title: batchSetFontFields
solution: Experience Manager
title: batchSetFontFields
topic: Scene7 Image Production System API
uuid: 0209865e-32b3-4bea-a508-05771a0365e1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# batchSetFontFields{#batchsetfontfields}

Hiermee stelt u metagegevensvelden voor lettertypen in.

## Toegestane gebruikerstypen {#section-89eff13b5ed54cddb87b1304ba4eff0e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-836f5948d00a46e98ccb62f0573e4e68}

**Input (batchSetFontFieldsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handle aan het bedrijf dat de doopvonten bevat. |
| ` *`updateArray`*` | `types:FontFieldUpdateArray` | Ja | Array met updates van lettertypevelden. |

**Output (batchSetFontFieldsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Het aantal lettertypevelden is ingesteld. |
| ` *`warningCount`*` | `xsd:int` | Ja | Het aantal waarschuwingen dat wordt gegenereerd wanneer de bewerking heeft geprobeerd lettertypevelden in te stellen. |
| ` *`errorCount`*` | `xsd:int` | Ja | Het aantal fouten dat wordt gegenereerd wanneer de bewerking heeft geprobeerd lettertypevelden in te stellen. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nee | De array met details die zijn gekoppeld aan de elementen die waarschuwingen hebben gegenereerd toen de bewerking probeerde de updates toe te passen. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nee | De array met details die zijn gekoppeld aan de elementen die fouten genereerden toen de bewerking probeerde de updates toe te passen. |

## Voorbeelden {#section-0449c2e4ec534f4b8ee849ec4fe12c4e}

**Verzoek**

```java
<batchSetFontFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
          <assetHandle>a|450|14|19</assetHandle>
          <fontName>Bookman Old Style Font Name</fontName>
          <postscriptName>Bookman Old Style PostScript</postscriptName>
          <rtfName>Bookman Old Style RTF</rtfName>
          <fontFamily>Bookman Old Style Family</fontFamily>
          <style>BoldItalic</style>
          <typeName>Open Type</typeName><type>OTF</type>
      </items>
   </updateArray>
</batchSetFontFieldsParam>
```

**Antwoord**

```java
<batchSetFontFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetFontFieldsReturn>
```

