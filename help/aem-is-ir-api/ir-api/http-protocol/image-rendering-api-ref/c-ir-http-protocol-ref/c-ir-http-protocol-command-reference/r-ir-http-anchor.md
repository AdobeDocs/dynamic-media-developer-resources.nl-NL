---
title: anker
description: Afbeeldingsanker (hotspot). Hiermee geeft u het structuurankerpunt (hotspot) van de herhaalbare structuur of het decale materiaal op.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2c5dce-6eb1-4f05-80bd-7336deb08b9e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# anker{#anchor}

Afbeeldingsanker (hotspot). Hiermee geeft u het structuurankerpunt (hotspot) van de herhaalbare structuur of het decale materiaal op.

`anchor= *`x`*, *`y`*`

`anchorN= *`xn`*, *`yn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>, <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>Pixelverschuiving ten opzichte van de linkerbovenhoek van de bronafbeelding (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>, <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>Genormaliseerde verschuiving ten opzichte van het midden van de bronafbeelding (reëel, reëel). </p></td> 
 </tr> 
</table>

Er wordt een herhaalbare structuur toegepast op een vignetobject, zodat het structuurankerpunt ( `anchor=`) bevindt zich op de oorsprong van de structuur van het object.

Er wordt een decimale afbeelding toegepast op een vignetobject, zodat het decal-ankerpunt zich op het decal-oorsprongpunt van het object bevindt. De positie van het decimaalteken kan verder worden aangepast met behulp van de `pos=` gebruiken.

`anchorN=0,0` Plaatst het afbeeldingsanker in het midden van de bronafbeelding. `anchorN=-0.5,-0.5` of `anchor=0,0` zich in de linkerbovenhoek bevindt, en `anchorN=0.5,0.5` bevindt zich in de rechterbenedenhoek van de bronafbeelding.

## Eigenschappen {#section-91f929d35cd745ab9e1eeecf45fcedae}

**Materiaalkenmerk**. Genegeerd als `align=2`of als het materiaal geen herhaalbare structuur, achtergrond of decal is.

## Standaard {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`, als het materiaal op een catalogusitem is gebaseerd. Anders, `anchor=0,0` (de linkerbovenhoek van de afbeelding) voor herhaalbare structuren en achtergronden, en `anchorN=0,0` (het midden van de afbeelding) voor decimalen.

## Zie ook {#section-b18bf0b035644ca5aedebbc64373718e}

[catalogus::Anker](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) , [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
