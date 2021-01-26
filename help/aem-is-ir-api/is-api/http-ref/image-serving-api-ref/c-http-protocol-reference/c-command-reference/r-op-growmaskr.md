---
description: Afbeelding vervagen/eroderen. Past een morfologische dilaat (straal > 0) of erode (straal < 0) op de maskergegevens toe.
seo-description: Afbeelding vervagen/eroderen. Past een morfologische dilaat (straal > 0) of erode (straal < 0) op de maskergegevens toe.
seo-title: op_growMaskR
solution: Experience Manager
title: op_growMaskR
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b81968e7-ebaf-426c-9230-1afcf4b5cf24
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# op_growMaskR{#op-growmaskr}

Afbeelding vervagen/eroderen. Past een morfologische dilaat (straal > 0) of erode (straal &lt; 0) op de maskergegevens toe.

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>Straal verwateren/eroderen in pixels waarin <span class="codeph"><span class="varname"> radiusR</span></span> ongewijzigd wordt toegepast, ongeacht of het masker is gedownsampled (int -100..100). </p></td> 
 </tr> 
</table>

Primair gebruikt om een masker lichtjes te kweken of te krimpen om artefacten rond de rand van het masker te vermijden.

## Eigenschappen {#section-b1c66d65168d4ea695e8662ea690bd4e}

Is van toepassing op de huidige laag of op laag `0` als `layer=comp`.

## Standaard {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`, voor niets.

## Zie ook {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Laageffecten](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_kweken](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_kwekenMasker](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
