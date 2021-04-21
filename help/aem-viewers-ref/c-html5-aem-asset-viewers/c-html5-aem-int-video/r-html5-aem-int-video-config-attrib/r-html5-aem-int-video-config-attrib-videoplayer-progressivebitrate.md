---
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
title: VideoPlayer.progressivebitrate
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 69f3c4c0-00d9-46ef-aebb-3116a0d83c85
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

Configuration attribute for Interactive Video Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Geeft in kBit per seconde (of kbps) de gewenste videobitsnelheid op voor afspelen vanuit een adaptieve videoset als het huidige systeem geen ondersteuning biedt voor adaptief afspelen van video. </p> <p>De component neemt de videostream op met de dichtstbijzijnde (maar niet meer dan) bitsnelheid voor de opgegeven waarde. Als alle videostreams in de Adaptive Video Set een hogere kwaliteit hebben dan de opgegeven waarde, kiest de logica de bitsnelheid met de laagste kwaliteit. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```
