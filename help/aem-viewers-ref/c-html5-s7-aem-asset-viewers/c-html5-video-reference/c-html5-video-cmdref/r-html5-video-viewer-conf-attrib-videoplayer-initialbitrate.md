---
title: VideoPlayer.initialbitrate
description: Configuration attribute for Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 83f2af31-e2dc-430c-b9ae-563cdcd20954
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Configuration attribute for Video Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value </span> </p> </td> 
   <td colname="col2"> <p>Hiermee stelt u de videobitsnelheid (in kilobits per seconde of kbps) in die wordt gebruikt voor de eerste weergave van video op desktops. </p> <p>Als deze bitsnelheidwaarde niet bestaat in de adaptieve videoset, start de videospeler de video met de eerstvolgende laagste bitsnelheid. </p> <p>Indien ingesteld op <span class="codeph"> 0 </span>begint de videospeler met de laagst mogelijke bitsnelheid. Alleen van toepassing op systemen die geen native ondersteuning bieden voor HTML5 HLS-video (Firefox-, Chrome- en Internet Explorer 11-browsers in Windows 10) en wanneer de afspeelmodus is ingesteld op <span class="codeph"> auto </span>. </p> </td> 
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
