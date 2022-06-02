---
title: kwantificeren
description: Kleurkwantiteit. Geeft kleurkwantiseringskenmerken op voor GIF-uitvoerconversie.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# kwantificeren{#quantize}

Kleurkwantiteit. Geeft kleurkwantiseringskenmerken op voor GIF-uitvoerconversie.

` quantize= *`type`*[, *`dithering`*[, *`numColors`*[, *`colorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptief|web|mac} </span> </p> <p>Hiermee geeft u het palettype op. </p> <p>Instellen op <span class="codeph"> adaptief </span> om een optimaal palet voor de afbeelding te berekenen. </p> <p>Instellen op <span class="codeph"> web </span> of <span class="codeph"> mac </span> om een vooraf gedefinieerd palet te kiezen. </p> <p> <p>Opmerking: De <span class="codeph"> mac </span> Type pallet wordt alleen ondersteund voor GIF- en PNG8-indelingen, maar niet voor GIF-Alpha- en PNG8-Alpha-indelingen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dithering </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off} </span> </p> <p>Hiermee geeft u de ditheringopties op. </p> <p>Instellen op <span class="codeph"> diffuus </span> voor Floyd-Steinberg foutverspreiding </p> <p>Instellen op <span class="codeph"> uit </span> om dithering uit te schakelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>Aantal uitvoerkleuren (2-256) </p> <p>Hiermee bepaalt u hoeveel kleuren worden opgenomen in het dialoogvenster <span class="codeph"> adaptief </span> palet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
   <td colname="col2"> <p>Een door komma's gescheiden lijst met geforceerde RGB-kleuren in hexadecimale 6-indeling </p> <p>Hiermee kunt u kleuren opgeven die in een <span class="codeph"> adaptief </span> palet. Als het opgegeven aantal kleuren kleiner is dan <span class="codeph"> <span class="varname"> numColors </span> </span>extra kleuren worden berekend op basis van de inhoud van de afbeelding. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-8ab5035055b24b858270d260912a7f3d}

Request-kenmerk. Ongeacht de huidige laaginstelling. Wordt alleen gebruikt als `fmt=gif`, `fmt=gif-alpha`, `fmt=png8`, of `fmt=png8-alpha`. Anders genegeerd.

De kleuren die zijn opgegeven met *`colorList`* moet bestaan uit RGB-waarden in hex6-indeling (zie [kleur](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md) zonder `0x` voorvoegsel. Andere kleurspecificaties zijn niet toegestaan. *`numColors`* moet tussen 2 en 256 liggen.

## Standaard {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Voorbeeld {#section-e34aca7587d548a7ae9d4266b80c9451}

Een miniatuur van een GIF genereren met de opdracht `web` palet en geen dithering:

` http:// *`server`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Zet de afbeelding om in een bitonal-GIF met toetsenbordkleurtransparantie en forceer de kleuren naar zwart-wit:

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Zie ook {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [kleur](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
