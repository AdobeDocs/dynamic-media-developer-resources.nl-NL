---
title: align
description: Uitlijning van structuurrenderen. Hiermee geeft u op welke oorsprongpunten door het geselecteerde vignetobject moeten worden gebruikt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---

# align {#align}

Uitlijning van structuurrenderen. Hiermee geeft u op welke oorsprongpunten door het geselecteerde vignetobject moeten worden gebruikt.

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Standaard oorsprong (midden-overeenkomst). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
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

De renderer past de structuur op het object toe, zodat het structuurankerpunt ( `anchor=`) samenvalt met het opgegeven punt van oorsprong.

Elk object kan maximaal zes oorsprongspunten definiëren (0, 1, 3, 4, 5, 6). Als een `align` -waarde wordt opgegeven, maar het corresponderende oorsprongpunt wordt niet gedefinieerd door het vignetobject. Het standaardoorsprongpunt (midden-overeenkomst) wordt gebruikt.

`align=2` Geeft willekeurige structuuruitlijning aan, in welk geval `anchor=` wordt genegeerd.

Meestal gebruikt voor bekledingsmaterialen, mogelijk voor kleding, om de uitlijning van de structuur tussen aangrenzende objecten te beheren.

## Eigenschappen {#section-350fadc87dcf4812a8a02d1c3d6697a0}

Materiaalkenmerk. Genegeerd als een wand-, kast-, apparaat- of vensterbekledingsframeobject is geselecteerd of als het materiaal geen herhaalbare structuur is.

## Standaard {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`, als het materiaal is gebaseerd op een catalogusitem, anders 0 (gecentreerd).

## Zie ook {#section-945d1ce275df487d9d564d4043156c79}

[catalogus::Uitlijning](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
