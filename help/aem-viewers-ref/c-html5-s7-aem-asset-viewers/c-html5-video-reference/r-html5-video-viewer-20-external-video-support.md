---
description: De viewer ondersteunt het afspelen van video die wordt gehost buiten het Scene7 Publishing System of AEM Dynamic Media.
seo-description: De viewer ondersteunt het afspelen van video die wordt gehost buiten het Scene7 Publishing System of AEM Dynamic Media.
seo-title: Externe videoondersteuning
solution: Experience Manager
title: Externe videoondersteuning
topic: Dynamic media
uuid: 24739a5a-3a5d-49b8-9a15-bcf3a95fc192
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---


# Externe videoondersteuning{#external-video-support}

De viewer ondersteunt het afspelen van video die wordt gehost buiten het Scene7 Publishing System of AEM Dynamic Media.

Ondersteunde indelingen voor de externe video zijn MP4 in H.264-indeling of M3U8-manifest voor de HLS-stream.

De viewer kan werken met Scene7- of Dynamic Media-video of met externe video. Als de viewer begint met Scene7/Dynamic Media-video, kunt u deze gebruiken terwijl het type element voorwaarts gaat. Het is dan niet mogelijk om een externe video in deze viewer te laden met de methode [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c). En omgekeerd: als de viewer aanvankelijk met externe video was geladen, moet deze alleen werken met externe video&#39;s.

Wanneer de kijker met externe video werkt negeert de waarde van playbackbepaling en ontdekt het playbacktype van de externe videouitbreiding. Als de externe video-URL eindigt met .m3u8, gebruikt de viewer het afspelen van HLS. Anders wordt progressief afspelen gebruikt.
