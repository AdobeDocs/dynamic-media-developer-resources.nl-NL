---
description: De viewer ondersteunt het afspelen van video die wordt gehost buiten SPS- of AEM Dynamic Media.
seo-description: De viewer ondersteunt het afspelen van video die wordt gehost buiten SPS- of AEM Dynamic Media.
seo-title: Externe videoondersteuning
solution: Experience Manager
title: Externe videoondersteuning
topic: Dynamic media
uuid: 2e9f1c54-627f-4462-ae85-8a5ca1d09762
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Externe videoondersteuning{#external-video-support}

De viewer ondersteunt het afspelen van video die wordt gehost buiten SPS- of AEM Dynamic Media.

Ondersteunde indelingen voor de externe video zijn MP4 in H.264-indeling of M3U8-manifest voor de HLS-stream.

De viewer kan zowel met Dynamic Media Classic als met AEM Dynamic Media-video of met externe video werken. Als de viewer begint met Dynamic Media Classic/AEM Dynamic Media-video, moet deze worden gebruikt met dit type elementen. Het is niet mogelijk om een externe video in deze viewer te laden met de [methode setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) en andersom. Dat wil zeggen dat als de viewer aanvankelijk met externe video was geladen, deze alleen met externe video&#39;s blijft werken.

Wanneer de kijker met externe video werkt negeert de waarde van om het even welke playbackbepaling en ontdekt het playbacktype van de externe videouitbreiding. Als de externe video-URL eindigt met `.m3u8`, gebruikt de viewer het afspelen van HLS. anders wordt progressief afspelen gebruikt.
