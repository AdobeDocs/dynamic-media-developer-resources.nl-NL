---
description: Verscherpen. Verscherpen, kenmerk, bepaalt wanneer het materiaal wordt verscherpt tijdens het renderen.
seo-description: Verscherpen. Verscherpen, kenmerk, bepaalt wanneer het materiaal wordt verscherpt tijdens het renderen.
seo-title: Scherp
solution: Experience Manager
title: Scherp
topic: Scene7 Image Serving - Image Rendering API
uuid: f153f496-f2c5-43d0-a7f0-00045fd96af8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---


# Sharp{#sharp}

Verscherpen. Verscherpen, kenmerk, bepaalt wanneer het materiaal wordt verscherpt tijdens het renderen.

Het type en de mate van verscherping worden bepaald door het vignet via een standaardmateriaalsjabloon of met `catalog::RenderSettings`.

## Eigenschappen {#section-aac81b1a611b4bca90b8544eae7896df}

Enum.

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Geen verscherping. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Normale verscherping (na de transformatie). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Alternatieve verscherping (vóór de transformatie). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Meer verscherping (zowel voor als na de transformatie). </p></td> 
 </tr> 
</table>

Genegeerd door effen kleurmaterialen, optioneel voor alle andere materialen.

## Standaard {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` wordt gebruikt als het veld niet aanwezig is, leeg is of als de waarde niet een van de ondersteunde keuzen is.

## Zie ook {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[kenmerk::Verscherpen](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) ,  [catalogus::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd),  [sharpening=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
