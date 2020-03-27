---
description: Type materiaaloppervlak. Hiermee geeft u het oppervlaktype van het materiaal op.
seo-description: Type materiaaloppervlak. Hiermee geeft u het oppervlaktype van het materiaal op.
seo-title: type
solution: Experience Manager
title: type
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f107d50-b363-4670-bb02-873677e7bbea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# type{#type}

Type materiaaloppervlak. Hiermee geeft u het oppervlaktype van het materiaal op.

`type=0...19`

<table id="simpletable_482728CD58144E7BBB2912B2F105FDCA"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Onbekend, server gebruikt standaard </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Overige </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Natuurlijk hout </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Gepolijst metaal </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p></td> 
  <td class="stentry"> <p>Geborsteld metaal </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p></td> 
  <td class="stentry"> <p>Verouderd metaal </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p></td> 
  <td class="stentry"> <p>Verf </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p></td> 
  <td class="stentry"> <p>Enamel/Lacquer </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p></td> 
  <td class="stentry"> <p>Achtergrond </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p></td> 
  <td class="stentry"> <p>Plastic </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10 </p></td> 
  <td class="stentry"> <p>Effen oppervlak </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11 </p></td> 
  <td class="stentry"> <p>Laminaat </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12 </p></td> 
  <td class="stentry"> <p>Vinyl </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13 </p></td> 
  <td class="stentry"> <p>Keramisch </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14 </p></td> 
  <td class="stentry"> <p>Natuursteen </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15 </p></td> 
  <td class="stentry"> <p>Glas </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16 </p></td> 
  <td class="stentry"> <p>Spiegelen </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17 </p></td> 
  <td class="stentry"> <p>Stof </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18 </p></td> 
  <td class="stentry"> <p>Zuiver weefsel </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19 </p></td> 
  <td class="stentry"> <p>tapijt </p></td> 
 </tr> 
</table>

Wordt gebruikt in combinatie met `gloss=` en `rough=` om het gedrag van reflectie- en glanseffecten te bepalen. Verschillende materialen zullen verschillende effecten hebben, ook al `gloss=` en `rough=` zijn ze hetzelfde.

## Eigenschappen {#section-2345b2508273426295ce8ac46182ea64}

Materiaalkenmerk. Genegeerd als het vignet geen 3-D reflectiegegevens bevat of als glanseffecten zijn uitgeschakeld in het vignet.

## Standaard {#section-0989055fb74a41a3b2f2a47fe7d90a42}

`catalog::Type` als het materiaal op een catalogusitem is gebaseerd. Anders `type=0`. Indien niet opgegeven, of indien `type=0`, selecteert de server een geschikte standaardinstelling afhankelijk van het doelobject en de andere materiaalkenmerken.

## Zie ook {#section-7cf808b0bb3d4b4fbb7b9a850d5a038b}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180)
