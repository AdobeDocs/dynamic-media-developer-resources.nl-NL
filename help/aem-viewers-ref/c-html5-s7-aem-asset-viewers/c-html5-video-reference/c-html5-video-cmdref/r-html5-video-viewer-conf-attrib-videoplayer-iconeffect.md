---
description: Configuration attribute for Video Viewer.
seo-description: Configuration attribute for Video Viewer.
seo-title: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
topic: Dynamic media
uuid: 1ba6f24a-77bb-41ef-a831-a7ac817abd73
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 1%

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Configuration attribute for Video Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Schakelt het IconEffect in om boven op de video weer te geven wanneer de video wordt gepauzeerd. Op sommige apparaten worden native besturingselementen gebruikt. In dat geval wordt de modifier <span class="codeph"> iconeffect</span> genegeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> aantal</span> </span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u het maximale aantal keren op dat het IconEffect wordt weergegeven en opnieuw wordt weergegeven. De waarde <span class="codeph"> -1</span> geeft aan dat het pictogram oneindig opnieuw wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> vervagen</span> </span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de duur van de animatie in seconden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> Stelt het aantal seconden in dat het IconEffect zichtbaar blijft voordat het automatisch wordt verborgen. De tijd nadat de animatie voor infaden is voltooid en voordat de animatie voor uitfaden wordt gestart. Met de instelling <span class="codeph"> 0</span> wordt het gedrag voor automatisch verbergen uitgeschakeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```

