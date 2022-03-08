---
description: Hiermee stelt u afbeeldingsspecifieke velden in voor een of meer afbeeldingselementen.
solution: Experience Manager
title: batchSetImageFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8ea6dbb8-4d32-43e5-961f-31110f983663
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# batchSetImageFields{#batchsetimagefields}

Hiermee stelt u afbeeldingsspecifieke velden in voor een of meer afbeeldingselementen.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-6b087bdcb7874c13acf76e113a093054}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-4969815cf67c4d11b13bb2017b3604e8}

**Input (batchSetImageFields)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | De handgreep naar het bedrijf dat de afbeeldingselementen bevat. |
| updateArray | `types:ImageFieldUpdateArray` | Ja | De array van afbeeldingsvelden wordt bijgewerkt. |

**Output (batchSetImageFields)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| successCount | `xsd:int` | Ja | Het aantal correct ingestelde afbeeldingsvelden. |
| warningCount | `xsd:int` | Ja | Het aantal waarschuwingen dat wordt gegenereerd wanneer de bewerking heeft geprobeerd de afbeeldingsvelden in te stellen. |
| errorCount | `xsd:int` | Ja | Het aantal fouten dat wordt gegenereerd toen de bewerking probeerde de afbeeldingsvelden in te stellen. |
| warningDetailArray | `types:AssetOperationFaultArray` | Nee | De array met details die zijn gekoppeld aan de elementen die waarschuwingen hebben gegenereerd toen de bewerking probeerde de updates toe te passen. |
| errorDetailArray | `types:AssetOperationFaultArray` | Nee | De array met details die zijn gekoppeld aan de elementen die fouten genereerden toen de bewerking probeerde de updates toe te passen. |

## Voorbeelden {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

In dit voorbeeld worden gegevens ingesteld in de velden van twee afbeeldingen in een updatearray. In de array worden de afbeeldingen aangegeven met de elementhandgrepen en bevatten ze de resolutie in pixels, de ankercoördinaten voor de x- en y-positie en gebruikersgegevens. Het antwoord geeft aan dat velden voor beide afbeeldingen correct zijn ingesteld.

**Verzoek**

```java
<batchSetImageFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|140626|1|102524</assetHandle>
         <resolution>72</resolution>
         <anchorX>50</anchorX>
         <anchorY>100</anchorY>
         <userData>nada1</userData>
      </items>
      <items>
         <assetHandle>a|96680|1|64865</assetHandle>
         <resolution>150</resolution>
         <anchorX>100</anchorX>
         <anchorY>50</anchorY>
         <userData>nada2</userData>
      </items>
   </updateArray>
</batchSetImageFieldsParam>
```

**Antwoord**

```java
<batchSetImageFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetImageFieldsReturn>
```
