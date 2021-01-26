---
description: Hiermee verwijdert u elementen uit een project. De activa worden niet vernietigd.
seo-description: Hiermee verwijdert u elementen uit een project. De activa worden niet vernietigd.
seo-title: removeProjectAssets
solution: Experience Manager
title: removeProjectAssets
topic: Dynamic Media Image Production System API
uuid: bae09dc3-4328-4264-8fb2-e4f0c53546eb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---


# removeProjectAssets{#removeprojectassets}

Hiermee verwijdert u elementen uit een project. De activa worden niet vernietigd.

Syntaxis

## Toegestane gebruikerstypen {#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-169d8e317417415b87df86242f65710e}

**Input (removeProjectAssetsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf met de activa u wilt bewegen. |
| `*`projectHandle`*` | `xsd:string` | Ja | De handgreep naar de projectelementen die u wilt verplaatsen. |
| `*`assetHandleArray`*` | `types:HandleArray` | Ja | Array van handgrepen naar de elementen die u wilt verplaatsen. |

**Output (removeProjectAssetsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Ja | Elementen tellen is verwijderd. |
| `*`warningCount`*` | `xsd:int` | Ja | Het aantal waarschuwingen dat wordt gegenereerd wanneer de bewerking heeft geprobeerd elementen uit het project te verwijderen. |
| `*`errorCount`*` | `xsd:int` | Ja | Het aantal fouten dat wordt gegenereerd toen de bewerking probeerde elementen uit het project te verwijderen. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nee | De array met details die zijn gekoppeld aan de elementen die waarschuwingen hebben gegenereerd toen de bewerking probeerde deze te verwijderen uit het project. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nee | De array met details die zijn gekoppeld aan de elementen die fouten genereerden toen de bewerking probeerde deze te verwijderen uit het project. |

## Voorbeelden {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

Deze codesteekproef verwijdert 2 activa uit een project (die door projecthandvat wordt gespecificeerd).

**Verzoek**

```java
<removeProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
      <items>a|739|1|537</items>
   </assetHandleArray>
</removeProjectAssetsParam>
```

