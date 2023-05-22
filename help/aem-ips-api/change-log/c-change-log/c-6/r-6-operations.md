---
description: Beschrijft nieuwe en veranderde verrichtingsmethodes voor IPS API versie 6.
solution: Experience Manager
title: Nieuwe en gewijzigde bewerkingen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

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

* Toegevoegd `isHidden` en `initialTagValue` tot:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* Toegevoegd `thumbAssetHandle` tot:

   * `createImageSet`
   * `createAssetSet`

   Toegevoegd `companyHandle` tot:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   Toegevoegd `contextHandle` tot:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* Toegevoegde includeInactive aan:

   * `getUsers`.
   * `getUserChars`.

* Toegevoegd `permissionArray` tot `createPropertySet`.

* Toegevoegd `exportJob` tot `submitJob`.

**Gewijzigd**

* In `addUser` en `setUser`, gewijzigd `role` tot `defaultRole`.

* In `getCompanyMembers`, gewijzigd `userArray` tot `memberArray`.

* In `getCompanyMembership`, gewijzigd `companyArray` tot `membershipArray`.

* In `addUser`, `setCompanyMembership`, en `addCompanyMembership`, gewijzigd `membershipArray` tot `companyHandleArray`.

* In `getCompanyMembership`, gewijzigd `companyArray` tot `membershipArray`.

* In `getUserChars`, `includeInvalid` is nu optioneel.

**Verwijderd**

* Verwijderd `renameFiles` van `renameAsset`.

* Verwijderd `getXMPPanelViewDefinition`.
* Verwijderd `searchAssetsByFulltext` en `searchAssetsBySimilarity`.
