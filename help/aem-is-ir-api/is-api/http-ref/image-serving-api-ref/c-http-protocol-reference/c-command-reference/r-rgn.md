---
description: Regio van belang. Hiermee geeft u een rechthoekig interessegebied (ROI) in de samengestelde afbeelding op, uitgedrukt in pixels.
seo-description: Regio van belang. Hiermee geeft u een rechthoekig interessegebied (ROI) in de samengestelde afbeelding op, uitgedrukt in pixels.
seo-title: rgn
solution: Experience Manager
title: rgn
topic: Scene7 Image Serving - Image Rendering API
uuid: 08657925-c52a-4279-8357-c26ad5c5ef3d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# rgn{#rgn}

Regio van belang. Hiermee geeft u een rechthoekig interessegebied (ROI) in de samengestelde afbeelding op, uitgedrukt in pixels.

rgn= *`coord`*, *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Pixelverschuiving van de linkerbovenhoek van de samengestelde afbeelding naar de linkerbovenhoek van de ROI (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> size</span> </p></td> 
  <td class="stentry"> <p>Grootte van de ROI in pixels (int, int). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=` definieert alleen een ROI zonder de afbeelding uit te snijden. Wanneer `wid=` en/of `hei=` groter dan grootte ook worden toegepast, kunnen extra gegevens van het samengestelde beeld in het definitieve antwoordbeeld zichtbaar zijn.

## Eigenschappen {#section-53edb35f4e364d7ca13fd0886e8b0c86}

Kenmerk weergeven. Is van toepassing ongeacht de huidige laaginstelling.

Om het even welke gebieden van het ROI die zich buiten het samengestelde beeld uitbreiden worden opgevuld met `bgc=`.

`rgn=` wordt toegepast vóór de definitieve schaling en aanpassing met `scl=`, `wid=`, `hei=`, `fit=`, `rect=`, of `align=`.

## Standaard {#section-6a3df8f670084def900ffef9dab7e94a}

Gehele samengestelde afbeelding ( `rgn=0,0,width,height`).

## Zie ook {#section-07883760f25c4d17aedbee36b7883891}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)[align=, fit=,rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)
