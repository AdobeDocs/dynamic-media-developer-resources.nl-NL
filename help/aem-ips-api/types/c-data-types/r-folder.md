---
description: Hierarchische bestands- of elementopslagobjecten. Mappen kunnen een (of meer) submappen bevatten.
seo-description: Hierarchische bestands- of elementopslagobjecten. Mappen kunnen een (of meer) submappen bevatten.
seo-title: Map
solution: Experience Manager
title: Map
uuid: 8ba8d9cb-c4e5-423c-b8cb-ba8751952771
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# Map{#folder}

Hierarchische bestands- of elementopslagobjecten. Mappen kunnen een (of meer) submappen bevatten.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Mapgreep. |
| `*`pad`*` | `xsd:string` | Mappad. |
| `*`lastModified`*` | `xsd:dateTime` | Datum laatste wijziging. |
| `*`childLastModified`*` | `xsd:dateTime` | Laatste wijzigingsdatum voor submappen en onderliggende elementen van mappen. |
| `*`permissionsSetHandle`*` | `xsd:string` | Mapmachtigingen worden afgehandeld. |
| `*`hasSubfolder`*` | `types:Boolean` | Hiermee wordt bepaald of een map submappen heeft. |
| `*`subfolderArray`*` | `types:FolderArray` | Een array van submappen in een map. |

