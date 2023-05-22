---
title: Video360Player.playback
description: Configuration attribute for Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e5a56195-c3ca-4748-aef6-e1f143ac254d
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# Video360Player.playback{#video-player-playback}

Configuration attribute for Video360 Viewer.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressief</span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u het type afspelen in dat door de viewer wordt gebruikt. </p> <p>Wanneer <span class="codeph"> auto</span> is ingesteld, gebruikt de viewer in de meeste desktopbrowsers en alle iOS-apparaten HTML5-streaming video in HLS-indeling. En het komt terug bij progressieve HTML5 playback op bepaalde systemen zoals oudere Internet Explorer en Android™. </p> <p>Wanneer <span class="codeph"> progressief</span> is ingesteld, is de viewer alleen afhankelijk van het afspelen van HTML5 als dit wordt ondersteund door browsers en wordt de video progressief afgespeeld op alle systemen. </p> <p>Voor meer informatie over de afspeelselectie in <span class="codeph"> auto</span> en <span class="codeph"> progressief</span> native modi, zie de gebruikershandleiding van de HTML5 Viewers SDK. </p> </td> 
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
