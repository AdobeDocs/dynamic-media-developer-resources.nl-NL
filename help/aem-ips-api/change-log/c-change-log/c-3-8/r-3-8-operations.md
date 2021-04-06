---
description: Beschrijft nieuwe en veranderde verrichtingsmethodes voor IPS API versie 3.8.
solution: Experience Manager
title: Nieuwe en gewijzigde bewerkingen
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---

# Bewerkingen: Nieuw en Gewijzigd{#operations-new-and-modified}

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

* Met de optionele parameter `publishState` kunt u zoeken naar de elementstatus `MarkedForPublish/NotMarkedForPublish`.

**getJobLogs**

* Met de optionele parameter `userHandle` kunt u taaklogboeken ophalen die door een specifieke gebruiker zijn ingediend.
