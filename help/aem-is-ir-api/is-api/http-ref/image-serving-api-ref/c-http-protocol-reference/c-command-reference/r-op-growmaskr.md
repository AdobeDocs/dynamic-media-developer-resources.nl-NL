---
description: Afbeelding vervagen/eroderen. Past een morfologische dilaat (straal > 0) of erode (straal < 0) op de maskergegevens toe.
solution: Experience Manager
title: op_growMaskR
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7abfbccf-8bcf-44d4-b50a-eca7a3f11360
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---

# op_growMaskR{#op-growmaskr}

Afbeelding vervagen/eroderen. Past een morfologische dilaat (straal > 0) of erode (straal &lt; 0) op de maskergegevens toe.

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>Straal drogen/eroderen in pixels waarin <span class="codeph"><span class="varname"> radiusR</span></span> wordt toegepast zoals is, ongeacht of het masker is gedownsampled (int -100..100). </p></td> 
 </tr> 
</table>

Primair gebruikt om een masker lichtjes te kweken of te krimpen om artefacten rond de rand van het masker te vermijden.

## Eigenschappen {#section-b1c66d65168d4ea695e8662ea690bd4e}

Is van toepassing op de huidige laag of op de laag `0` indien `layer=comp`.

## Standaard {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`, voor niets.

## Zie ook {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Laageffecten](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_kweken](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_kwekenMasker](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
