---
description: Kenmerken Tekst op pad.
seo-description: Kenmerken Tekst op pad.
seo-title: pathAttr
solution: Experience Manager
title: pathAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: b0ca5821-ee08-4c18-919d-775b75f19acd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# pathAttr{#pathattr}

Kenmerken Tekst op pad.

` pathAttr= *``*[, *``*[, *`directionstartPosendPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> richting </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> norm </span> | <span class="codeph"> omgekeerd </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos </span> </p> </td> 
  <td class="stentry"> <p>Startpositie van tekst op pad (real 0.0...1.0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos </span> </p> </td> 
  <td class="stentry"> <p>Eindpositie van tekst op pad (reëel 0.0...&lt;2.0). </p> </td> 
 </tr> 
</table>

Geef op `norm` of u tekst wilt tekenen die begint bij het eerste padhoekpunt en `reverse` dat u tekst in de tegenovergestelde richting tekent, te beginnen bij het laatste hoekpunt.

*`startPos`* en *`endPos`* kunt u aanpassen waar op het pad de tekst wordt getekend. 0,0 komt overeen met het eerste hoekpunt in het pad en 1,0 met het laatste hoekpunt; Met tussenliggende waarden wordt de afstand uitgedrukt langs het pad tussen het eerste en laatste hoekpunt.

## Eigenschappen {#section-80f266da4e2549d89f022a3f9ff4584d}

Laagkenmerk. Genegeerd als de laag geen `textPs=` en `textPath=` opdrachten bevat.

*`startPos`* moet groter zijn dan of gelijk zijn aan 0 en kleiner dan 1,0. moet groter *`endPos`* en kleiner dan of gelijk aan 1,0 *`startPos`* zijn bij toepassing op een open pad, of kleiner dan of gelijk aan ( *`startPos`* + 1,0) bij toepassing op een gesloten pad.

## Standaard {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## Zie ook {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
