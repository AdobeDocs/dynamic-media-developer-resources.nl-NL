---
description: Hiermee herstelt u elementen van de prullenbak.
solution: Experience Manager
title: restoreAssetsFromTrash
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b1cde1a9-d726-4ebc-9d49-ee72a6b56fc9
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# restoreAssetsFromTrash{#restoreassetsfromtrash}

Hiermee herstelt u elementen van de prullenbak.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-15e887782c7d4ace897ff02c6ad5baa0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-200a61d040c94e489a85241b29cd499a}

**Input (restoreAssetsFromTrashParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep naar een bedrijf met de middelen die u wilt herstellen. |
| `*`assetHandleArray`*` | `types:HandleArray` | Ja | Array met handgrepen voor de elementen die u wilt herstellen. |

**Output (restoreAssetsFromTrashReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Ja | Aantal elementen dat is verwijderd uit de prullenbak. |
| `*`warningCount`*` | `xsd:int` | Ja | Het aantal waarschuwingen dat wordt gegenereerd wanneer de bewerking probeerde elementen uit de prullenbak te herstellen. |
| `*`errorCount`*` | `xsd:int` | Ja | Het aantal fouten dat wordt gegenereerd wanneer wordt geprobeerd elementen uit de prullenbak te herstellen. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nee | De array met details die zijn gekoppeld aan de elementen die waarschuwingen hebben gegenereerd toen de bewerking probeerde elementen van de prullenbak te herstellen. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nee | De array met details die zijn gekoppeld aan de elementen die fouten genereerden toen de bewerking probeerde elementen van de prullenbak te herstellen. |

## Voorbeelden {#section-98fe0394b0634ca397c395f14f8a9358}

In dit codevoorbeeld worden elementen uit de prullenbak hersteld. De reactie geeft aan dat de bewerking is voltooid.

**Verzoek**

```java
<restoreAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</restoreAssetsFromTrashParam>
```

**Antwoord**

```java
<restoreAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</restoreAssetsFromTrashReturn
```
