---
title: herhalen
description: Modus Structuur herhalen. Hiermee bepaalt u de herhalingsmodus voor herhaalbare structuurmaterialen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6cc82742-4ba0-4524-a87b-586539d7fe38
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 12%

---

# herhalen{#repeat}

Modus Structuur herhalen. Hiermee bepaalt u de herhalingsmodus voor herhaalbare structuurmaterialen.

`repeat=0...19`

<table id="simpletable_0D54E62EAF50482A95EDE166D0645D9E"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Rechte herhaling. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
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
  <td class="stentry"> <p>Achtergrond hangend, kwartdrop. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Achtergrond van derde druppel hangend. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p> </td> 
  <td class="stentry"> <p>Achtergrond voor halve neerslag hangend. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p> </td> 
  <td class="stentry"> <p>Achtergrond met 5-delige schaling hangend. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p> </td> 
  <td class="stentry"> <p>Achtergrond omkeren. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p> </td> 
  <td class="stentry"> <p>Willekeurige achtergrond hangend. </p> </td> 
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

Met de willekeurige overvulmodi (14...18) kunt u structuren samenstellen op basis van afbeeldingen die niet gemakkelijk herhaalbaar zijn. Met het algoritme maakt u volledig willekeurige of gedeeltelijk willekeurige structuren op basis van de oorspronkelijke afbeelding.

## Eigenschappen {#section-262bf540930d4890b678ea00cefe1909}

Materiaalkenmerk. Wordt genegeerd door effen kleuren, decal en kabinetsmaterialen.

## Standaard {#section-e5bbd7d9fbb74852849e605d20f550bb}

`catalog::Repeat`, als het materiaal op een catalogusitem is gebaseerd, anders `0` (recht herhalen).

## Zie ook {#section-ac99113b64654d75a3a86e41db546269}

[catalogus::Herhalen](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-repeat.md#reference-20e149211e1f4e8285db5ecb83c1902e)
