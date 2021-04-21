---
description: Hiermee voegt u een of meer elementen aan een project toe.
solution: Experience Manager
title: addProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---


# addProjectAssets{#addprojectassets}

Hiermee voegt u een of meer elementen aan een project toe.

Syntaxis

## Toegestane gebruikerstypen {#section-c67e7422921047f4ab4d4e9ba5a7aafe}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-20d498e971b6466298e60c8a77fc32b2}

**Input (addProjectAssetsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handgreep aan het bedrijf verbonden aan het huidige project. |
| `*`projectHandle`*` | `xsd:string` | Ja | Verwerk het project waaraan u elementen toevoegt. |
| `*`projectHandleArray`*` | `xsd:HandleArray` | Ja | Array met elementen die u toevoegt aan het huidige project. |

**Output (addProjectAssetsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Ja | Het aantal elementen dat is toegevoegd. |
| `*`warningCount`*` | `xsd:int` | Ja | Het aantal waarschuwingen dat wordt gegenereerd wanneer de bewerking heeft geprobeerd elementen aan een project toe te voegen. |
| `*`errorCount`*` | `xsd:int` | Ja | Het aantal fouten dat is gegenereerd toen de bewerking probeerde elementen toe te voegen aan een project. |
| `*`warningDetailHandle`*` | `xsd:AssetOperationFaultArray` | Nee | Array met waarschuwingen die door elementen worden gegenereerd wanneer de bewerking probeerde deze aan een project toe te voegen. |
| `*`companyHandle`*` | `xsd:AssetOperationFaultArray` | Nee | Array met fouten die door elementen worden gegenereerd wanneer de bewerking probeerde deze toe te voegen aan een project. |

## Voorbeelden {#section-bee5be2402f54cb9a3a02cc07def4135}

In dit voorbeeld wordt één element (waarnaar wordt verwezen door de greep ervan) toegevoegd aan een element handle array aan een project dat in de aanvraag is opgegeven. De bewerking is voltooid wanneer de reactie `successCount` `1` retourneert.

**Verzoek**

```java
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**Antwoord**

```java
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```

