---
description: Beschrijft nieuwe en veranderde gegevenstypes voor IPS API versie 4.5.
solution: Experience Manager
title: Nieuwe en gewijzigde gegevenstypen
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '60'
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

