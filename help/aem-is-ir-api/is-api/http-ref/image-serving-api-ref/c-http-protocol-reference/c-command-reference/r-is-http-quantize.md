---
description: Kleurkwantiteit. Geeft kleurkwantiseringskenmerken voor GIF-uitvoerconversie op.
seo-description: Kleurkwantiteit. Geeft kleurkwantiseringskenmerken voor GIF-uitvoerconversie op.
seo-title: kwantificeren
solution: Experience Manager
title: kwantificeren
topic: Scene7 Image Serving - Image Rendering API
uuid: 4e9c4807-59bc-4eb9-bcab-0bf0cfdf56d4
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---


# quantize{#quantize}

Kleurkwantiteit. Geeft kleurkwantiseringskenmerken voor GIF-uitvoerconversie op.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptief|web|mac}  </span> </p> <p>Hiermee geeft u het palettype op. </p> <p>Stel dit in op <span class="codeph"> adaptief </span> om een optimaal palet voor de afbeelding te berekenen. </p> <p>Stel in op <span class="codeph"> web </span> of <span class="codeph"> mac </span> om een vooraf gedefinieerd palet te kiezen. </p> <p> <p>Opmerking:  Het <span class="codeph"> mac </span> pallettype wordt alleen ondersteund voor GIF- en PNG8-indelingen, maar niet voor GIF-Alpha- en PNG8-Alpha-indelingen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dithering  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off}  </span> </p> <p>Hiermee geeft u de ditheringopties op. </p> <p>Instellen op <span class="codeph"> diffuse </span> voor Floyd-Steinberg-foutdiffusie </p> <p>Stel in op <span class="codeph"> uit </span> om dithering uit te schakelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
   <td colname="col2"> <p>Aantal uitvoerkleuren (2-256) </p> <p>Hiermee geeft u op hoeveel kleuren worden opgenomen in het adaptieve <span class="codeph">-palet.</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
   <td colname="col2"> <p>Een door komma's gescheiden lijst met geforceerde RGB-kleuren in hexadecimale 6-indeling </p> <p>Hiermee kunt u kleuren opgeven die moeten worden opgenomen in een <span class="codeph"> adaptief </span>-palet. Als het opgegeven aantal kleuren kleiner is dan <span class="codeph"> <span class="varname"> numColors </span> </span>, worden extra kleuren berekend op basis van de inhoud van de afbeelding. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-8ab5035055b24b858270d260912a7f3d}

Request-kenmerk. Ongeacht de huidige laaginstelling. Wordt alleen gebruikt als `fmt=gif`, `fmt=gif-alpha`, `fmt=png8` of `fmt=png8-alpha`. Anders genegeerd.

De kleuren die worden opgegeven met ` *`colorList`*` moeten bestaan uit RGB-waarden in hex6-indeling (zie ` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)`) zonder voorvoegsel &#39; `0x`&#39;. Andere kleurspecificaties zijn niet toegestaan. *`numColors`* moet tussen 2 en 256 liggen.

## Standaard {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Voorbeeld {#section-e34aca7587d548a7ae9d4266b80c9451}

Genereer een GIF-miniatuur met het palet `web` en geen dithering:

` http:// *`server`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Zet de afbeelding om in een bitonale GIF met toetkleurtransparantie en forceer de kleuren naar zwart-wit:

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Zie ook {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
