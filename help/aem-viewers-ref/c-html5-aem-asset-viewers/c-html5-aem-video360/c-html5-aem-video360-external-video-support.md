---
description: De viewer ondersteunt het afspelen van video die buiten Dynamic Media Classic of AEM Dynamic Media wordt gehost.
solution: Experience Manager
title: Externe videoondersteuning
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR-video
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# Externe videoondersteuning{#external-video-support}

De viewer ondersteunt het afspelen van video die buiten Dynamic Media Classic of AEM Dynamic Media wordt gehost.

Ondersteunde indelingen voor de externe video zijn MP4 in H.264-indeling of M3U8-manifest voor de HLS-stream.

De viewer kan werken met Dynamic Media Classic of AEM Dynamic Media-video of met externe video. Als de viewer begint met Dynamic Media Classic/AEM Dynamic Media-video, moet deze worden gebruikt met het volgende type element. Het is niet mogelijk om een externe video in deze viewer te laden met de methode [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) en omgekeerd. Dat wil zeggen dat als de viewer aanvankelijk met externe video was geladen, deze alleen met externe video&#39;s blijft werken.

Wanneer de kijker met externe video werkt negeert de waarde van om het even welke playbackbepaling en ontdekt het playbacktype van de externe videouitbreiding. Als de externe video-URL eindigt met `.m3u8`, gebruikt de viewer het afspelen van HLS. anders wordt progressief afspelen gebruikt.
