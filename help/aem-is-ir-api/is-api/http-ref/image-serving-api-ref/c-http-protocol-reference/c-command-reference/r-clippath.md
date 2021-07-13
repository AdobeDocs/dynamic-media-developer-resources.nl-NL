---
description: Laaguitknippad. Hiermee geeft u een clippad voor de huidige laag op.
solution: Experience Manager
title: clipPath
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# clipPath{#clippath}

Laaguitknippad. Hiermee geeft u een clippad voor de huidige laag op.

`clipPath= *`pathDefinition`*`

`clipPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Padgegevens. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Naam van pad dat is ingesloten in bronafbeelding van laag (alleen ASCII). </p></td> 
 </tr> 
</table>

Alle delen van de laag die buiten het gebied vallen dat wordt gedefinieerd door `clipPath=`, worden transparant gemaakt.

`*``*` pathName is de naam van een pad dat is ingesloten in de bronafbeelding van de laag. Het pad wordt automatisch getransformeerd om de relatieve uitlijning met de inhoud van de afbeelding te behouden. Als meer dan één `*`pathName`*` wordt gespecificeerd, klemt de server het beeld aan de doorsnede van deze wegen. `*`pathName`*` niet gevonden in de bronafbeelding wordt genegeerd.

>[!NOTE]
>
>Alleen ASCII-tekenreeksen worden ondersteund voor `*`pathName`*`.

`*`Met `*` pathDefinition kunnen expliciete padgegevens worden opgegeven in pixelcoördinaten van lagen.

Als `size=` wordt gespecificeerd en niet 0.0, is de laag presized. In dit geval zijn padcoördinaten relatief ten opzichte van de linkerbovenhoek van de laagrechthoek en wordt de laag geplaatst op basis van `origin=` of de standaardinstelling ervan. Eventuele gebieden van het pad buiten de laagrechthoek blijven transparant.

Wanneer `size=` niet is opgegeven voor een effen kleur of een tekstlaag, wordt de laag beschouwd als een laag van zichzelf te wijzigen, waarbij de grootte van het pad wordt bepaald. Wanneer `origin=` niet is opgegeven, wordt standaard ingesteld op (0,0) van de coördinaatruimte van het pad. Hierdoor kunnen in feite padcoördinaten worden opgegeven ten opzichte van de oorsprong van laag 0.

>[!NOTE]
>
>`scale=`,  `rotate=`en  `anchor=` opdrachten zijn niet toegestaan voor lagen met effen kleuren waarvan het formaat automatisch wordt aangepast.

`*``*` pathDefinition accepteert een tekenreeks die lijkt op de waarde van het  `d=` kenmerk van het SVG- `<path>` element, behalve dat komma&#39;s worden gebruikt in plaats van spaties om waarden te scheiden. `*``*` pathDefinition kan een of meer subpaden met gesloten lus bevatten.

De volgende padopdrachten worden ondersteund in `*`pathDefinition`*`:

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
   <td> <b> </b> <span class="varname"> Mx,y</span> </td> 
   <td> <p> absoluut </p> </td> 
   <td> <p> Start een nieuw subpad op x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> </b> <span class="varname"> mx,y</span> </td> 
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
   <td> <b> Z</b> |  <b>z</b> </td> 
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

Laagkenmerk. Wordt toegepast op de huidige laag of op de samengestelde afbeelding als `layer=comp`. Effectlagen negeren deze.

`clipPathE=` wordt genegeerd als er geen pad met de opgegeven naam is gevonden in de bronafbeelding van de laag of als de laagbron geen afbeelding is.

## Standaard {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Geen, voor geen extra uitknippen van de laag.

## Zie ook {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) ,  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) ,  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
