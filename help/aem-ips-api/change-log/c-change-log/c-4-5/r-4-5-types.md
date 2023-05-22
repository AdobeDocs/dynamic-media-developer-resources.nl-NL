---
description: Beschrijft nieuwe en veranderde gegevenstypes voor IPS API versie 4.5.
solution: Experience Manager
title: Nieuwe en gewijzigde gegevenstypen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 45024d75-8058-40f8-b3e3-9b28b4cdc3f7
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

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

* Element bevat een nieuw element `fileName` veld dat de naam van het virtuele bestand retourneert.
* `AssetSummary` retourneert een `type` en `name` field

* `MetadataField` include `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` vereist een `urlArray` en voegt een optionele `numUrls` aantal
