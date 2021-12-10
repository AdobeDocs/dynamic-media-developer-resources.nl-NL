---
title: TableOfContents.bearing
description: TableOfContents.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b140c9ba-353d-49ef-9e6b-f5bc45e0dbfd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# TableOfContents.bearing{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> lateraal|verticaal passend</span> </p> </td> 
   <td> <p> Hiermee bepaalt u de richting van de vormgeving van het vervolgkeuzepaneel. </p> <p>Wanneer ingesteld op <span class="codeph"> verticaal passend</span>De component verschuift eerst de positie van het basisdeelvenster naar de onderkant van de knop en probeert het deelvenster naar rechts of naar links uit te rollen vanaf de basislocatie. Bij elke poging controleert de component of het deelvenster is bijgesneden door een buitencontainer. Als alle pogingen mislukken, probeert de component om de positie van het basispaneel naar de bovenkant te verschuiven en rollout pogingen in de juiste en linkerrichting te herhalen. </p> <p>Wanneer ingesteld op <span class="codeph"> monteerbaar</span>, gebruikt de component een gelijkaardige logica, maar verschuift de basis eerst naar het recht, die neer en omhoog roloutrichtingen probeert. Vervolgens verschuift het de basis naar links en probeert het de rollout richtingen omlaag en omhoog. </p> </td> 
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

`fit-vertical,2`

## Voorbeeld {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
