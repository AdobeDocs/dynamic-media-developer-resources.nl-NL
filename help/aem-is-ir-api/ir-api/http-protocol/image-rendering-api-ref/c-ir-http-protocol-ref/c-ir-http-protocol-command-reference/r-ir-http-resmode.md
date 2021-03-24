---
description: Modus Nieuwe pixels berekenen. Hiermee selecteert u het algoritme voor resampling en/of interpolatie dat moet worden gebruikt om de gerenderde afbeelding te schalen naar de grootte die met wid=, hei= of scl= is opgegeven.
solution: Experience Manager
title: resMode
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# resMode{#resmode}

Modus Nieuwe pixels berekenen. Hiermee selecteert u het algoritme voor resampling en/of interpolatie dat moet worden gebruikt om de gerenderde afbeelding te schalen naar de grootte die met wid=, hei= of scl= is opgegeven.

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bilin  </span> </p> </td> 
   <td colname="col2"> <p>Hiermee selecteert u de standaard bilineaire interpolatie. Snelste methode voor het berekenen van nieuwe monsters; sommige aliasingartefacten kunnen waarneembaar zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>Selecteert bicubische interpolatie. Meer CPU-intensief dan bilineaire interpolatie, maar levert scherpere beelden op met minder merkbare aliasing-artefacten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>Selecteert een gewijzigde functie van het Venster Lanczos als interpolatiealgoritme. Dit levert mogelijk iets scherpere resultaten op dan bicubisch tegen hogere CPU-kosten. </p> <p> <span class="codeph"> shark  </span> is vervangen door  <span class="codeph"> sharé2  </span>, waardoor het minder waarschijnlijk is dat aliasing artefacten ontstaan, ook wel Moiré genoemd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp  </span> </p> </td> 
   <td colname="col2"> <p>Hiermee selecteert u het standaardresampler <span class="keyword"> voor de Adobe Photoshop </span> voor het verkleinen van de afbeeldingsgrootte. Dit wordt 'bicubische scherper' genoemd in <span class="keyword"> Adobe Photoshop </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-ea7029f37e094d9cb85646b85fbac0ce}

Kan overal binnen het verzoek voorkomen. Genegeerd als er geen definitieve afbeeldingsschaling is toegepast.

## Standaard {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## Zie ook {#section-16c557a2250e4f04b3e6cbef18add9ce}

[kenmerk::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) ,  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
