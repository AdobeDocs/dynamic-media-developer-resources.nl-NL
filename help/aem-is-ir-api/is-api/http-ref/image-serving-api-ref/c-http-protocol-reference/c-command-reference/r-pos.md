---
description: Positie laag.
seo-description: Positie laag.
seo-title: pos
solution: Experience Manager
title: pos
topic: Scene7 Image Serving - Image Rendering API
uuid: e9872ce9-5c47-49c5-9c87-4fa8441c4770
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---


# pos{#pos}

Positie laag.

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>De pixelverschuiving van de oorsprong van deze laag naar de oorsprong van de laag 0 (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Genormaliseerde verschuiving van oorsprong van deze laag naar oorsprong van laag 0 (reëel, reëel). </p></td> 
 </tr> 
</table>

In het geval van afbeeldings-, tekst- en effen-kleurlagen geeft `pos=` de positie van een laaganker op ten opzichte van het anker van laag 0. `posN=` coördinaatwaarden worden genormaliseerd ten opzichte van de werkelijke grootte van de laag 0 rect.

Bij effectlagen verschuift `pos=` de effectlaag ten opzichte van de bovenliggende laag.

Bij een positieve waarde wordt de laag naar rechts/onder verplaatst en naar links/boven negatief. `posN=0.5,0.5` Hiermee verplaatst u de laag met de helft van de breedte en hoogte van de laag naar beneden en naar rechts.

## Eigenschappen {#section-51a60cdc52d040538fef378ace7c2e7d}

Laagkenmerk. Genegeerd als `layer=0` of `layer=comp`.

## Standaard {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. Hierdoor wordt het laaganker op dezelfde locatie geplaatst als het anker van laag 0 als dit een afbeelding, tekst of een effen kleurlaag is. Hiermee plaatst u een effectlaag rechtstreeks boven of onder de bovenliggende laag.

## Voorbeeld {#section-a89a02c22f6b4260bfcf7c842cd6069d}

Zie voorbeeld A in [Sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Zie ook {#section-812d95575ba542808e8387d0a8650606}

[oorsprong=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
