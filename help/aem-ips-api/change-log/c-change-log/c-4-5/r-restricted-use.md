---
description: Deze nieuwe of gewijzigde bewerkingen en gegevenstypen die beschikbaar zijn in de bètaversie van WSDL, mogen niet worden gebruikt buiten Dynamic Media-toepassingen.
solution: Experience Manager
title: Beperkt gebruik
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Beperkt gebruik{#restricted-use}

Deze nieuwe of gewijzigde bewerkingen en gegevenstypen die beschikbaar zijn in de bètaversie van WSDL, mogen niet worden gebruikt buiten Dynamic Media-toepassingen.

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

* Gewijzigd `ActiveJob` een `createVideoSitemapJob` type

* Gewijzigd `ScheduledJob` een `createVideoSitemapJob` type

* Gewijzigd `ImageServingPublishJob` om een facultatieve `contextHandle`

* Gewijzigd `ImageRenderingPublishJob` om een facultatieve `contextHandle`

* Gewijzigd `MetadataField` om een facultatieve `initialTagField`

* Gewijzigd `MetadataCondition` om op te nemen en facultatief `caseSensitive` parameter

* Gewijzigd `PropertySet` om een facultatieve `PermissionArray` als `permissions`

* Gewijzigd `UploadDirectoryJob` Optioneel opnemen `xmpKeywords`, `xmpTemplateId` en `xmpTemplateOverride` parameters

* Gewijzigd `VideoPublishJob` om een facultatieve `contextHandle`

**Gewijzigde bewerkingen**

* Gewijzigd `createAssetSet` om een facultatieve `thumbAssetHandle`

* Gewijzigd `createImageSet` om een facultatieve `thumbAssetHandle`

* Gewijzigd `createMetadataField` om een facultatieve `initialTagValue` parameter

* Gewijzigd `createPropertySet` om een facultatieve `PermissionUpdateArray` als `permissionArray`

* Gewijzigd `getImageServingPublishSettings` om een facultatieve `contextHandle` parameter

* Gewijzigd `getImageRenderingPublishSettings` om een facultatieve `contextHandle` parameter

* Gewijzigd `searchAssetsByFullText` een reeks facultatieve parameters op te nemen:

   * `SearchFilter` als `filters` parameter

   * `sortBy`
   * `sortDirection`

* Gewijzigd `searchAssetsByMetadata` een reeks facultatieve parameters op te nemen:

   * `SearchFilter` als `filters` parameter

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` reeks van zeven parameters

* Gewijzigd `setAssetPublishState` om een facultatieve `HandleArray` als `contextHandleArray`

* Gewijzigd `setImageServingPublishSettings` om een facultatieve `contextHandle` parameter

* Gewijzigd `setImageRenderingPublishSettings` om een facultatieve `contextHandle`parameter

* Gewijzigd `submitJob` om een facultatieve `createVideoSitemap` taaktype
