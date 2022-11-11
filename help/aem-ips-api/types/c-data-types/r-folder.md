---
description: Hierarchische bestands- of elementopslagobjecten. Mappen kunnen een (of meer) submappen bevatten.
solution: Experience Manager
title: Map
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# [!DNL Folder]{#folder}

Hierarchische bestands- of elementopslagobjecten. Mappen kunnen een (of meer) submappen bevatten.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| folderHandle | `xsd:string` | Mapgreep. |
| [!DNL path] | `xsd:string` | Mappad. |
| lastModified | `xsd:dateTime` | Datum laatste wijziging. |
| childLastModified | `xsd:dateTime` | Laatste wijzigingsdatum voor submappen en onderliggende elementen van mappen. |
| permissionsSetHandle | `xsd:string` | Mapmachtigingen worden afgehandeld. |
| hasSubfolder | `types:Boolean` | Hiermee wordt bepaald of een map submappen heeft. |
| subfolderArray | `types:FolderArray` | Een array van submappen in een map. |
