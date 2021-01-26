---
description: Deze nieuwe of gewijzigde bewerkingen en gegevenstypen die beschikbaar zijn in de bètaversie van WSDL, mogen niet worden gebruikt buiten Dynamic Media-toepassingen.
solution: Experience Manager
title: Beperkt gebruik
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
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

* Gewijzigd `ActiveJob` om een `createVideoSitemapJob` type op te nemen

* Gewijzigd `ScheduledJob` om een `createVideoSitemapJob` type op te nemen

* `ImageServingPublishJob` gewijzigd om een optionele `contextHandle` op te nemen

* `ImageRenderingPublishJob` gewijzigd om een optionele `contextHandle` op te nemen

* `MetadataField` gewijzigd om een optionele `initialTagField` op te nemen

* `MetadataCondition` gewijzigd om de parameter `caseSensitive` op te nemen en op te tioneel te maken

* `PropertySet` gewijzigd om een optionele `PermissionArray` als `permissions` op te nemen

* Gewijzigd `UploadDirectoryJob` om optionele parameters `xmpKeywords`, `xmpTemplateId` en `xmpTemplateOverride` op te nemen

* `VideoPublishJob` gewijzigd om een optionele `contextHandle` op te nemen

**Gewijzigde bewerkingen**

* `createAssetSet` gewijzigd om een optionele `thumbAssetHandle` op te nemen

* `createImageSet` gewijzigd om een optionele `thumbAssetHandle` op te nemen

* `createMetadataField` gewijzigd om een optionele `initialTagValue`-parameter op te nemen

* `createPropertySet` gewijzigd om een optionele `PermissionUpdateArray` als `permissionArray` op te nemen

* `getImageServingPublishSettings` gewijzigd om een optionele `contextHandle`-parameter op te nemen

* `getImageRenderingPublishSettings` gewijzigd om een optionele `contextHandle`-parameter op te nemen

* `searchAssetsByFullText` gewijzigd om een reeks optionele parameters op te nemen:

   * `SearchFilter` as,  `filters` parameter

   * `sortBy`
   * `sortDirection`

* `searchAssetsByMetadata` gewijzigd om een reeks optionele parameters op te nemen:

   * `SearchFilter` as,  `filters` parameter

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` reeks van zeven parameters

* `setAssetPublishState` gewijzigd om een optionele `HandleArray` als `contextHandleArray` op te nemen

* `setImageServingPublishSettings` gewijzigd om een optionele `contextHandle`-parameter op te nemen

* `setImageRenderingPublishSettings` gewijzigd om een optionele `contextHandle`parameter op te nemen

* Gewijzigd `submitJob` om een optioneel `createVideoSitemap` taaktype op te nemen

