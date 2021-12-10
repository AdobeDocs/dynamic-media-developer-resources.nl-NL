---
title: FavoritesMenu.bearing
description: Hiermee bepaalt u de richting van de dianavigatie voor de knoppencontainer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: f08545fd-f039-41a1-ad0b-430ce7c1bdd1
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

Hiermee bepaalt u de richting van de dianavigatie voor de knoppencontainer.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateraal</span> </p> </td> 
   <td colname="col2"> <p> Wanneer ingesteld op <span class="codeph"> omhoog</span>, <span class="codeph"> omlaag</span>, <span class="codeph"> left</span>, of <span class="codeph"> right</span>wordt het deelvenster in de opgegeven richting uitgelijnd zonder dat er een extra controle op de grenzen plaatsvindt. Dit betekent dat het deelvenster wordt bijgesneden door een buitencontainer. </p> <p>Wanneer ingesteld op <span class="codeph"> verticaal passend</span>verschuift de component eerst de positie van het basisdeelvenster naar de onderkant van het menu Favorieten. Het probeert om het paneel in één van de volgende richtingen van zulk basisplaats uit te rollen: onder, rechts, links. Bij elke poging controleert de component of het deelvenster is bijgesneden door een buitencontainer. Als alle pogingen mislukken, probeert de component om de positie van het basispaneel naar de bovenkant te verschuiven en rolloverpogingen van een bovenkant, juist, en linkerrichting te herhalen. </p> <p>Wanneer ingesteld op <span class="codeph"> monteerbaar</span>, gebruikt de component een vergelijkbare logica. De basis wordt eerst naar rechts verplaatst en probeert rechts, omlaag en omhoog de richting uit te rollen. Vervolgens verschuift het de basis naar links, waarbij naar links, omlaag en omhoog routebeschrijving wordt geprobeerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
