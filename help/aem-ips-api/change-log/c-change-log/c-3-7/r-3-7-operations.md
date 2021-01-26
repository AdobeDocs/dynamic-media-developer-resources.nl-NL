---
description: Beschrijft nieuwe en veranderde verrichtingsmethodes voor IPS API versie 3.7.
solution: Experience Manager
title: Nieuwe en gewijzigde bewerkingen
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 0%

---


# Bewerkingen: Nieuw en Gewijzigd{#operations-new-and-modified}

Beschrijft nieuwe en veranderde verrichtingsmethodes voor IPS API versie 3.7.

Syntaxis

## Nieuwe bewerkingen {#section-c4d34a58f8194d548fbe26ab3764ea58}

* `moveAsset`
* `renameAsset`
* `deleteAsset`
* `createFolder`
* `deleteFolder`
* `getActiveJobs`
* `getScheduledJobs`
* `getJobLogs`
* `getJbLogDetails`
* `submitJob`
* `stopJob`
* `pauseJob`
* `resumeJob`
* `executeJob`
* `deleteJob`

## Gewijzigde bewerkingen {#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* `name` parameter verwijderd.
* Toegevoegd `excludeFieldArray`.

**getFolders**

* Toegevoegd `excludeFieldArray`.

**getFolderTree**

* Toegevoegd `excludeFieldArray` en `getUniqueMetadataValues`.
* `fieldHandle` is een vereiste parameter.

