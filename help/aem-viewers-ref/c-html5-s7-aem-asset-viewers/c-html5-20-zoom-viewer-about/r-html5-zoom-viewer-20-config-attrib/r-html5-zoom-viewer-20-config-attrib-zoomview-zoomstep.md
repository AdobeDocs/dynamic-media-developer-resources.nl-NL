---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: bcd153f3-7a87-4e8f-825b-fc4a136de1dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *`stap`*[, *`limiet`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> stap</span></span> </p> </td> 
   <td colname="col2"> <p> Vormt het aantal gezoem binnen en gezoem uit acties die worden vereist om de resolutie met factor twee te verhogen of te verminderen. De resolutie voor elke zoomactie wordt 2^1 per stap gewijzigd. Instellen op <span class="codeph"> 0</span> zoomen naar volledige resolutie met één zoomactie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> limiet</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u de maximale zoomresolutie in ten opzichte van de afbeelding met volledige resolutie. De standaardwaarde is <span class="codeph"> 1,0</span>, waardoor u niet verder kunt zoomen dan de volledige resolutie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`1,1`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

`zoomstep=2,3`
