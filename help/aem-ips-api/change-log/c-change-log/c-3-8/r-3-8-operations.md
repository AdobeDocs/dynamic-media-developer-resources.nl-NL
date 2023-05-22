---
description: Beschrijft nieuwe en veranderde verrichtingsmethodes voor IPS API versie 3.8.
solution: Experience Manager
title: Nieuwe en gewijzigde bewerkingen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# Bewerkingen: Nieuw en gewijzigd{#operations-new-and-modified}

Beschrijft nieuwe en veranderde verrichtingsmethodes voor IPS API versie 3.8.

Syntaxis

## Nieuwe bewerkingen {#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState`
* `saveZoomTarget`
* `deleteZoomTarget`
* `saveImageMap`
* `deleteImageMap`
* `createImageSet`
* `getImageSetMembers`

## Gewijzigde bewerkingen {#section-25eee732b69c49d0a27b1f3290f8654a}

**searchAssets**

* De optionele `publishState` parameter laat u op `MarkedForPublish/NotMarkedForPublish` toestand van het element.

**getJobLogs**

* De optionele `userHandle` Met deze parameter kunt u taaklogboeken ophalen die door een specifieke gebruiker zijn ingediend.
