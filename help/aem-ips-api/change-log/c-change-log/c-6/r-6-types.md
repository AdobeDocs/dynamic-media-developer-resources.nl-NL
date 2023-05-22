---
description: Beschrijft nieuwe en veranderde types voor IPS API versie 6.
solution: Experience Manager
title: Nieuwe en gewijzigde gegevenstypen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 0%

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

* Toegevoegd `numUrls` tot `UploadUrlsJob`.

* Toegevoegd `fileName` tot `Asset.`

* Toegevoegd `isHidden` tot `MetadataField`.

* Toegevoegd `taskState` tot `TaskProgress`.

* Toegevoegd `exportJob` tot `ActiveJob` en `ScheduledJob`.

* Toegevoegd `optmizedPath` en `optimizedFile` tot `PsdInfo`.

* Toegevoegd `contextHandle` tot:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* De volgende parameters zijn toegevoegd aan `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Gewijzigd**

* In `User`, gewijzigd `role` tot `defaultRole`.

* In `Folder`, gewijzigd `permissions` tot `permissionsSetHandle`.

* In `AssetSummary`, `type` en `name` zijn nu optioneel.
