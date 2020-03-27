---
description: De kijker steunt het spelen video die buiten het het Publiceren Scene7 Systeem of Dynamische Media wordt ontvangen AEM.
seo-description: De kijker steunt het spelen video die buiten het het Publiceren Scene7 Systeem of Dynamische Media wordt ontvangen AEM.
seo-title: Externe videoondersteuning
solution: Experience Manager
title: Externe videoondersteuning
topic: Dynamic media
uuid: 24739a5a-3a5d-49b8-9a15-bcf3a95fc192
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Externe videoondersteuning{#external-video-support}

De kijker steunt het spelen video die buiten het het Publiceren Scene7 Systeem of Dynamische Media wordt ontvangen AEM.

Ondersteunde indelingen voor de externe video zijn MP4 in H.264-indeling of M3U8-manifest voor de HLS-stream.

De kijker kan of Scene7 of Dynamische video van Media of met externe video werken. Als de kijker met Scene7/de Dynamische video van Media begint, gebruik het met zulk middeltype vooruit lopend, is het niet mogelijk om een externe video in deze kijker te laden gebruikend [`setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) methode. En omgekeerd: als de viewer aanvankelijk met externe video was geladen, moet deze alleen werken met externe video&#39;s.

Wanneer de kijker met externe video werkt negeert de waarde van playbackbepaling en ontdekt het playbacktype van de externe videouitbreiding. Als de externe video-URL eindigt met .m3u8, gebruikt de viewer het afspelen van HLS. Anders wordt progressief afspelen gebruikt.
