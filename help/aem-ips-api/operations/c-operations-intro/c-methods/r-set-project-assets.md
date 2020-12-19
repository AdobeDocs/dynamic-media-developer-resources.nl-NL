---
description: Elementen in een project toewijzen of bijwerken.
seo-description: Elementen in een project toewijzen of bijwerken.
seo-title: setProjectAssets
solution: Experience Manager
title: setProjectAssets
topic: Scene7 Image Production System API
uuid: 98d18948-d387-4890-9c27-e8ab60cded1d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---


# setProjectAssets{#setprojectassets}

Elementen in een project toewijzen of bijwerken.

Syntaxis

## Toegestane gebruikerstypen {#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**Input (setProjectAssetsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyName`*` | `xsd:string` | Ja | Bedrijfshandgreep. |
| ` *`projectHandle`*` | `xsd:string` | Ja | Projecthandgreep. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Ja | De array met elementhandgrepen die u aan het project wilt koppelen. |

**Output (setProjectAssetsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Het aantal toegevoegde elementen. |

## Voorbeelden {#section-33c1a909c3dc4aa98da474c23a036596}

Deze codesteekproef wijst activa aan een project toe. Het verzoek retourneert een succesaantal van één.

**Verzoek**

```java
<setProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|739|1|537</items>
   </assetHandleArray>
</setProjectAssetsParam>
```

**Antwoord**

```java
<setProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</setProjectAssetsReturn>
```

