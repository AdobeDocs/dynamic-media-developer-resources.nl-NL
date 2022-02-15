---
title: Externe videoondersteuning
description: De viewer ondersteunt het afspelen van video die buiten Dynamic Media Classic of Adobe Experience Manager - Dynamic Media wordt gehost.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Externe videoondersteuning{#external-video-support}

De viewer ondersteunt het afspelen van video die buiten Dynamic Media Classic of Adobe Experience Manager - Dynamic Media wordt gehost.

Ondersteunde indelingen voor de externe video zijn MP4 in H.264-indeling of M3U8-manifest voor de HLS-stream.

De viewer kan werken met Dynamic Media Classic of Experience Manager - Dynamic Media-video of met externe video. Als de viewer begint met Dynamic Media Classic/Dynamic Media-video, kunt u deze gebruiken terwijl het type element voorwaarts gaat. Het is niet mogelijk om een externe video in deze viewer te laden met [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) methode. En omgekeerd: als de viewer aanvankelijk met externe video was geladen, moet deze alleen werken met externe video&#39;s.

Wanneer de kijker met externe video werkt, negeert de waarde van playbackbepaling en ontdekt het playbacktype van de externe videouitbreiding. Als de externe video-URL eindigt met `.m3u8` De viewer gebruikt het afspelen van HLS, anders wordt progressief afspelen gebruikt.
