---
description: Laag uitbreiden. Hiermee voegt u marges toe aan een laag of snijdt u de laagrechthoek bij.
seo-description: Laag uitbreiden. Hiermee voegt u marges toe aan een laag of snijdt u de laagrechthoek bij.
seo-title: uitbreiden
solution: Experience Manager
title: uitbreiden
topic: Scene7 Image Serving - Image Rendering API
uuid: 7ca69994-e788-41a9-93ac-f22b6b9920d0
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# uitbreiden{#extend}

Laag uitbreiden. Hiermee voegt u marges toe aan een laag of snijdt u de laagrechthoek bij.

`extend= *``*, *``*, *``*, *`linksRechtsonder`*`

`extendN= *``*, *``*, *``*, *`leftNtopNrightNbottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> links,boven,onder,rechts</span></span> </p></td> 
  <td class="stentry"> <p>Aantal pixels dat moet worden toegevoegd aan (of verwijderd uit, als de waarde negatief is) de linker-, boven-, rechter- en onderrand van de laagrect (int, int, int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>De hoeveelheid ruimte die aan de linker-, boven-, rechter- en onderrand van de laagrect moet worden toegevoegd (of uit deze rand moet worden verwijderd als de waarde negatief is), uitgedrukt als genormaliseerde hoeveelheden ten opzichte van de grootte van de oorspronkelijke laagrect (reëel, reëel, reëel). </p></td> 
 </tr> 
</table>

`extend=` wordt toegepast op de laag *nadat* de afbeelding is uitgesneden ( `crop=`) en alle laagtransformaties, inclusief `rotate=`, zijn toegepast.

Het uitgebreide gebied wordt gevuld met `bgColor=`, of blijft transparant als dit niet is opgegeven.

De argumentwaarden voor `extendN=` worden genormaliseerd ten opzichte van de grootte van de laagrechthoek nadat de laagtransformaties, inclusief `rotate=` zijn toegepast.

## Eigenschappen {#section-8fc94de871f841f3bf5e1df135972ca9}

Laagkenmerk. Is van toepassing op laag 0 als `layer=comp`. Genegeerd door effectlagen.

## Standaard {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`, voor geen wijziging van de laagrechthoek.

## Voorbeelden {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**Snijd een afbeelding uit en voeg vervolgens een rode rand van 5 pixels breed toe:**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**Schaal een afbeelding naar een breedte van 200 pixels en voeg titeltekst toe in een marge van 30 pixels boven de afbeelding.**

De hoogte van de samengestelde afbeelding hangt af van de hoogte-breedteverhouding van de afbeelding.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## Zie ook {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b), [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
