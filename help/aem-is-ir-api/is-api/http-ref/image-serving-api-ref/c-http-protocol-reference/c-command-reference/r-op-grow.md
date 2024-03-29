---
title: op_kweken
description: Afbeelding vervagen/eroderen. Hiermee past u een morfologische dilaat (straal > 0) of erode (straal < 0) toe op de afbeeldingsgegevens.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4c5bef4e-f80e-454d-8e93-30bf33d7ec9e
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '107'
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

`*`radius`*` in pixels ten opzichte van de samengestelde afbeelding. Als de afbeelding een gekleurde afbeelding is, wordt elke component afzonderlijk verwerkt.

Wordt voornamelijk gebruikt om de grootte van laageffecten te wijzigen. Dit is ook handig voor speciale effecten op tekstlagen of effen kleurlagen met maskers.

## Eigenschappen {#section-b1c66d65168d4ea695e8662ea690bd4e}

Laagkenmerk. Is van toepassing op de huidige laag of op de samengestelde afbeelding als `layer=comp`.

## Standaard {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`, voor niets.

## Zie ook {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Laageffecten](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
