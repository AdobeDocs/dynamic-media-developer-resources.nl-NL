---
description: Afbeeldingsanker (hotspot). Hiermee geeft u het structuurankerpunt (hotspot) van de herhaalbare structuur of het decale materiaal op.
seo-description: Afbeeldingsanker (hotspot). Hiermee geeft u het structuurankerpunt (hotspot) van de herhaalbare structuur of het decale materiaal op.
seo-title: anker
solution: Experience Manager
title: anker
topic: Scene7 Image Serving - Image Rendering API
uuid: 1e695882-f97a-4208-b595-2851b91bdbfe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# anker{#anchor}

Afbeeldingsanker (hotspot). Hiermee geeft u het structuurankerpunt (hotspot) van de herhaalbare structuur of het decale materiaal op.

`anchor= *``*, *`xy`*`

`anchorN= *``*, *`xnyn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>,  <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>Pixelverschuiving ten opzichte van de linkerbovenhoek van de bronafbeelding (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>,  <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>Genormaliseerde verschuiving ten opzichte van het midden van de bronafbeelding (reëel, reëel). </p></td> 
 </tr> 
</table>

Er wordt een herhaalbare structuur toegepast op een vignetobject, zodat het structuurankerpunt ( `anchor=`) zich op het oorsprongpunt van de structuur van het object bevindt.

Er wordt een decimale afbeelding toegepast op een vignetobject, zodat het decale ankerpunt zich op het decimale oorsprongpunt van het object bevindt. De decimale positie kan verder worden aangepast met de opdracht `pos=`.

`anchorN=0,0` plaatst het afbeeldingsanker in het midden van de bronafbeelding. `anchorN=-0.5,-0.5` of  `anchor=0,0` bevindt zich in de linkerbovenhoek en  `anchorN=0.5,0.5` bevindt zich in de rechterbenedenhoek van de bronafbeelding.

## Eigenschappen {#section-91f929d35cd745ab9e1eeecf45fcedae}

**Materiaalkenmerk**. Genegeerd als `align=2`, of als het materiaal geen herhaalbare textuur, een achtergrond, of een decal is.

## Standaard {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`, als het materiaal op een catalogusitem is gebaseerd. Anders `anchor=0,0` (de linkerbovenhoek van de afbeelding) voor herhaalbare structuren en achtergronden en `anchorN=0,0` (het midden van de afbeelding) voor decimalen.

## Zie ook {#section-b18bf0b035644ca5aedebbc64373718e}

[catalogus::Anker](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) ,  [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
