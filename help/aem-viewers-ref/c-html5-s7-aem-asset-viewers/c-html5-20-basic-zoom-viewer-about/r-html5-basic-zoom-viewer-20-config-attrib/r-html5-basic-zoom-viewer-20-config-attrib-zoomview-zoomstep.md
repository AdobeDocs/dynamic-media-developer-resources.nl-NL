---
description: ZoomView.zoomstep
solution: Experience Manager
title: ZoomView.zoomstep
feature: Dynamic Media Classic,Viewers,SDK/API,Zoomen
role: Developer,User
exl-id: ded8168e-08f7-4bc0-bb8a-624bac82759e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 1%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> stap</span> </span> </p> </td> 
   <td colname="col2"> <p> Vormt het aantal acties voor inzoomen en uitzoomen die nodig zijn om de resolutie met een factor twee te verhogen of te verlagen. De resolutie voor elke zoomactie wordt 2^1 per stap gewijzigd. Stel in op <span class="codeph"> 0</span> om te zoomen naar volledige resolutie met één zoomactie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> limiet</span> </span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u de maximale zoomresolutie in ten opzichte van de afbeelding met volledige resolutie. De standaardwaarde is <span class="codeph"> 1.0</span>, die het zoomen voorbij volledige resolutie niet toestaat. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-50bcd15223174bb79ce08b31ea03d682}

Optioneel.

## Standaard {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1`

## Voorbeeld {#section-96e69b70365f461dae4399e49044ea2f}

`zoomstep=2,3`
