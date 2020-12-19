---
description: Beschrijft nieuwe en veranderde types voor IPS API versie 6.
seo-description: Beschrijft nieuwe en veranderde types voor IPS API versie 6.
seo-title: Nieuwe en gewijzigde gegevenstypen
solution: Experience Manager
title: Nieuwe en gewijzigde gegevenstypen
topic: Scene7 Image Production System API
uuid: ef7c43ee-467f-46b9-bd82-05e8359bd829
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '84'
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

