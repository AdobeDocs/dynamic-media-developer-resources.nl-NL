---
description: Hiermee bepaalt u de richting van de dianavigatie voor de knoppencontainer.
seo-description: Hiermee bepaalt u de richting van de dianavigatie voor de knoppencontainer.
seo-title: FavoritesMenu.bearing
solution: Experience Manager
title: FavoritesMenu.bearing
topic: Dynamic media
uuid: c3f415ad-f976-464a-9067-a5d526908352
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---


# FavoritesMenu.bearing{#favoritesmenu-bearing}

Hiermee bepaalt u de richting van de dianavigatie voor de knoppencontainer.

[!DNL `[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`]

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

[!DNL `fit-vertical`]

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `bearing=left`]
