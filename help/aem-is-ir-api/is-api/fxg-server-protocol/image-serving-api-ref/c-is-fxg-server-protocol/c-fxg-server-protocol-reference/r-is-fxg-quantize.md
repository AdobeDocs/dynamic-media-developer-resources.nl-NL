---
description: Kleurkwantiteit. Geeft kleurkwantiseringskenmerken voor GIF-uitvoerconversie op.
seo-description: Kleurkwantiteit. Geeft kleurkwantiseringskenmerken voor GIF-uitvoerconversie op.
seo-title: kwantificeren
solution: Experience Manager
title: kwantificeren
topic: Scene7 Image Serving - Image Rendering API
uuid: 624cdc45-51f2-4b18-a658-311770974521
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---


# quantize{#quantize}

Kleurkwantiteit. Geeft kleurkwantiseringskenmerken voor GIF-uitvoerconversie op.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptief|web|mac}  </span> palettype </p> <p>Selecteer ' <span class="codeph"> web </span>' of ' <span class="codeph"> mac </span>' om een vooraf gedefinieerd palet te kiezen, of selecteer ' <span class="codeph"> adaptief </span>' om een optimaal palet voor de afbeelding te berekenen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dithering  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off}  </span> dithering-opties </p> <p>Selecteer 'diffuse' voor Floyd-Steinberg-foutdiffusie of 'off' om dithering uit te schakelen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
  <td class="stentry"> <p>Aantal uitvoerkleuren (geheel getal) in het adaptieve <span class="codeph">-palet.</span> </p> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> moet tussen 2 en 256 liggen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
  <td class="stentry"> <p>Lijst met door komma's gescheiden geforceerde RGB-kleuren in hexadecimale 6-indeling. Hiermee kunt u geforceerde kleuren opgeven die moeten worden opgenomen in een adaptief <span class="codeph">-palet. </span> Als het opgegeven aantal kleuren kleiner is dan <span class="codeph"> numColors </span>, worden extra kleuren berekend op basis van de inhoud van de afbeelding. </p> <p>Wordt alleen gebruikt als <span class="codeph"> fmt=gif </span> of <span class="codeph"> fmt=gif-alpha </span>. Anders genegeerd. De kleuren die worden opgegeven met <span class="codeph"> <span class="varname"> colorList </span> </span> moeten RGB-waarden zijn in hex6-indeling (zie <span class="codeph"> kleur </span>); er zijn geen andere kleurspecificaties toegestaan . </p> </td> 
 </tr> 
</table>

## Standaard {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Voorbeeld {#section-b3a979dc9ae3459baa093bf17310988f}

Genereer een GIF-miniatuur met het palet &#39; `web`&#39; en geen dithering:

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

Zet de afbeelding om in een bitonale GIF met toetkleurtransparantie en forceer de kleuren naar zwart-wit:

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
