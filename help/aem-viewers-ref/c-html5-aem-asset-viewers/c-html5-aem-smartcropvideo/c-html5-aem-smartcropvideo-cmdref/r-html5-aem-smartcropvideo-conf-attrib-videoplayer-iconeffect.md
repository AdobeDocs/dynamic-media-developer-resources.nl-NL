---
title: SmartCropVideoPlayer.iconeffect
description: Configuration attribute for Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 369e389c-f0e2-405e-b4aa-2f6b9ac8b8ea
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---

# SmartCropVideoPlayer.iconeffect{#smartcropvideoplayer-iconeffect}

Configuration attribute for Smart Crop Video Viewer.

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`aantal`*][, *`vervagen`*][, *`autoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Schakelt het IconEffect in om boven op de video weer te geven wanneer de video wordt gepauzeerd. Op sommige apparaten worden native besturingselementen gebruikt. In dat geval <span class="codeph"> iconeffect</span> modifier wordt genegeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> aantal</span> </span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u het maximale aantal keren op dat het IconEffect wordt weergegeven en opnieuw wordt weergegeven. Een waarde van <span class="codeph"> -1</span> Hiermee wordt aangegeven dat het pictogram voor onbepaalde tijd opnieuw wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> vervagen</span> </span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de duur van de animatie in seconden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> Stelt het aantal seconden in dat het IconEffect zichtbaar blijft voordat het automatisch wordt verborgen. De tijd nadat de animatie voor infaden is voltooid en voordat de animatie voor uitfaden wordt gestart. Een instelling van <span class="codeph"> 0</span> Schakelt automatisch verbergen uit. </p> </td> 
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
