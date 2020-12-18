---
description: 'null'
seo-description: 'null'
seo-title: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
topic: Dynamic media
uuid: 832ebacf-d57f-4efa-ab1a-6a454f7c7a32
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---


# TableOfContents.bearing{#tableofcontents-bearing}

[!DNL `[TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`]

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> lateraal|verticaal passend</span> </p> </td> 
   <td> <p> Hiermee bepaalt u de richting van de vormgeving van het vervolgkeuzepaneel. </p> <p>Wanneer ingesteld op <span class="codeph"> fit-vertical</span>, verplaatst de component eerst de positie van het basispaneel naar de bodem van zijn knoop en probeert om het paneel of aan het recht of aan de linkerkant van de basisplaats uit te rollen. Bij elke poging controleert de component of het deelvenster is bijgesneden door een buitencontainer. Als alle pogingen mislukken, probeert de component om de positie van het basispaneel naar de bovenkant te verschuiven en rollopouten in de juiste en linkerrichting te herhalen. </p> <p>Wanneer ingesteld op <span class="codeph"> fit-lateraal</span>, gebruikt de component een gelijkaardige logica, maar verschuift de basis eerst naar rechts, waarbij de rolrichtingen omlaag en omhoog worden geprobeerd. Vervolgens verschuift het de basis naar links en probeert het de richting omlaag en omhoog. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> Hiermee stelt u de vertraging in seconden in voor de timer voor automatisch verbergen van de vervolgkeuzelijst, die het deelvenster verbergt wanneer een gebruiker inactief is. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-55436ddd78b04f538dbb9a7a8463feae}

Optioneel.

## Standaard {#section-049d3f94c9794510906c6f81d6cc5485}

[!DNL `fit-vertical,2`]

## Voorbeeld {#section-68ff51c4e2b740c995fc5109cc0063bd}

[!DNL `bearing=fit-vertical,0.5`]
