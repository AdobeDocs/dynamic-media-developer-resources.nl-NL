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

---


# Bewerkingen: Nieuw en gewijzigd{#operations-new-and-modified}

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

* Toegevoegd `isHidden` en `initialTagValue` aan:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* Toegevoegd `thumbAssetHandle` aan:

   * `createImageSet`
   * `createAssetSet`
   Toegevoegd `companyHandle` aan:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`
   Toegevoegd `contextHandle` aan:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* Toegevoegde includeInactive aan:

   * `getUsers`.
   * `getUserChars`.

* Toegevoegd `permissionArray` aan `createPropertySet`.

* Toegevoegd `exportJob` aan `submitJob`.

**Gewijzigd**

* In `addUser` en `setUser`, gewijzigd `role` in `defaultRole`.

* In `getCompanyMembers`, veranderd `userArray` in `memberArray`.

* In `getCompanyMembership`, veranderd `companyArray` in `membershipArray`.

* In `addUser`, `setCompanyMembership`, en `addCompanyMembership`, veranderd `membershipArray` in `companyHandleArray`.

* In `getCompanyMembership`, veranderd `companyArray` in `membershipArray`.

* In `getUserChars`, `includeInvalid` is nu facultatief.

**Verwijderd**

* Verwijderd `renameFiles` uit `renameAsset`.

* Verwijderd `getXMPPanelViewDefinition`.
* Verwijderd `searchAssetsByFulltext` en `searchAssetsBySimilarity`.

