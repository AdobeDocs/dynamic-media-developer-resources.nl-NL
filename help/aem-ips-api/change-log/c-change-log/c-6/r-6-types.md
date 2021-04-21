---
description: Beschrijft nieuwe en veranderde types voor IPS API versie 6.
solution: Experience Manager
title: Nieuwe en gewijzigde gegevenstypen
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '76'
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

