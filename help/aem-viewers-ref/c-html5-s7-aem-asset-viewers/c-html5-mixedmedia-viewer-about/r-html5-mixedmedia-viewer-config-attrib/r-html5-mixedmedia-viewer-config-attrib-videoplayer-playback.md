---
title: VideoPlayer.playback
description: Configuration attribute for Mixed Media Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: accf2b56-d7bd-483d-9759-fa38246a0a8f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---

# VideoPlayer.playback{#videoplayer-playback}

Configuration attribute for Mixed Media Video Viewer.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressief</span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u het type afspelen in dat door de viewer wordt gebruikt. Wanneer <span class="codeph"> auto</span> is ingesteld, gebruikt de viewer op de meeste desktopbrowsers en op alle iOS-apparaten HTML5-streaming video in HLS-indeling. De functie wordt teruggezet naar progressieve HTML5-weergave op bepaalde systemen, zoals oudere Internet Explorer en Android™. </p> <p>Indien <span class="codeph"> progressief</span> is opgegeven, is de viewer alleen afhankelijk van het afspelen van HTML5 als dit native wordt ondersteund door browsers en wordt de video progressief afgespeeld op alle systemen. </p> <p>Raadpleeg de gebruikershandleiding van de SDK van de viewer voor meer informatie over de afspeelselectie in de modus Automatisch en progressief. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
