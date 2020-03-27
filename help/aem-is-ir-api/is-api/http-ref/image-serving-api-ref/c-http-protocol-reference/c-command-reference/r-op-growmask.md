---
description: Afbeelding vervagen/eroderen. Past een morfologische dilaat (straal > 0) of erode (straal < 0) op de maskergegevens toe.
seo-description: Afbeelding vervagen/eroderen. Past een morfologische dilaat (straal > 0) of erode (straal < 0) op de maskergegevens toe.
seo-title: op_kwekenMasker
solution: Experience Manager
title: op_kwekenMasker
topic: Scene7 Image Serving - Image Rendering API
uuid: 016501e8-33c5-4c9e-8d26-120b1e929c55
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_kwekenMasker{#op-growmask}

Afbeelding vervagen/eroderen. Past een morfologische dilaat (straal > 0) of erode (straal &lt; 0) op de maskergegevens toe.

`op_growMask= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>Straal verwateren/eroderen in pixels, waarbij de straal wordt verondersteld van toepassing te zijn op het volledige resolutiemasker en daarom wordt verkleind voor gedownsampled maskers (int -100..100). </p></td> 
 </tr> 
</table>

Primair gebruikt om een masker lichtjes te kweken of te krimpen om artefacten rond de rand van het masker te vermijden.

## Eigenschappen {#section-b1c66d65168d4ea695e8662ea690bd4e}

Is van toepassing op de huidige laag of op laag `0` als `layer=comp`.

## Standaard {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`, voor niets.

## Zie ook {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Laageffecten](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_kweken](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)
