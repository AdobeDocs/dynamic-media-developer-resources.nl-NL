---
description: Verscherp de structuur. Hiermee geeft u de verscherping op die moet worden toegepast bij het renderen van dit materiaal.
seo-description: Verscherp de structuur. Hiermee geeft u de verscherping op die moet worden toegepast bij het renderen van dit materiaal.
seo-title: scherp
solution: Experience Manager
title: scherp
topic: Scene7 Image Serving - Image Rendering API
uuid: 8265eebf-9cec-4ad3-8b22-0f46f33a89f1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scherp{#sharp}

Verscherp de structuur. Hiermee geeft u de verscherping op die moet worden toegepast bij het renderen van dit materiaal.

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Geen verscherping. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Normaal verscherpen (laat). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0 alternatief verscherpen (vroeg). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Meer verscherping (vroeg en laat). </p> </td> 
 </tr> 
</table>

`sharp=1` verscherping toepast nadat het materiaal is gerenderd; past verscherping toe na de eerste schaling van de structuur, maar voordat deze in de scène wordt omgezet; `sharp=2` Hiermee `sharp=3` past u verscherping toe voor en na de transformatie.

Het verscherpingsalgoritme en de mate van verscherping en andere USM-parameters (unsharp masking) worden bepaald door de standaardmateriaalsjabloon die door het vignet of met `rs=`wordt geboden.

## Eigenschappen {#section-498ec9fcb8eb415fb99532d36c11d4c7}

Materiaalkenmerk. Genegeerd door effen kleurmaterialen.

## Standaard {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`, als het materiaal op een catalogusitem is gebaseerd, anders `attribute::Sharp`.

## Zie ook {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catalogus::Verscherpen](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [verscherpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e), [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
