---
description: SpinView.zoomstep
solution: Experience Manager
title: SpinView.zoomstep
feature: Dynamic Media Classic,Viewers,SDK/API,Draaiensets
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 1%

---


# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> stap</span></span> </p> </td> 
   <td colname="col2"> <p> Vormt het aantal gezoem binnen en gezoem uit acties die worden vereist om de resolutie met factor twee te verhogen of te verminderen. De resolutie voor elke zoomactie wordt 2^1 per stap gewijzigd. Stel in op <span class="codeph"> 0</span> om te zoomen naar volledige resolutie met één zoomactie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> limiet</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u de maximale zoomresolutie in ten opzichte van de afbeelding met volledige resolutie. De standaardwaarde is <span class="codeph"> 1.0</span>, die het zoomen voorbij volledige resolutie niet toestaat. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-924163cb2f6542499f49894becef7fb5}

Optioneel.

## Standaard {#section-7a2128fd488941948aff18421f533ccf}

`1,1`

## Voorbeeld {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`zoomstep=2,3`
