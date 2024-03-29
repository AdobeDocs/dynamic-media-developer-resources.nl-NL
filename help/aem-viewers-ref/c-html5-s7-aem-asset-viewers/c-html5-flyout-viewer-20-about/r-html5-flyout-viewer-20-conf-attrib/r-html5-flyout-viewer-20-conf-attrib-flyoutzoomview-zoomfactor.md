---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 150968d2-aece-4d2a-b5a8-31b03dae25bb
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '178'
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

## Eigenschappen {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optioneel.

## Standaard {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## Voorbeeld {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
