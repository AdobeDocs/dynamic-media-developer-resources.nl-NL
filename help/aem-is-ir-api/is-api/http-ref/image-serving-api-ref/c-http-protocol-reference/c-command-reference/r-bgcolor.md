---
description: Achtergrondkleur laag. Hiermee geeft u de achtergrondkleur en dekking van de huidige laag op.
seo-description: Achtergrondkleur laag. Hiermee geeft u de achtergrondkleur en dekking van de huidige laag op.
seo-title: bgColor
solution: Experience Manager
title: bgColor
topic: Dynamic Media Image Serving - Image Rendering API
uuid: bcbd368f-d200-4b1f-8e9f-bf4d88f14b72
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# bgColor{#bgcolor}

Achtergrondkleur laag. Hiermee geeft u de achtergrondkleur en dekking van de huidige laag op.

`bgColor= *`kleur`*`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> kleur</span></span> </p> </td> 
  <td class="stentry"> <p>Grijswaarde, RGB- of CMYK-kleurwaarde, met of zonder alfa. </p></td> 
 </tr> 
</table>

Transparante en semi-dekkende gebieden binnen het selectiekader van de laag worden gevuld met de opgegeven kleur* nadat* `opac=`, `rotate=` en `extend=` zijn toegepast.

## Eigenschappen {#section-19dfc13e997f4a33889a1df1e4ad50b9}

Laagkenmerk. Wordt toegepast op de huidige laag of op laag 0 als `layer=comp`. Genegeerd door effectlagen.

*`color`* wordt aangenomen dat deze voorkomt in de werkkleurruimte die overeenkomt met het pixeltype van  *`color`*. *`color`* nauwkeurig wordt omgezet als de uiteindelijke laagafbeelding een ander pixeltype heeft.

## Standaard {#section-30cd43f922c04ed9b75875ff7f20c88f}

0,0,0,0 (volledig transparant).

## Voorbeeld {#section-6e14fcf1d31e432dbdb56b9320904453}

Zie [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423).

## Zie ook {#section-64b3f153c6d94ab58f46e77324697818}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),  [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423),  [blendMode=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172),  [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)  [rotate=,bgc=, Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
