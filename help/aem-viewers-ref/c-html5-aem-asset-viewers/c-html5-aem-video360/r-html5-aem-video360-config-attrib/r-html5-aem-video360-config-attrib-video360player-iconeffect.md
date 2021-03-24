---
description: Configuration attribute for Video360 Viewer.
solution: Experience Manager
title: Video360Player.iconeffect
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR-video
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 4%

---


# Video360Player.iconeffect{#video-player-iconeffect}

Configuration attribute for Video360 Viewer.

` [Video360Player.|<containerId>_video360Player.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Hiermee wordt het IconEffect vóór de video weergegeven wanneer de video is gepauzeerd. Op sommige apparaten worden native besturingselementen gebruikt. In dergelijke gevallen wordt de pictogrameffect<span class="codeph">/&gt;-modifier genegeerd.</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> aantal</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u het maximale aantal keren op dat het IconEffect wordt weergegeven en opnieuw wordt weergegeven. De waarde <span class="codeph"> -1</span> geeft aan dat het pictogram oneindig opnieuw wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> vervagen</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de duur van de animatie in seconden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> Stelt het aantal seconden in dat het IconEffect volledig zichtbaar blijft voordat het automatisch wordt verborgen. De tijd nadat de animatie voor vervagen is voltooid en voordat de animatie voor vervagen wordt gestart. Stel in op <span class="codeph"> 0</span> om automatisch verbergen uit te schakelen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
