---
description: Beschrijft nieuwe en veranderde types voor IPS API versie 6.
solution: Experience Manager
title: Nieuwe en gewijzigde gegevenstypen
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 0%

---


# Gegevenstypen: Nieuw en Gewijzigd{#data-types-new-and-modified}

Beschrijft nieuwe en veranderde types voor IPS API versie 6.

Syntaxis

## Nieuwe typen {#section-71ba6954339e4ba899acdf8a3212d6f3}

* `AssetContextStateUpdate`
* `AssetContextStateUpdateArray`
* `AssetPublishContexts`
* `AssetPublishContextsArray`
* `CompanyMember`
* `CompanyMemberArray`
* `CompanyMembershipUpdate`
* `CompanyMembershipUpdateArray`
* `ContextStateUpdate`
* `ContextStateUpdateArray`
* `Export Job`
* `PermissionsSet`
* `PermissionsSetArray`
* `PublishContext`
* `PublishContextArray`

## Gewijzigde typen {#section-56b834b1a3b843279d8715b4a4f3890b}

**Toegevoegd**

* `numUrls` toegevoegd aan `UploadUrlsJob`.

* `fileName` toegevoegd aan `Asset.`

* `isHidden` toegevoegd aan `MetadataField`.

* `taskState` toegevoegd aan `TaskProgress`.

* `exportJob` toegevoegd aan `ActiveJob` en `ScheduledJob`.

* `optmizedPath` en `optimizedFile` toegevoegd aan `PsdInfo`.

* `contextHandle` toegevoegd aan:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* De volgende parameters zijn toegevoegd aan `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Gewijzigd**

* In `User` is `role` gewijzigd in `defaultRole`.

* In `Folder` is `permissions` gewijzigd in `permissionsSetHandle`.

* In `AssetSummary` zijn `type` en `name` nu optioneel.

