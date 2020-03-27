---
description: 'null'
seo-description: 'null'
seo-title: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
topic: Dynamic media
uuid: 11458300-4a1b-4623-8ea1-db804daab3cf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PageView.zoomstep{#pageview-zoomstep}

` [PageView.|<containerId>_pageView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> stap</span></span> </p> </td> 
   <td colname="col2"> <p> Vormt het aantal acties voor inzoomen en uitzoomen die nodig zijn om de resolutie met een factor twee te verhogen of te verlagen. De resolutie voor elke zoomactie wordt 2^1 per stap gewijzigd. Stel in op <span class="codeph"> 0</span> om met één zoomactie in te zoomen op volledige resolutie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> limiet</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u de maximale zoomresolutie in ten opzichte van de afbeelding met volledige resolutie. De standaardwaarde is <span class="codeph"> 1,0</span>, zodat u alleen kunt inzoomen met volledige resolutie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-636d35a4791447039f1902973f568320}

Optioneel.

## Standaard {#section-ad8a5fe2383e4c228bf177a41b53d921}

`1,1`

## Voorbeeld {#section-1e20672d42c845bd84f02f88cbc53efc}

`zoomstep=2,3`
