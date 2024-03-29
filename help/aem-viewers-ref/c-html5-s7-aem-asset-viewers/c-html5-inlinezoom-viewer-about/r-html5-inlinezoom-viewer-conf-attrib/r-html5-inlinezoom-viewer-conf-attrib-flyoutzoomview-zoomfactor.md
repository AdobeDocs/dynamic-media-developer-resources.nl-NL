---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 2a9d4450-a1a0-471c-86bf-105d516b0bd7
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secundairFactor`*][, *`verhogen`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u de vergroting van de afbeelding voor de vervolgweergave ten opzichte van de hoofdweergave op. Moet een geheel getal of een zwevende-kommawaarde zijn <span class="codeph"> 1,0</span> of groter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secundairFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> U kunt een optionele secundaire factor opgeven die toegankelijk is door op de hoofdweergave te klikken of erop te tikken wanneer de markering actief is. Wanneer u nogmaals klikt of tikt, wordt de primaire zoomfactor hersteld. Een waarde van <span class="codeph"> -1</span> Hiermee schakelt u de secundaire zoomfactor uit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> verhogen</span></span> </p> </td> 
   <td colname="col2"> <p>Hiermee bepaalt u hoe kleine afbeeldingen worden verwerkt. </p> <p>Indien ingesteld op <span class="codeph"> 1</span> de component vergroot of verkleint de hoofdafbeelding zodat deze in de hoofdweergave past. Bovendien wordt de vergroting van de zoomafbeelding vergroot, zodat het geconfigureerde gebied van het vervolgvenster volledig wordt gevuld. </p> <p>Indien ingesteld op <span class="codeph"> 0</span>kleine afbeeldingen worden met de oorspronkelijke resolutie weergegeven en worden gecentreerd weergegeven in het hoofdweergavegebied en in het vervolgvenster. U kunt extra witruimte rondom de afbeelding configureren met een achtergrond of een vergelijkbare CSS-eigenschap van de <span class="codeph"> s7flyoutzoomview</span> en <span class="codeph"> s7flyoutzoom</span> CSS-klassen in respectievelijk de hoofdweergave en het vervolgvenster. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optioneel.

## Standaard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## Voorbeeld {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
