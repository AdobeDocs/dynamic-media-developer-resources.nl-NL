---
description: Configuration attribute for Video360 Viewer.
solution: Experience Manager
title: Video360Player.playback
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: e5a56195-c3ca-4748-aef6-e1f143ac254d
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 3%

---

# Video360Player.playback{#video-player-playback}

Configuration attribute for Video360 Viewer.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressief</span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u het type afspelen in dat door de viewer wordt gebruikt. </p> <p>Wanneer <span class="codeph"> auto</span> is ingesteld, gebruikt de viewer in de meeste desktopbrowsers en alle iOS-apparaten HTML5-streaming video in HLS-indeling en wordt deze teruggezet naar progressieve HTML5-weergave op bepaalde systemen, zoals oudere Internet Explorer en Android. </p> <p>Wanneer <span class="codeph"> progressief</span> wordt geplaatst, baseert de kijker zich slechts op playback van HTML5 zoals oorspronkelijk gesteund door browsers en speelt progressief video op alle systemen. </p> <p>Raadpleeg de gebruikershandleiding bij de HTML5 Viewers SDK voor meer informatie over de afspeelselectie in de native modi <span class="codeph"> auto</span> en <span class="codeph"> progressief</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel. Genegeerd wanneer de viewer werkt met externe video.

Zie [Externe videoondersteuning](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) voor meer informatie.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`auto`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
