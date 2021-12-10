---
title: ZoomView.frametransition
description: ZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 1%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`duur`*[, *`afstand`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|faden|dia </span> </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u het type effect op dat wordt toegepast op de framewijziging. Het kenmerk <span class="codeph"> none </span> staat voor geen overgang; de framewijziging gebeurt onmiddellijk. Het kenmerk <span class="codeph"> vervagen </span> betekent overgang tussen oude en nieuwe frames met vervagingen. Het kenmerk <span class="codeph"> dia </span> Hiermee activeert u een overgang waarin het oude frame uit de weergave schuift en waarin het nieuwe frame schuift. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duur </span> </span> </p> </td> 
   <td colname="col2"> <p>Geeft de duur aan (in seconden) van <span class="codeph"> vervagen </span> of <span class="codeph"> dia </span> overgangseffect. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> afstand </span> </span> </p> </td> 
   <td colname="col2"> <p>De afstand tussen aangrenzende frames in <span class="codeph"> dia </span> overgang, heeft de waaier van <span class="codeph"> 0 </span> doorheen <span class="codeph"> 1 </span> en is relatief ten opzichte van de breedte van de component. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

Geen.

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
