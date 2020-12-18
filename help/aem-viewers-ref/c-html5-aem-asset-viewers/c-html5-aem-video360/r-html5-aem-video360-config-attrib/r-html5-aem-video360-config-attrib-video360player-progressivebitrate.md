---
description: Configuration attribute for Video360 Viewer.
seo-description: Configuration attribute for Video360 Viewer.
seo-title: Video360Player.progressivebitrate
solution: Experience Manager
title: Video360Player.progressivebitrate
topic: Dynamic media
uuid: 438c18d7-e7ac-4834-8445-def590264448
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 6%

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

