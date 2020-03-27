---
description: Deze nieuwe of gewijzigde verrichtingen en gegevenstypes beschikbaar in bèta WSDL moeten niet buiten Scene7 ontwikkelde toepassingen worden gebruikt.
seo-description: Deze nieuwe of gewijzigde verrichtingen en gegevenstypes beschikbaar in bèta WSDL moeten niet buiten Scene7 ontwikkelde toepassingen worden gebruikt.
seo-title: Beperkt gebruik
solution: Experience Manager
title: Beperkt gebruik
topic: Scene7 Image Production System API
uuid: 76a423e5-ff7d-44a3-aba4-af258ea55256
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Beperkt gebruik{#restricted-use}

Deze nieuwe of gewijzigde verrichtingen en gegevenstypes beschikbaar in bèta WSDL moeten niet buiten Scene7 ontwikkelde toepassingen worden gebruikt.

Deze bewerkingen en typen zijn onderhevig aan uitschakelen, wijzigen of vervangen met volgende systeemupdates.

**Nieuwe typen**

* AssetPublishContext
* AssetPublishContextArray
* CompanyMetadataInfo
* CompanyMetadataInfoArray
* CreateVideoSitemapJob
* PublishContext
* PublishContextArray
* SearchFilter
* LongArray

**Nieuwe bewerkingen**

* applyMetadataTemplate
* batchGetAssetPublishContext
* createCompanyMetadata
* deleteCompanyMetadata
* getCompanyMetadata
* getPublishContext
* listCompanyMetadata
* removeMask
* removePropertySetPermissions
* searchAssetsBysimilar
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAssetSet
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**Gewijzigde typen**

* Gewijzigd `ActiveJob` om een `createVideoSitemapJob` type op te nemen

* Gewijzigd `ScheduledJob` om een `createVideoSitemapJob` type op te nemen

* Gewijzigd `ImageServingPublishJob` om een optioneel object op te nemen `contextHandle`

* Gewijzigd `ImageRenderingPublishJob` om een optioneel object op te nemen `contextHandle`

* Gewijzigd `MetadataField` om een optioneel object op te nemen `initialTagField`

* Gewijzigd `MetadataCondition` in include en optionele `caseSensitive` parameter

* Gewijzigd `PropertySet` om een optioneel object op te nemen `PermissionArray` zoals `permissions`

* Gewijzigd `UploadDirectoryJob` om optionele `xmpKeywords`, `xmpTemplateId` en `xmpTemplateOverride` parameters op te nemen

* Gewijzigd `VideoPublishJob` om een optioneel object op te nemen `contextHandle`

**Gewijzigde bewerkingen**

* Gewijzigd `createAssetSet` om een optioneel object op te nemen `thumbAssetHandle`

* Gewijzigd `createImageSet` om een optioneel object op te nemen `thumbAssetHandle`

* Gewijzigd `createMetadataField` om een optionele `initialTagValue` parameter op te nemen

* Gewijzigd `createPropertySet` om een optioneel object op te nemen `PermissionUpdateArray` zoals `permissionArray`

* Gewijzigd `getImageServingPublishSettings` om een optionele `contextHandle` parameter op te nemen

* Gewijzigd `getImageRenderingPublishSettings` om een optionele `contextHandle` parameter op te nemen

* Gewijzigd `searchAssetsByFullText` om een reeks optionele parameters op te nemen:

   * `SearchFilter` as, `filters` parameter

   * `sortBy`
   * `sortDirection`

* Gewijzigd `searchAssetsByMetadata` om een reeks optionele parameters op te nemen:

   * `SearchFilter` as, `filters` parameter

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` reeks van zeven parameters

* Gewijzigd `setAssetPublishState` om een optioneel object op te nemen `HandleArray` zoals `contextHandleArray`

* Gewijzigd `setImageServingPublishSettings` om een optionele `contextHandle` parameter op te nemen

* Gewijzigd `setImageRenderingPublishSettings` om een optionele `contextHandle`parameter op te nemen

* Gewijzigd `submitJob` om een optioneel `createVideoSitemap` taaktype op te nemen

