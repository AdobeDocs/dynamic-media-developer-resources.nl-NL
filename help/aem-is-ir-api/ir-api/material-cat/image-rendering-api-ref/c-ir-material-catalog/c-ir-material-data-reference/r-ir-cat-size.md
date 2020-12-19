---
description: Decal size. Breedte, hoogte en dikte van een decaal materiaalobject.
seo-description: Decal size. Breedte, hoogte en dikte van een decaal materiaalobject.
seo-title: Grootte
solution: Experience Manager
title: Grootte
topic: Scene7 Image Serving - Image Rendering API
uuid: 07d41f71-e18d-4559-afc7-75dc1c45be93
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---


# Grootte{#size}

Decal size. Breedte, hoogte en dikte van een decaal materiaalobject.

## Eigenschappen {#section-967bf1112eec4032a91ed0c8a7b10a07}

Drie echte getallen, gescheiden door komma&#39;s. Mag niet negatief zijn. Ongebruikte waarden instellen op 0. volgnullen mogen worden weggelaten.

Geef alleen de breedte en de hoogte op als de afbeelding moet worden uitgerekt zodat deze binnen de opgegeven grootte past (de hoogte-breedteverhouding kan veranderen). Stel de breedte of hoogte in om de afbeelding proportioneel te schalen. Stel zowel de breedte als de hoogte in op 0 om `catalog::Resolution`de objectgrootte te bepalen.

Geef een waarde voor de dikte op om een slagschaduw toe te voegen aan het decimale object. Facultatief voor decal materialen, genegeerd door alle andere materialen.

## Standaard {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. Dit geeft aan dat de decimale grootte moet worden bepaald op basis van de volgende catalogus::Resolutie, en dat het object geen dikte heeft (er wordt dus geen slagschaduw gerenderd).

## Voorbeelden {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>Het decal wordt geforceerd tot 12x3 duim in grootte en heeft geen dikte (dit is, geen slagschaduw). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>Het decal is 5 duim breed, de hoogte wordt bepaald door de aspectverhouding van het beeld, en een slagschaduw wordt teruggegeven gebaseerd op een dikte van 1 duim. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0, 0,5 </p></td> 
  <td class="stentry"> <p>De breedte en hoogte van het decal worden bepaald door de catalogus::Resolutie, en dat deze 1,5 cm dik is. </p></td> 
 </tr> 
</table>

## Zie ook {#section-31a164e781d14e92bd9d379d3c329e92}

[catalogus:Resolutie](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
