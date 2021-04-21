---
description: Beschrijft nieuwe en veranderde gegevenstypes voor IPS API versie 4.5.
solution: Experience Manager
title: Nieuwe en gewijzigde gegevenstypen
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---


# Gegevenstypen: Nieuw en Gewijzigd{#data-types-new-and-modified}

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

* Element bevat een nieuw veld `fileName` dat de naam van het virtuele bestand retourneert.
* `AssetSummary` retourneert een  `type` en  `name` veld

* `MetadataField` include  `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` vereist een  `urlArray` en voegt een optioneel  `numUrls` aantal toe

