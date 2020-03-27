---
description: Beschrijft nieuwe en veranderde gegevenstypes voor IPS API versie 4.5.
seo-description: Beschrijft nieuwe en veranderde gegevenstypes voor IPS API versie 4.5.
seo-title: Nieuwe en gewijzigde gegevenstypen
solution: Experience Manager
title: Nieuwe en gewijzigde gegevenstypen
topic: Scene7 Image Production System API
uuid: 2752f9dd-ec47-45d6-a465-6d275ec2b2fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Gegevenstypen: Nieuw en gewijzigd{#data-types-new-and-modified}

Beschrijft nieuwe en veranderde gegevenstypes voor IPS API versie 4.5.

Syntaxis

## Nieuwe typen {#section-6941b228cf6747a987e98c3d6e4b6b17}

* `AssetSummary`
* `AssetSummaryArray`
* `JobLogDetailAux`
* `JobLogDetailAuxArray`
* `MPEvent`
* `MPEventArray`
* `OperationFault`
* `OperationFaultArray`
* `PhotoshopOptions`
* `TagCondition`
* `TagConditionArray`
* `TagFieldValues`
* `TagFieldValuesArray`
* `TagValueUpdate`
* `TagValueUpdateArray`
* `TagValueUpdateFault`
* `TagValueUpdateFaultArray`
* `UrlArray`

## Gewijzigde typen {#section-6ecdf752cc1a4636a583b4c546a0fccf}

* Element bevat een nieuw `fileName` veld dat de virtuele bestandsnaam retourneert.
* `AssetSummary` retourneert een `type` en `name` veld

* `MetadataField` include `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` vereist een `urlArray` en voegt een optioneel `numUrls` aantal toe

