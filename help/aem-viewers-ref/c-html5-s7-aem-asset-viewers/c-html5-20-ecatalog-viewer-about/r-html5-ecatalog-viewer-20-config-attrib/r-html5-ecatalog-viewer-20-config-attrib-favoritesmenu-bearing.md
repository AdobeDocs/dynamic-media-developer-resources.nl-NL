---
description: Hiermee bepaalt u de richting van de dianavigatie voor de knoppencontainer.
seo-description: Hiermee bepaalt u de richting van de dianavigatie voor de knoppencontainer.
seo-title: FavorietenMenu.iling
solution: Experience Manager
title: FavorietenMenu.iling
topic: Dynamic media
uuid: badc02ef-2724-41bb-9b00-c65966be8577
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FavorietenMenu.iling{#favoritesmenu-bearing}

Hiermee bepaalt u de richting van de dianavigatie voor de knoppencontainer.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateraal</span> </p> </td> 
   <td colname="col2"> <p> Wanneer het deelvenster is ingesteld op <span class="codeph"> Omhoog</span>, <span class="codeph"> Omlaag</span>, <span class="codeph"> links</span>of <span class="codeph"> rechts</span>, wordt het in de opgegeven richting rolt zonder dat er een extra controle op de begrenzingen plaatsvindt. Dit betekent dat het deelvenster wordt bijgesneden door een buitencontainer. </p> <p>Wanneer ingesteld op <span class="codeph"> passend maken-verticaal</span>, verschuift de component eerst de positie van het basisdeelvenster naar de onderkant van het menu Favorieten en wordt geprobeerd het deelvenster in een van de volgende richtingen uit te rollen vanaf een dergelijke basislocatie: onder, rechts, links. Bij elke poging controleert de component of het deelvenster is bijgesneden door een buitencontainer. Als alle pogingen mislukken, probeert de component om de positie van het basispaneel naar de bovenkant te verschuiven en rollopogingen van een bovenkant, juist, en linkerrichting te herhalen. </p> <p>Wanneer de component op <span class="codeph"> fit-lateraal</span>wordt geplaatst, gebruikt de component een gelijkaardige logica. De basis wordt eerst naar rechts verplaatst en probeert rechts, omlaag en omhoog de richting uit te rollen. Vervolgens verschuift het de basis naar links, waarbij naar links, omlaag en omhoog routebeschrijving wordt geprobeerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
