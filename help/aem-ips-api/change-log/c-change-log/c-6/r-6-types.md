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

---


# Gegevenstypen: Nieuw en gewijzigd{#data-types-new-and-modified}

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

* Toegevoegd `numUrls` aan `UploadUrlsJob`.

* Toegevoegd `fileName` aan `Asset.`

* Toegevoegd `isHidden` aan `MetadataField`.

* Toegevoegd `taskState` aan `TaskProgress`.

* Toegevoegd `exportJob` aan `ActiveJob` en `ScheduledJob`.

* Toegevoegd `optmizedPath` en `optimizedFile` aan `PsdInfo`.

* Toegevoegd `contextHandle` aan:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* De volgende parameters zijn toegevoegd aan `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Gewijzigd**

* In `User`, veranderd `role` in `defaultRole`.

* In `Folder`, veranderd `permissions` in `permissionsSetHandle`.

* In `AssetSummary`, `type` en `name` zijn nu facultatief.

