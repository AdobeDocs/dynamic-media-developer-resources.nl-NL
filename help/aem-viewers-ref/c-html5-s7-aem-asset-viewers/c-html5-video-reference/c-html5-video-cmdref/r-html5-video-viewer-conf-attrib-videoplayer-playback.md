---
description: Configuration attribute for Video Viewer.
solution: Experience Manager
title: VideoPlayer.playback
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# VideoPlayer.playback{#videoplayer-playback}

Configuration attribute for Video Viewer.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressief</span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u het type afspelen in dat door de viewer wordt gebruikt. Wanneer <span class="codeph"> auto</span> is ingesteld, gebruikt de viewer op de meeste desktopbrowsers en alle iOS-apparaten HTML5-streaming video in HLS-indeling. De functie wordt teruggezet naar progressieve HTML5-weergave op bepaalde systemen, zoals oudere Internet Explorer en Android. </p> <p>Als <span class="codeph"> progressief</span> wordt gespecificeerd, baseert de kijker zich slechts op playback van HTML5 zoals oorspronkelijk gesteund door browsers en speelt progressief video op alle systemen. </p> <p>Raadpleeg de gebruikershandleiding van de SDK van de viewer voor meer informatie over de afspeelselectie in de modi voor automatisch en progressief afspelen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

Genegeerd wanneer de viewer werkt met externe video. Zie [Externe videoondersteuning](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
