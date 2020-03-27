---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
topic: Dynamic media
uuid: 8c4e6bf8-0238-470b-9fbe-262eb17f8f3b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`primaryFactorsecundairFactorupscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaire factor</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u de vergroting van de afbeelding voor de vervolgweergave ten opzichte van de hoofdweergave op. Moet een geheel getal of een drijvende-kommawaarde <span class="codeph"> 1,0</span> of hoger zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secundaire factor</span></span> </p> </td> 
   <td colname="col2"> <p> U kunt een optionele secundaire factor opgeven die toegankelijk is door op de hoofdweergave te klikken of erop te tikken wanneer de markering actief is. Wanneer u nogmaals klikt of tikt, wordt de primaire zoomfactor hersteld. De waarde <span class="codeph"> -1</span> schakelt de secundaire zoomfactor uit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> verhogen</span></span> </p> </td> 
   <td colname="col2"> <p>Hiermee bepaalt u hoe kleine afbeeldingen worden verwerkt. </p> <p>Indien ingesteld op <span class="codeph"> 1</span> , wordt de hoofdafbeelding geschaald, zodat deze past in de hoofdweergave. Bovendien wordt de vergroting van de zoomafbeelding vergroot, zodat het geconfigureerde gebied van het vervolgvenster volledig wordt gevuld. </p> <p>Als de waarde is ingesteld op <span class="codeph"> 0</span> , worden kleine afbeeldingen met hun oorspronkelijke resolutie weergegeven en wordt de weergave gecentreerd weergegeven in het hoofdweergavegebied en in het vervolgvenster. U kunt extra witruimte rond de afbeelding configureren met een achtergrond of een vergelijkbare CSS-eigenschap van de CSS-klassen <span class="codeph"> s7flyoutzoomview</span> en <span class="codeph"> s7flyoutzoom</span> in respectievelijk de hoofdweergave en het vervolgvenster. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optioneel.

## Standaard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## Voorbeeld {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
