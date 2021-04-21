---
description: Configuration attribute for Video360 Viewer.
solution: Experience Manager
title: Video360Player.progressivebitrate
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: a253ef01-19ae-4de4-a4fc-b10b28e72c00
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 4%

---

# Video360Player.progressivebitrate{#video-player-progressivebitrate}

Configuration attribute for Video360 Viewer.

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`value`*`

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
