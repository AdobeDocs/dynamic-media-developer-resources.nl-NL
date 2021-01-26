---
description: Uitlijning van structuurrenderen. Hiermee geeft u op welke oorsprongpunten door het geselecteerde vignetobject moeten worden gebruikt.
seo-description: Uitlijning van structuurrenderen. Hiermee geeft u op welke oorsprongpunten door het geselecteerde vignetobject moeten worden gebruikt.
seo-title: align
solution: Experience Manager
title: align
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0b24cd82-f9b2-48f4-9052-8c2026370ff7
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 2%

---


# align{#align}

Uitlijning van structuurrenderen. Hiermee geeft u op welke oorsprongpunten door het geselecteerde vignetobject moeten worden gebruikt.

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Standaard oorsprong (midden-overeenkomst). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Continu overeenkomende oorsprong. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Willekeurige uitlijning. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3,6 </p></td> 
  <td class="stentry"> <p>Door gebruiker gedefinieerde oorsprong. </p></td> 
 </tr> 
</table>

De renderer past de structuur op het object toe, zodat het structuurankerpunt ( `anchor=`) samenvalt met het opgegeven oorsprongpunt.

Elk object kan maximaal 6 oorsprongspunten definiëren (0,1, 3, 4, 5, 6). Wanneer een waarde `align` wordt opgegeven maar het corresponderende oorsprongpunt niet door het vignetobject wordt gedefinieerd, wordt het standaardoorsprongpunt (midden-overeenkomst) gebruikt.

`align=2` Hiermee geeft u willekeurige structuuruitlijning op. In dit geval  `anchor=` wordt de uitlijning van de structuur genegeerd.

Meestal gebruikt voor bekledingsmaterialen, mogelijk voor kleding, om de uitlijning van de structuur tussen aangrenzende objecten te beheren.

## Eigenschappen {#section-350fadc87dcf4812a8a02d1c3d6697a0}

Materiaalkenmerk. Genegeerd als een wand-, kast-, apparaat- of vensterbekledingsframeobject is geselecteerd of als het materiaal geen herhaalbare structuur is.

## Standaard {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`, als het materiaal is gebaseerd op een catalogusitem, anders 0 (gecentreerd).

## Zie ook {#section-945d1ce275df487d9d564d4043156c79}

[catalogus::Uitlijning](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [anker=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
