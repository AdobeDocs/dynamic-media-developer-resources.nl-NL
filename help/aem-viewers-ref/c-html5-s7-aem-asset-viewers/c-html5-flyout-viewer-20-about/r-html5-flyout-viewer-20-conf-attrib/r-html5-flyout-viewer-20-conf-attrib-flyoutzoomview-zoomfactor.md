---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
topic: Dynamic media
uuid: 58d49de7-4828-46ae-b2e7-eb9398e98a99
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`primaryFactorsecundairFactorupscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u de vergroting van de afbeelding voor de vervolgweergave ten opzichte van de hoofdweergave op. Moet een geheel getal of een drijvende-kommawaarde <span class="codeph"> 1,0</span> of groter zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secundairFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> U kunt een optionele secundaire factor opgeven die toegankelijk is door op de hoofdweergave te klikken of erop te tikken wanneer de markering actief is. Wanneer u nogmaals klikt of tikt, wordt de primaire zoomfactor hersteld. De waarde <span class="codeph"> -1</span> schakelt de secundaire zoomfactor uit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> verhogen</span></span> </p> </td> 
   <td colname="col2"> <p>Hiermee bepaalt u hoe kleine afbeeldingen worden verwerkt. </p> <p>Indien ingesteld op <span class="codeph"> 1</span>, wordt de hoofdafbeelding zodanig geschaald dat deze in de hoofdweergave past. Bovendien wordt de vergroting van de zoomafbeelding vergroot, zodat het geconfigureerde gebied van het vervolgvenster volledig wordt gevuld. </p> <p>Indien ingesteld op <span class="codeph"> 0</span> worden kleine afbeeldingen weergegeven met hun oorspronkelijke resolutie en worden ze gecentreerd weergegeven in het hoofdweergavegebied en binnen het vervolgvenster. U kunt extra witruimte rond de afbeelding configureren met een achtergrond of een vergelijkbare CSS-eigenschap van de CSS-klassen <span class="codeph"> s7flyoutzoomview</span> en <span class="codeph"> s7flyoutzoom</span> in respectievelijk de hoofdweergave en het vervolgvenster. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optioneel.

## Standaard {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## Voorbeeld {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
