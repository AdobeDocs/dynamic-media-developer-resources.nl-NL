---
title: Video360Player.progressivebitrate
description: Configuration attribute for Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: a253ef01-19ae-4de4-a4fc-b10b28e72c00
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---

# Video360Player.progressivebitrate{#video-player-progressivebitrate}

Configuration attribute for Video360 Viewer.

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Geeft de gewenste videobitsnelheid op (in kilobits per seconde of kbps) voor afspelen vanaf een adaptieve videoset voor het geval dat het huidige systeem adaptieve videoweergave niet ondersteunt. </p> <p>De component neemt de videostream op met de dichtstbijzijnde (maar niet meer dan) bitsnelheid voor de opgegeven waarde. Als alle videostreams in de Adaptive Video Set een hogere kwaliteit hebben dan de opgegeven waarde, kiest de logica de bitsnelheid met de laagste kwaliteit. </p> </td> 
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
