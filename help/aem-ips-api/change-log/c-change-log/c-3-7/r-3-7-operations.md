---
description: Beschrijft nieuwe en veranderde verrichtingsmethodes voor IPS API versie 3.7.
solution: Experience Manager
title: Nieuwe en gewijzigde bewerkingen
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '55'
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

