---
title: VideoPlayer.initialbitrate
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 75ee2c74-21c4-41b6-9d0f-15aa8432f177
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Configuration attribute for Interactive Video Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u de videobitsnelheid (in kilobits per seconde of kbps) in die wordt gebruikt voor de eerste weergave van video op een bureaublad. </p> <p>Als deze bitsnelheidwaarde niet bestaat in de adaptieve videoret, begint de videospeler met de video die de volgende lagere bitsnelheid heeft. </p> <p>Wanneer ingesteld op <span class="codeph"> 0</span>, start de videospeler bij de laagst mogelijke bitsnelheid. </p> <p>Alleen van toepassing op systemen zonder native ondersteuning voor HTML5 HLS-video (zoals Firefox-, Chrome- en Internet Explorer 11-browsers in Windows 10) en wanneer de afspeelmodus is ingesteld op auto. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```
