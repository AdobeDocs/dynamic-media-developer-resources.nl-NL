---
description: Beschrijft nieuwe en veranderde verrichtingsmethodes voor IPS API versie 4.5.
solution: Experience Manager
title: Nieuwe en gewijzigde bewerkingen
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---


# Bewerkingen: Nieuw en Gewijzigd{#operations-new-and-modified}

Beschrijft nieuwe en veranderde verrichtingsmethodes voor IPS API versie 4.5.

Syntaxis

## Nieuwe bewerkingen {#section-a3be679d8e9345aba2e97699c3a537b9}

* `addMediaPortalEvent`
* `addTagFieldValues`
* `cdnCacheInvalidation`
* `deleteTagFieldValues`
* `deleteTagFieldValues`
* `getDistinctMetadataValues`
* `getMediaPortalEvent`
* `getTagFieldValues`
* `getXMPPacket`
* `searchAssetsByFullText`
* `searchAssetsByMetadata`
* `setTagFieldValues`
* `updateTagFieldValues`
* `updateXMPPacket`

## Gewijzigde bewerkingen {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` bevat  `animatedGifInfo`,  `swcInfo`,  `cssInfo`en  `javascriptInfo` parameters.

* `createMetadataField` bevat een optionele  `isHidden` parameter.

* `saveMetadataField` bevat een optionele  `isHidden` parameter.

* `searchAssets`
* 
* De parameter `renameFiles` is vervangen voor eerdere versies en is verwijderd uit de bewerking `renameAsset`. Het pad van het virtuele bestand wordt gewijzigd en aangepast aan de naam van het nieuwe element (met behoud van de bestandsextensie), maar dit heeft geen invloed op de fysieke bestandspaden. API-clients moeten verwijzingen naar deze parameter verwijderen bij het bijwerken naar de nieuwe API-versie.

