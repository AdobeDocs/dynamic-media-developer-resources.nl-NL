---
description: Afbeelding vervagen/eroderen. Hiermee past u een morfologische dilaat (straal > 0) of erode (straal < 0) toe op de afbeeldingsgegevens.
seo-description: Afbeelding vervagen/eroderen. Hiermee past u een morfologische dilaat (straal > 0) of erode (straal < 0) toe op de afbeeldingsgegevens.
seo-title: op_kweken
solution: Experience Manager
title: op_kweken
topic: Dynamic Media Image Serving - Image Rendering API
uuid: bc9bf889-f7e1-4a65-b6d6-7e1257ef8c11
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# op_kweken{#op-grow}

Afbeelding vervagen/eroderen. Hiermee past u een morfologische dilaat (straal > 0) of erode (straal &lt; 0) toe op de afbeeldingsgegevens.

`op_grow= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p> </td> 
  <td class="stentry"> <p>Straal verwateren/eroderen in pixels (int -100..100). </p></td> 
 </tr> 
</table>

`*`De `*` stralen worden uitgedrukt in pixels ten opzichte van de samengestelde afbeelding. Als de afbeelding een gekleurde afbeelding is, wordt elke component afzonderlijk verwerkt.

Wordt voornamelijk gebruikt om de grootte van laageffecten te wijzigen. Dit is ook handig voor speciale effecten op tekstlagen of effen kleurlagen met maskers.

## Eigenschappen {#section-b1c66d65168d4ea695e8662ea690bd4e}

Laagkenmerk. Wordt toegepast op de huidige laag of op de samengestelde afbeelding als `layer=comp`.

## Standaard {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`, voor niets.

## Zie ook {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Laageffecten](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
