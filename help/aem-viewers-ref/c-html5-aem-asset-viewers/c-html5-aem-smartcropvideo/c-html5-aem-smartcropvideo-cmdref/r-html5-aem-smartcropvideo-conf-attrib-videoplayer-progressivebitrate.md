---
description: Configuration attribute for Smart Crop Video Viewer.
solution: Experience Manager
title: SmartCropVideoPlayer.progressivebitrate
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 7f9f1bfe-c68f-4ad4-a4a3-e0a8952e07af
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 1%

---

# SmartCropVideoPlayer.progressivebitrate{#smartcropvideoplayer-progressivebitrate}

Configuration attribute for Smart Crop Video Viewer.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Geeft (in kBit per seconde of kbps) de gewenste videobitsnelheid op voor afspelen vanuit een adaptieve videoset als het huidige systeem geen ondersteuning biedt voor adaptieve videoweergave. </p> <p>De component pakt de videostream op met de dichtstbijzijnde (maar niet meer dan) bitsnelheid voor de opgegeven waarde. Als alle videostreams in de Adaptive Video Set een hogere kwaliteit hebben dan de opgegeven waarde, kiest de logica de bitsnelheid met de laagste kwaliteit. </p> </td> 
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
