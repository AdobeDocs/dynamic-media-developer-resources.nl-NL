---
title: textAttr
description: Kenmerken tekstlaag. Geeft extra kenmerken op voor tekstlagen die niet beschikbaar zijn als rtf-opdrachten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c8a3d2a-2524-436a-8bc7-60241af0fd17
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# textAttr{#textattr}

Kenmerken tekstlaag. Geeft extra kenmerken op voor tekstlagen die niet beschikbaar zijn als rtf-opdrachten.

` textAttr= *`res`*[, *`antiAliasing`*[, *`resMode`*[, *`wordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res </span> </span> </p> </td> 
  <td class="stentry"> <p>Dit biedt een manier om de tekstlaag te schalen zonder de tekengrootte te wijzigen. Bij hogere resolutiewaarden neemt de grootte van de gerenderde tekst toe ten opzichte van de canvasgrootte. Bij lagere waarden wordt de tekst kleiner. Tekstresolutie in dots per inch (int groter dan 0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> antiAliasing </span> </span> </p> </td> 
  <td class="stentry"> <p>Bepaalt de anti-aliasingmodus die wordt gebruikt door de text rendering engine. </p> <p> <span class="codeph"> uit | norm | zuiver | scherp | sterk | vloeiend </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> uit </span> </p> </td> 
      <td class="stentry"> <p>Anti-aliasing van tekst uitschakelen. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> norm </span> </p> </td> 
      <td class="stentry"> <p>De standaardmodus voor anti-aliasing van tekst inschakelen (standaard). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> scherp </span> </p> </td> 
      <td class="stentry"> <p>Anti-aliasingmodus voor Photoshop selecteren <span class="codeph"> scherp </span> ( <span class="codeph"> textPs= </span> alleen). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> scherp </span> </p> </td> 
      <td class="stentry"> <p>Anti-aliasingmodus voor Photoshop selecteren <span class="codeph"> scherp </span> ( <span class="codeph"> textPs= </span> alleen). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> sterk </span> </p> </td> 
      <td class="stentry"> <p>Anti-aliasingmodus voor Photoshop selecteren <span class="codeph"> sterk </span> ( <span class="codeph"> textPs= </span> alleen). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>Bepaalt hoe res wordt gebruikt bij het renderen van de tekst </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes </span> </p> </td> 
      <td class="stentry"> <p>Gebruik de opgegeven resolutie. </p> <p>Gebruik deze optie als de tekst moet worden weergegeven in een exacte grootte ten opzichte van het samengestelde canvas. Tekst kan worden bijgesneden tot de laaggrootte (indien opgegeven) als het tekstvak te klein is. Dit is de enige <span class="varname"> resMode </span> optie ondersteund door <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes </span> </p> </td> 
      <td class="stentry"> <p>Pas de resolutie automatisch aan om de laagrechthoek het beste te vullen met de tekst. </p> <p>Gebruik deze optie om de tekstgrootte automatisch aan te passen, zodat het tekstvak zoveel mogelijk wordt gevuld, zonder dat er een risico op afkapping bestaat. Als tekstomloop is ingeschakeld, kan de tekst worden teruggeplaatst met de uiteindelijke resolutie. De <span class="varname"> res </span> wordt genegeerd als <span class="codeph"> autoRes </span> is geselecteerd. Niet ondersteund door <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes </span> </p> </td> 
      <td class="stentry"> <p>Gebruik de opgegeven resolutie; verlaag deze indien nodig om te voorkomen dat tekst wordt afgekapt naar de laagrechthoek. </p> <p>Gebruik deze optie om tekst met de opgegeven resolutie te renderen, zolang er geen bijsnijden plaatsvindt. Als er wordt bijgesneden, wordt de resolutie automatisch verlaagd om ervoor te zorgen dat alle tekst zich volledig in het tekstvak bevindt. Als tekstomloop is ingeschakeld, kan de tekst worden teruggeplaatst met de uiteindelijke resolutie. Niet ondersteund door <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>Als de grootte van de tekstlaag niet is opgegeven met size= of als alleen de breedte is opgegeven, worden de instellingen 'autoRes' en 'maxRes' genegeerd. In dergelijke gevallen wordt de opgegeven resolutie gebruikt om de tekst te renderen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap </span> </span> </p> </td> 
  <td class="stentry"> <p>Hiermee geeft u de omloopmodus op. </p> <p> <span class="codeph"> wrap | noWrap | nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap </span> </p> </td> 
      <td class="stentry"> <p>Word-wrap uitschakelen. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> wrap </span> </p> </td> 
      <td class="stentry"> <p>Standaardtekstomloop inschakelen. </p> <p>Het breekt zo nodig lange woorden. <span class="codeph"> textPs= </span> alleen ondersteuning <span class="codeph"> wrap </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>Tekstomloop inschakelen. </p> <p>Hiermee breekt u nooit een woord, zelfs niet als het aan het einde wordt afgekapt. Meestal gebruikt met <span class="codeph"> autoRes </span> of <span class="codeph"> maxRes </span> ervoor te zorgen dat lange woorden nooit worden gebroken . </p> </td> 
     </tr> 
    </table> </p> <p>Beide <span class="codeph"> wrap </span> en <span class="codeph"> nbwrap </span> automatische tekstomloop op woordgrenzen en afbreekstreepjes. </p> </td> 
 </tr> 
</table>

## Eigenschappen {#section-114ca0b8585b403c873e2251478ad1d5}

Kenmerk tekstlaag. Genegeerd door afbeeldings-, effen kleur- en effectlagen. Van toepassing op `layer=0` indien gespecificeerd voor `layer=comp`.

## Standaard {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## Zie ook {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
