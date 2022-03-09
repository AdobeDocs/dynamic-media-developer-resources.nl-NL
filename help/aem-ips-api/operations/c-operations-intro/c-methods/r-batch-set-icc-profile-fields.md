---
description: Hiermee stelt u metagegevensvelden voor ICC-profielen in.
solution: Experience Manager
title: batchSetIccProfileFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d10a30ca-afa7-4ef0-8cef-0329b0068bf3
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# batchSetIccProfileFields{#batchseticcprofilefields}

Hiermee stelt u metagegevensvelden voor ICC-profielen in.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-f6f7caf9434b4f469518dab64b76c0f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-75a02b55ae0d444ca26b59aac6e86d6f}

**Input (batchSetIccProfileFields)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Verwerk het bedrijf dat de ICC-profielen bevat. |
| update-array | `xsd:string` | Ja | Array van ICC-profielupdates. |

**Output (batchSetIccProfileFields)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| successCount | `xsd:int` | Ja | Het aantal ICC-profielvelden is ingesteld. |
| warningCount | `xsd:int` | Ja | Het aantal waarschuwingen dat wordt gegenereerd wanneer de bewerking probeerde de ICC-profielvelden in te stellen. |
| errorCount | `xsd:int` | Ja | Het aantal fouten dat wordt gegenereerd wanneer de bewerking probeerde de ICC-profielvelden in te stellen. |
| warningDetailArray | `types:AssetOperationFaultArray` | Nee | De array met details die zijn gekoppeld aan de elementen die waarschuwingen hebben gegenereerd toen de bewerking probeerde de updates toe te passen. |
| errorDetailArray | `types:AssetOperationFaultArray` | Nee | De array met details die zijn gekoppeld aan de elementen die fouten genereerden toen de bewerking probeerde de updates toe te passen. |

## Voorbeelden {#section-5dc90cfbd9b1411485b44859032f7cb9}

**Verzoek**

```java {.line-numbers}
<batchSetIccProfileFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|1808|13|169</assetHandle>
         <class>Output</class>
         <colorSpace>CMYK</colorSpace>
         <pcsType>Luv</pcsType>
      </items>
   </updateArray>
</batchSetIccProfileFieldsParam>
```

**Antwoord**

```java {.line-numbers}
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```
