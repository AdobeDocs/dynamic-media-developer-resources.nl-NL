---
title: kwantificeren
description: Kleurkwantiteit. Geeft kleurkwantiseringskenmerken op voor GIF-uitvoerconversie.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# kwantificeren{#quantize}

Kleurkwantiteit. Geeft kleurkwantiseringskenmerken op voor GIF-uitvoerconversie.

` quantize= *`type`*[, *`dithering`*[, *`numColors`*[, *`colorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptief|web|mac} </span> palettype </p> <p>Selecteren ' <span class="codeph"> web </span>' of ' <span class="codeph"> mac </span>" om een vooraf gedefinieerd palet te kiezen of op " <span class="codeph"> adaptief </span>om een optimaal palet voor de afbeelding te berekenen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dithering </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} </span> dithering, opties </p> <p>Selecteer 'diffuse' voor Floyd-Steinberg-foutdiffusie of 'off' om dithering uit te schakelen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>Het aantal uitvoerkleuren (geheel getal) dat is opgenomen in de \" <span class="codeph"> adaptief </span>". </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> moet tussen 2 en 256 liggen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
  <td class="stentry"> <p>Door komma's gescheiden lijst met geforceerde RGB kleuren in hexadecimale 6-indeling. Hiermee kunt u geforceerde kleuren opgeven die moeten worden opgenomen in een ' <span class="codeph"> adaptief </span>". Als het opgegeven aantal kleuren kleiner is dan <span class="codeph"> numColors </span>extra kleuren worden berekend op basis van de inhoud van de afbeelding. </p> <p>Wordt alleen gebruikt als <span class="codeph"> fmt=gif </span> of <span class="codeph"> fmt=gif-alpha </span>. Anders genegeerd. De kleuren die zijn opgegeven met <span class="codeph"> <span class="varname"> colorList </span> </span> moet RGB-waarden zijn in hex6-indeling (zie <span class="codeph"> kleur </span>); er zijn geen andere kleurspecificaties toegestaan. </p> </td> 
 </tr> 
</table>

## Standaard {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Voorbeeld {#section-b3a979dc9ae3459baa093bf17310988f}

Een miniatuur van een GIF genereren met de &#39; `web`&#39; en geen dithering:

[!DNL `http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`]

Zet de afbeelding om in een bitonaal GIF met kleurentransparantie en forceer de kleuren in zwart-wit:

[!DNL `http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`]
