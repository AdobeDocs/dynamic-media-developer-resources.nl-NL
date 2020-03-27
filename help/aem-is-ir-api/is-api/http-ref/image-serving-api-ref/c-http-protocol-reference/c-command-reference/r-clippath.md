---
description: Laaguitknippad. Hiermee geeft u een clippad voor de huidige laag op.
seo-description: Laaguitknippad. Hiermee geeft u een clippad voor de huidige laag op.
seo-title: clipPath
solution: Experience Manager
title: clipPath
topic: Scene7 Image Serving - Image Rendering API
uuid: fe84cf7a-63af-47d3-ae4f-2122f2f0a262
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# clipPath{#clippath}

Laaguitknippad. Hiermee geeft u een clippad voor de huidige laag op.

`clipPath= *`pathDefinition`*`

`clipPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span></span> </p> </td> 
  <td class="stentry"> <p>Padgegevens. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Naam van pad dat is ingesloten in bronafbeelding van laag (alleen ASCII). </p></td> 
 </tr> 
</table>

Alle delen van de laag die buiten het door gedefinieerde gebied vallen, `clipPath=` worden transparant gemaakt.

` *`pathName`*` is de naam van een pad dat is ingesloten in de bronafbeelding van de laag. Het pad wordt automatisch getransformeerd om de relatieve uitlijning met de inhoud van de afbeelding te behouden. Als er meer dan één ` *`pathName`*` is opgegeven, knipt de server de afbeelding naar het snijpunt van deze paden. Eventuele ` *`pathName`*` die niet in de bronafbeelding worden gevonden, wordt genegeerd.

>[!NOTE]
>
>Alleen ASCII-tekenreeksen worden ondersteund voor ` *`pathName`*`.

` *`pathDefinition`*` maakt het mogelijk expliciete padgegevens op te geven in pixelcoördinaten van lagen.

Wanneer `size=` u een waarde opgeeft die niet gelijk is aan 0,0, wordt de grootte van de laag gewijzigd. In dit geval zijn padcoördinaten relatief ten opzichte van de linkerbovenhoek van de laagrechthoek en wordt de laag op basis van `origin=` of de standaardinstelling geplaatst. Eventuele gebieden van het pad buiten de laagrechthoek blijven transparant.

Wanneer `size=` geen waarde is opgegeven voor een effen kleur of tekstlaag, wordt de laag beschouwd als een laag van zichzelf te wijzigen, waarbij de grootte van het pad wordt bepaald. Als `origin=` deze niet is opgegeven, wordt de standaardwaarde (0,0) van de coördinaatruimte van het pad gebruikt. Hierdoor kunnen in feite padcoördinaten worden opgegeven ten opzichte van de oorsprong van laag 0.

>[!NOTE]
>
>`scale=`, `rotate=`en `anchor=` opdrachten zijn niet toegestaan voor lagen met effen kleuren waarvan het formaat automatisch wordt aangepast.

` *`pathDefinition`*` accepteert een tekenreeks die lijkt op de waarde van het `d=` kenmerk van het SVG- `<path>` element, behalve dat komma&#39;s worden gebruikt in plaats van spaties om waarden te scheiden. ` *`pathDefinition`*` kan een of meer subpaden met gesloten lus bevatten.

De volgende padopdrachten worden ondersteund in ` *`pathDefinition`*`:

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Opdracht</b> </th> 
   <th class="entry"> <b> Naam</b> </th> 
   <th class="entry"> <b> Beschrijving</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <b> M</b> <span class="varname"> x,y</span> </td> 
   <td> <p> absoluut </p> </td> 
   <td> <p> Start een nieuw subpad op x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> m</b> <span class="varname"> x,y</span> </td> 
   <td> <p> verplaatsen naar relatief </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto absoluut </p> </td> 
   <td> <p> Teken een lijn van de huidige positie naar x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto relatief </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> absoluut </p> </td> 
   <td> <p> Teken een Bézier-curve van de huidige positie naar x,y. x1,y1 is het besturingspunt aan het begin van de curve en x2,y2 is het besturingspunt aan het einde van de curve. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto relatief </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> sluiten </p> </td> 
   <td> <p> Sluit het huidige subpad met een rechte lijn. </p> </td> 
  </tr> 
 </tbody> 
</table>

Opdrachten in hoofdletters geven aan dat de coördinaatwaarden in absolute pixelposities staan (ten opzichte van de linkerbovenhoek van de laagrechthoek). Pixelverschuivingen volgen opdrachten in kleine letters ten opzichte van de huidige positie.

&#39;m&#39; of &#39;M&#39; begint altijd een nieuw subpad. Subpaden worden automatisch gesloten (met een rechte lijn) als &#39;Z&#39; of &#39;z&#39; niet is opgegeven aan het einde.

Als een subpad begint met een relatieve beweging (&#39;m&#39;), is het relatief ten opzichte van een van de volgende:

* Het beginpunt van het vorige subpad, als dit is gesloten met &#39;z&#39; of &#39;Z&#39;.
* Het eindpunt van het vorige subpad, als dit niet expliciet is gesloten.
* 0,0, als dit het eerste subpad is.

## Eigenschappen {#section-d4127db0dac54e3cbd44f7ea1e001960}

Laagkenmerk. Is van toepassing op de huidige laag of op de samengestelde afbeelding, indien van toepassing `layer=comp`. Effectlagen negeren deze.

`clipPathE=` wordt genegeerd als er geen pad met de opgegeven naam is gevonden in de bronafbeelding van de laag of als de laagbron geen afbeelding is.

## Standaard {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Geen, voor geen extra uitknippen van de laag.

## Zie ook {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) , [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
