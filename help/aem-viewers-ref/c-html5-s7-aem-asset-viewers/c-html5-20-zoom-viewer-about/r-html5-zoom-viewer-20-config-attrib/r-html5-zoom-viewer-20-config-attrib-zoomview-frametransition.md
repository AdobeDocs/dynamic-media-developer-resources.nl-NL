---
description: ZoomView.frametransition
solution: Experience Manager
title: ZoomView.frametransition
topic: Dynamic media
uuid: 28e283ca-51d8-4d6c-9b8a-d16da21f4da1
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 1%

---


# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *``*[, *`tijdsspatiëring`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|faden|dia  </span> </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u het type effect op dat wordt toegepast op de framewijziging. <span class="codeph"> geen  </span> staat voor geen overgang; de framewijziging gebeurt onmiddellijk. <span class="codeph"> vervagen  </span> betekent een overgang tussen oude en nieuwe frames met vervaging. <span class="codeph"> dia  </span> activeert overgang waar het oude kader uit de mening glijdt en het nieuwe kader binnen schuift. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duur  </span> </span> </p> </td> 
   <td colname="col2"> <p>Geeft de duur (in seconden) aan van <span class="codeph"> vervagen </span> of <span class="codeph"> dia </span> overgangseffect. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> afstand  </span> </span> </p> </td> 
   <td colname="col2"> <p>De ruimte tussen aangrenzende kaders in <span class="codeph"> dia </span> overgang, heeft de waaier tussen <span class="codeph"> 0 </span> en <span class="codeph"> 1 </span> en is met betrekking tot de breedte van de component. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

Geen.

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
