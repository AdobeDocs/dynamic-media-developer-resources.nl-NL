---
description: Hiermee bepaalt u de richting van de dianavigatie voor de knoppencontainer.
solution: Experience Manager
title: FavoritesMenu.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# FavoritesMenu.bearing{#favoritesmenu-bearing}

Hiermee bepaalt u de richting van de dianavigatie voor de knoppencontainer.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateraal</span> </p> </td> 
   <td colname="col2"> <p> Wanneer ingesteld op <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span>, of <span class="codeph"> right</span>, rolt het paneel uit in gespecificeerde richting zonder een extra grenscontrole, die in paneel het knippen door een buitencontainer resulteert. </p> <p>Wanneer ingesteld op <span class="codeph"> fit-vertical</span>, verplaatst de component eerst de positie van het basispaneel naar de bodem van het menu van Favorieten en probeert om het paneel in één van de volgende richtingen van zulk basisplaats uit te rollen: onder, rechts, links. Bij elke poging controleert de component of het deelvenster is bijgesneden door een buitencontainer. Als alle pogingen mislukken, probeert de component om de positie van het basispaneel naar de bovenkant te verschuiven en rollopogingen van een bovenkant, juist, en linkerrichting te herhalen. </p> <p>Wanneer ingesteld op <span class="codeph"> fit-lateraal</span>, gebruikt de component een gelijkaardige logica. De basis wordt eerst naar rechts verplaatst en probeert rechts, omlaag en omhoog de richting uit te rollen. Vervolgens verschuift het de basis naar links, waarbij naar links, omlaag en omhoog routebeschrijving wordt geprobeerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
