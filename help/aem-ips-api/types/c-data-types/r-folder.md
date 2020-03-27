---
description: Hierarchische bestands- of elementopslagobjecten. Mappen kunnen een (of meer) submappen bevatten.
seo-description: Hierarchische bestands- of elementopslagobjecten. Mappen kunnen een (of meer) submappen bevatten.
seo-title: Map
solution: Experience Manager
title: Map
topic: Scene7 Image Production System API
uuid: 8ba8d9cb-c4e5-423c-b8cb-ba8751952771
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Map{#folder}

Hierarchische bestands- of elementopslagobjecten. Mappen kunnen een (of meer) submappen bevatten.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | Mapgreep. |
| ` *`pad`*` | `xsd:string` | Mappad. |
| ` *`lastModified`*` | `xsd:dateTime` | Datum laatste wijziging. |
| ` *`childLastModified`*` | `xsd:dateTime` | Laatste wijzigingsdatum voor submappen en onderliggende elementen van mappen. |
| ` *`permissionsSetHandle`*` | `xsd:string` | Mapmachtigingen worden afgehandeld. |
| ` *`hasSubfolder`*` | `types:Boolean` | Hiermee wordt bepaald of een map submappen heeft. |
| ` *`subfolderArray`*` | `types:FolderArray` | Een array van submappen in een map. |

