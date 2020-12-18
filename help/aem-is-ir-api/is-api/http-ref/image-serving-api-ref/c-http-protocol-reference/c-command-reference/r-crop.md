---
description: Afbeelding uitsnijden. Hiermee geeft u een rechthoekig uitsnijdgebied op, uitgedrukt in pixels of genormaliseerd ten opzichte van de bronafbeelding of maskerafbeelding met volledige resolutie.
seo-description: Afbeelding uitsnijden. Hiermee geeft u een rechthoekig uitsnijdgebied op, uitgedrukt in pixels of genormaliseerd ten opzichte van de bronafbeelding of maskerafbeelding met volledige resolutie.
seo-title: uitsnijden
solution: Experience Manager
title: uitsnijden
topic: Scene7 Image Serving - Image Rendering API
uuid: c8eca467-7564-48a6-82d7-17f68a1399e1
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---


# uitsnijden{#crop}

Afbeelding uitsnijden. Hiermee geeft u een rechthoekig uitsnijdgebied op, uitgedrukt in pixels of genormaliseerd ten opzichte van de bronafbeelding of maskerafbeelding met volledige resolutie.

`crop= *``*, *`coördineren`*`

`cropN= *``*, *`coordNsizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span></span> </p> </td> 
  <td class="stentry"> <p>Pixelverschuiving van de linkerbovenhoek van de bronafbeelding naar de linkerbovenhoek van de uitsnijdvak (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>Genormaliseerde verschuiving van de linkerbovenhoek van de bronafbeelding naar de linkerbovenhoek van de uitsnijdvak (reëel, reëel). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> size</span></span> </p></td> 
  <td class="stentry"> <p>Grootte van de uitsnijdlijn in pixels (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>Genormaliseerde grootte van de uitsnijdvak ten opzichte van de grootte van de bronafbeelding (reëel, reëel). </p></td> 
 </tr> 
</table>

Kan ook worden gebruikt om de afbeelding buiten de grenzen te vergroten door negatieve x-, y-waarden en/of breedte en hoogtewaarden op te geven die groter zijn dan de breedte en hoogte van de afbeelding. In dit geval is het uitgebreide gebied volledig transparant (tenzij `bgColor=` is opgegeven).

## Eigenschappen {#section-632e0405bb9940679b5f8b1c10e0902e}

Kenmerk van bronafbeelding/masker. Wordt toegepast op de bronafbeelding van laag 0 als `layer=comp`. Genegeerd door lagen die niet zijn gekoppeld aan een bronafbeelding of -masker.

## Standaard {#section-41f62d386c664f77952bc22e7286bb88}

Gehele afbeelding ( `cropN=0,0,1,1`).

## Voorbeelden {#section-2c99b481c0a04321979a3b522aa295d1}

**Uitsnijden 10% van links en 10% van rechts:**

`…&cropN=0.1,0,0.8,1&…`

**20% uitsnijden ten opzichte van de onderrand van een afbeelding:**

`…&cropN=0,0,1,0.8&…`

## Zie ook {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [cropPathbgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
