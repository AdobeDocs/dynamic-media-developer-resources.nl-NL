---
description: Beschrijft nieuwe en veranderde verrichtingsmethodes voor IPS API versie 4.5.
seo-description: Beschrijft nieuwe en veranderde verrichtingsmethodes voor IPS API versie 4.5.
seo-title: Nieuwe en gewijzigde bewerkingen
solution: Experience Manager
title: Nieuwe en gewijzigde bewerkingen
topic: Scene7 Image Production System API
uuid: c4002670-c830-474e-bb84-343f76b6fb80
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Bewerkingen: Nieuw en gewijzigd{#operations-new-and-modified}

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

* `Asset` bevat `animatedGifInfo`, `swcInfo`, `cssInfo`en `javascriptInfo` parameters.

* `createMetadataField` bevat een optionele `isHidden` parameter.

* `saveMetadataField` bevat een optionele `isHidden` parameter.

* `searchAssets`
* 
* De `renameFiles` parameter is vervangen voor eerdere versies en is verwijderd uit de `renameAsset` bewerking. Het pad van het virtuele bestand wordt gewijzigd en aangepast aan de naam van het nieuwe element (met behoud van de bestandsextensie), maar dit heeft geen invloed op de fysieke bestandspaden. API-clients moeten verwijzingen naar deze parameter verwijderen bij het bijwerken naar de nieuwe API-versie.

