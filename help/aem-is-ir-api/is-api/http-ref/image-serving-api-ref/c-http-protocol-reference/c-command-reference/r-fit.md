---
description: Modus Reactieafbeelding passend. Hiermee geeft u op hoe de schaalfactor wordt berekend. Deze wordt gebruikt om de samengestelde afbeelding te schalen naar de reactieafbeelding wanneer de reactiegrootte met wid= en hei= en scl= niet is opgegeven.
seo-description: Modus Reactieafbeelding passend. Hiermee geeft u op hoe de schaalfactor wordt berekend. Deze wordt gebruikt om de samengestelde afbeelding te schalen naar de reactieafbeelding wanneer de reactiegrootte met wid= en hei= en scl= niet is opgegeven.
seo-title: aanpassen
solution: Experience Manager
title: aanpassen
topic: Scene7 Image Serving - Image Rendering API
uuid: 669fe757-f3a1-4cd4-b46c-6fbe5a039ce0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 0%

---


# fit{#fit}

Modus Reactieafbeelding passend. Hiermee geeft u op hoe de schaalfactor wordt berekend. Deze wordt gebruikt om de samengestelde afbeelding te schalen naar de reactieafbeelding wanneer de reactiegrootte met wid= en hei= en scl= niet is opgegeven.

` fit= *``*, *`modeupscale`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> mode  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|constraine|crop|wrap|stretch|hfit|vfit  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> verhogen  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
 </tr> 
</table>

In de volgende beschrijving van de modusopties wordt ervan uitgegaan dat *`xScale`* de verhouding is tussen de breedte van de samengestelde afbeelding en de breedte van de responsieafbeelding en *`yScale`* de verhouding is tussen de hoogte van de samengestelde afbeelding en de hoogte van de reactieafbeelding.

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Definitie </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> aanpassen  </span> </p> </td> 
   <td colname="col2"> <p>Schaalt de samengestelde afbeelding zodanig dat deze past in de ruimte die wordt toegewezen met <span class="codeph"> wid= </span> en <span class="codeph"> hei= </span>, met minimale witruimte en geen uitsnijden. De reactieafbeelding heeft de exacte grootte die is opgegeven met <span class="codeph"> wid= </span> en <span class="codeph"> hei= </span>. De kleinste waarde van <span class="varname"> xScale </span> en <span class="varname"> yScale </span> wordt toegepast. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> beperken  </span> </p> </td> 
   <td colname="col2"> <p>Schaalt de samengestelde afbeelding als <span class="codeph"> passend </span> zodat deze past in de ruimte die wordt toegewezen met <span class="codeph"> wid= </span> en <span class="codeph"> hei= </span>, maar de werkelijke responsimage kan kleiner zijn dan opgegeven met <span class="codeph"> wid= </span> en <span class="codeph"> hei= </span> om witruimte te voorkomen. De kleinste waarde van <span class="varname"> xScale </span> en <span class="varname"> yScale </span> wordt toegepast. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> uitsnijden  </span> </p> </td> 
   <td colname="col2"> <p>Hiermee schaalt u de samengestelde afbeelding, zodat deze de volledige reactieafbeelding vult, met minimale uitsnijding en geen witruimte. De grootste van <span class="varname"> xScale </span> en <span class="varname"> yScale </span> wordt toegepast. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> wrap  </span> </p> </td> 
   <td colname="col2"> <p>Hiermee schaalt u de samengestelde afbeelding zoals <span class="codeph"> uitsnijden </span>, zodat deze het gehele reactiebeeld bedekt, maar de werkelijke reactieafbeelding kan groter zijn dan opgegeven met <span class="codeph"> wid= </span> en <span class="codeph"> hei= </span> om uitsnijden te voorkomen. De grootste van <span class="varname"> xScale </span> en <span class="varname"> yScale </span>wordt toegepast. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> uitrekken  </span> </p> </td> 
   <td colname="col2"> <p>Hiermee schaalt u de samengestelde afbeelding afzonderlijk in x en y om de hele reactieafbeelding te vullen, zonder uitsnijden en zonder witruimte. Dit wijzigt doorgaans de hoogte-breedteverhouding van de afbeelding. <span class="varname"> xScale  </span> wordt gebruikt voor horizontale schaling en  <span class="varname"> yScale  </span> voor verticale schaling. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit  </span> </p> </td> 
   <td colname="col2"> <p>Hiermee past u <span class="varname"> xScale </span> toe om de afbeelding horizontaal precies passend te maken, met uitsnijden of witruimte boven en/of onder mogelijk. Nuttig voor speciale toepassingen. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit  </span> </p> </td> 
   <td colname="col2"> <p>Hiermee past u <span class="varname"> yScale </span> toe om de afbeelding verticaal precies passend te maken, met uitsnijden of witruimte aan de linkerkant en/of rechterkant. Nuttig voor speciale toepassingen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Stel *`upscale`* in op &#39;1&#39; om upscaling toe te staan of op &#39;0&#39; om *`xScale`*en *`yScale`* te beperken tot 1:1. Als upscaling is uitgeschakeld, kan er extra witruimte aanwezig zijn als de samengestelde afbeelding kleiner is dan de reactieafbeelding.

Uitsnijden en witruimte worden standaard gecentreerd. hun positie kan worden bepaald met `align=`. De kleur en dekking van de vulling met witruimte worden bepaald door `bgc=`.

## Eigenschappen {#section-6d7a5a7e18434bca9bc2fdb236af8909}

Kenmerk weergeven. Is van toepassing ongeacht de huidige laaginstelling. Ten minste een van `wid=` of `hei=` moet ook worden opgegeven, anders wordt een fout geretourneerd; zowel `wid=` als `hei=` moeten worden gespecificeerd om de geschikte wijzen te gedragen zoals beschreven. Er wordt een fout geretourneerd wanneer `req=tmb` ook wordt opgegeven.

## Standaard {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## Zie ook {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
