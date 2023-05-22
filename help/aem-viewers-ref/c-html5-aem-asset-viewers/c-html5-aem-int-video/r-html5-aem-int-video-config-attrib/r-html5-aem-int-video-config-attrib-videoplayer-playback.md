---
title: VideoPlayer.playback
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: fa49e025-1a46-4be7-ad1e-eda3b31bdc8d
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# VideoPlayer.playback{#videoplayer-playback}

Configuration attribute for Interactive Video Viewer.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressief</span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u het type afspelen in dat door de viewer wordt gebruikt. </p> <p>Wanneer <span class="codeph"> auto</span> is ingesteld, gebruikt de viewer in de meeste desktopbrowsers en alle iOS-apparaten HTML5-streaming video in HLS-indeling. En het komt terug bij progressieve HTML5 playback op bepaalde systemen zoals oudere Internet Explorer en Android™. </p> <p>Wanneer <span class="codeph"> progressief</span> is ingesteld, is de viewer alleen afhankelijk van het afspelen van HTML5 als dit wordt ondersteund door browsers en wordt de video progressief afgespeeld op alle systemen. </p> <p>Voor meer informatie over de afspeelselectie in <span class="codeph"> auto</span> en <span class="codeph"> progressief</span> native modi, zie de gebruikershandleiding van de HTML5 Viewers SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`auto`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
