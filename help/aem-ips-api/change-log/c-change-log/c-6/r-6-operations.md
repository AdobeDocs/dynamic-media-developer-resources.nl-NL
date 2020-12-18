---
description: Beschrijft nieuwe en veranderde verrichtingsmethodes voor IPS API versie 6.
seo-description: Beschrijft nieuwe en veranderde verrichtingsmethodes voor IPS API versie 6.
seo-title: Nieuwe en gewijzigde bewerkingen
solution: Experience Manager
title: Nieuwe en gewijzigde bewerkingen
topic: Scene7 Image Production System API
uuid: e36f0d5c-0170-4a65-9347-c7fd3538726b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---


# Bewerkingen: Nieuw en Gewijzigd{#operations-new-and-modified}

Beschrijft nieuwe en veranderde verrichtingsmethodes voor IPS API versie 6.

Syntaxis

## Nieuwe bewerkingen {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## Gewijzigde bewerkingen {#section-f4e8755527444266ae806e3f4c851ae6}

**Toegevoegd**

* `isHidden` en `initialTagValue` toegevoegd aan:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* `thumbAssetHandle` toegevoegd aan:

   * `createImageSet`
   * `createAssetSet`

   `companyHandle` toegevoegd aan:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   `contextHandle` toegevoegd aan:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* Toegevoegde includeInactive aan:

   * `getUsers`.
   * `getUserChars`.

* `permissionArray` toegevoegd aan `createPropertySet`.

* `exportJob` toegevoegd aan `submitJob`.

**Gewijzigd**

* In `addUser` en `setUser` is `role` gewijzigd in `defaultRole`.

* In `getCompanyMembers` is `userArray` gewijzigd in `memberArray`.

* In `getCompanyMembership` is `companyArray` gewijzigd in `membershipArray`.

* In `addUser`, `setCompanyMembership`, en `addCompanyMembership`, veranderde `membershipArray` in `companyHandleArray`.

* In `getCompanyMembership` is `companyArray` gewijzigd in `membershipArray`.

* In `getUserChars` is `includeInvalid` nu optioneel.

**Verwijderd**

* `renameFiles` verwijderd uit `renameAsset`.

* `getXMPPanelViewDefinition` verwijderd.
* `searchAssetsByFulltext` en `searchAssetsBySimilarity` zijn verwijderd.

