---
description: Modus Structuur herhalen. Hiermee bepaalt u de herhalingsmodus voor herhaalbare structuurmaterialen.
seo-description: Modus Structuur herhalen. Hiermee bepaalt u de herhalingsmodus voor herhaalbare structuurmaterialen.
seo-title: herhalen
solution: Experience Manager
title: herhalen
topic: Scene7 Image Serving - Image Rendering API
uuid: 6508fdff-27cd-4038-b506-39b927f3526a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 12%

---


# repeat{#repeat}

Modus Structuur herhalen. Hiermee bepaalt u de herhalingsmodus voor herhaalbare structuurmaterialen.

`repeat=0...19`

<table id="simpletable_0D54E62EAF50482A95EDE166D0645D9E"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Rechte herhaling. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>willekeurige verdeling in vier richtingen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>willekeurige verdeling in acht richtingen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Ruitvormige betegeling. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Achtergrond met kwartdrop hangend. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Achtergrond van drie druppels hangen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p> </td> 
  <td class="stentry"> <p>Achtergrond voor halve neerslag hangend. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p> </td> 
  <td class="stentry"> <p>Achtergrond met vijf druppels hangend. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p> </td> 
  <td class="stentry"> <p>Achtergrond omkeren hangend. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p> </td> 
  <td class="stentry"> <p>Willekeurige achtergrond hangt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10 </p> </td> 
  <td class="stentry"> <p>Willekeurig neerzetten. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11 </p> </td> 
  <td class="stentry"> <p>Willekeurig over. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12 </p> </td> 
  <td class="stentry"> <p>Half over. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13 </p> </td> 
  <td class="stentry"> <p>Spiegelen (boekovereenkomst). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14 </p> </td> 
  <td class="stentry"> <p>Standaard randomizer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15 </p> </td> 
  <td class="stentry"> <p>Hoge frequentie randomizer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16 </p> </td> 
  <td class="stentry"> <p>Lage-frequentie randomizer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17 </p> </td> 
  <td class="stentry"> <p>Horizontale randomizer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18 </p> </td> 
  <td class="stentry"> <p>Verticale randomizer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19 </p> </td> 
  <td class="stentry"> <p>Randrandrandomizer. </p> </td> 
 </tr> 
</table>

De willekeurige opvulmodi (14...18) kunnen worden gebruikt om structuren te synthetiseren op basis van beelden die niet gemakkelijk herhaalbaar zijn; het algoritme zal volledig willekeurige of gedeeltelijk willekeurige texturen tot stand brengen die op het originele beeld worden gebaseerd.

## Eigenschappen {#section-262bf540930d4890b678ea00cefe1909}

Materiaalkenmerk. Wordt genegeerd door effen kleuren, decal en kabinetsmaterialen.

## Standaard {#section-e5bbd7d9fbb74852849e605d20f550bb}

`catalog::Repeat`, als het materiaal op een catalogusitem is gebaseerd, anders  `0` (recht herhalen).

## Zie ook {#section-ac99113b64654d75a3a86e41db546269}

[catalogus::Herhalen](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-repeat.md#reference-20e149211e1f4e8285db5ecb83c1902e)
