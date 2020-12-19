---
description: Configuration attribute for Video360 Viewer.
seo-description: Configuration attribute for Video360 Viewer.
seo-title: Video360Player.initialbitrate
solution: Experience Manager
title: Video360Player.initialbitrate
topic: Dynamic media
uuid: a23fa941-6dd2-41c0-aca9-06f0cdb027b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 5%

---


# Video360Player.initialbitrate{#video-player-initialbitrate}

Configuration attribute for Video360 Viewer.

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u de videobitsnelheid (in kBit per seconde of kbps) in die wordt gebruikt voor de eerste weergave van video op een bureaublad. </p> <p>Als deze bitsnelheidwaarde niet bestaat in de adaptieve videoret, begint de videospeler met de video die de volgende lagere bitsnelheid heeft. </p> <p>Wanneer ingesteld op <span class="codeph"> 0</span>, start de videospeler bij de laagst mogelijke bitsnelheid. </p> <p>Alleen van toepassing op systemen zonder native ondersteuning voor HTML5 HLS-video (zoals Firefox-, Chrome- en Internet Explorer 11-browsers in Windows 10) en wanneer de afspeelmodus is ingesteld op auto. </p> </td> 
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

