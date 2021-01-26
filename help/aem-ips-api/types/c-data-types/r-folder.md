---
description: Hierarchische bestands- of elementopslagobjecten. Mappen kunnen een (of meer) submappen bevatten.
seo-description: Hierarchische bestands- of elementopslagobjecten. Mappen kunnen een (of meer) submappen bevatten.
seo-title: Map
solution: Experience Manager
title: Map
topic: Dynamic Media Image Production System API
uuid: 8ba8d9cb-c4e5-423c-b8cb-ba8751952771
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '86'
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

