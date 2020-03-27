---
description: 'null'
seo-description: 'null'
seo-title: CarouselView.frametransition
solution: Experience Manager
title: CarouselView.frametransition
topic: Dynamic media
uuid: 9539ede1-08fb-4bfc-8a5a-870c7d84de7f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *``*[, *`tijdsspatiëring`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|faden|dia </span> </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u het type effect op dat wordt toegepast op de framewijziging. <span class="codeph"> geen </span> staat voor een overgang; de framewijziging gebeurt onmiddellijk. </p> <p> <span class="codeph"> vervagen </span> betekent een overgang tussen oude en nieuwe frames met vervaging. </p> <p> <span class="codeph"> dia activeert overgang waar het oude kader uit de mening glijdt en het nieuwe kader binnen schuift. </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duur </span></span> </p> </td> 
   <td colname="col2"> <p>Hiermee bepaalt u de duur (in seconden) van het effect <span class="codeph"> Vervagen </span> of <span class="codeph"> Diaovergang </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> tussenruimte </span></span> </p> </td> 
   <td colname="col2"> <p>De afstand tussen aangrenzende frames in een <span class="codeph"> dia- </span> overgang ligt tussen <span class="codeph"> 0 </span> en <span class="codeph"> 1 </span> en is relatief ten opzichte van de breedte van de component. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

Geen.

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
