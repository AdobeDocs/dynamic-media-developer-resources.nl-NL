---
description: Configuration attribute for Smart Crop Video Viewer.
solution: Experience Manager
title: SmartCropVideoPlayer.playback
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

Configuration attribute for Smart Crop Video Viewer.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressief</span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u het type afspelen in dat door de viewer wordt gebruikt. Wanneer <span class="codeph"> auto</span> is ingesteld, gebruikt de viewer op de meeste desktopbrowsers en op alle iOS-apparaten HTML5-streaming video in HLS-indeling. Het komt terug bij progressieve HTML5 playback op bepaalde systemen zoals ouder Internet Explorer en Android. </p> <p>Indien <span class="codeph"> progressief</span> is opgegeven, is de viewer alleen afhankelijk van het afspelen van HTML5 als dit native wordt ondersteund door browsers en wordt de video progressief afgespeeld op alle systemen. </p> <p>Raadpleeg de gebruikershandleiding van de SDK van de viewer voor meer informatie over de afspeelselectie in de modi voor automatisch en progressief afspelen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

Genegeerd wanneer de viewer werkt met externe video. Zie [Externe videoondersteuning]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
