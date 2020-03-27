---
description: Beschrijft nieuwe en veranderde verrichtingsmethodes voor IPS API versie 3.7.
seo-description: Beschrijft nieuwe en veranderde verrichtingsmethodes voor IPS API versie 3.7.
seo-title: Nieuwe en gewijzigde bewerkingen
solution: Experience Manager
title: Nieuwe en gewijzigde bewerkingen
topic: Scene7 Image Production System API
uuid: 3c163157-cd0d-4887-a1f0-7941d96c36f9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Bewerkingen: Nieuw en gewijzigd{#operations-new-and-modified}

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

* Verwijderd `name` parameter.
* Toegevoegd `excludeFieldArray`.

**getFolders**

* Toegevoegd `excludeFieldArray`.

**getFolderTree**

* Toegevoegd `excludeFieldArray` en `getUniqueMetadataValues`.
* Een `fieldHandle` vereiste parameter gemaakt.

