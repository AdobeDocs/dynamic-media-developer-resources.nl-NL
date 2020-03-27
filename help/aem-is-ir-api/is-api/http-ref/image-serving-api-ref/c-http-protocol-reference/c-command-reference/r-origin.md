---
description: Oorsprong laag.
seo-description: Oorsprong laag.
seo-title: oorsprong
solution: Experience Manager
title: oorsprong
topic: Scene7 Image Serving - Image Rendering API
uuid: a36fc0b6-7744-4c1c-b9f8-4aa31a886bff
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# oorsprong{#origin}

Oorsprong laag.

`origin= *`coord`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p></td> 
  <td class="stentry"> <p>Pixelverschuiving ten opzichte van de linkerbovenhoek van de laagrechthoek (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Genormaliseerde verschuiving vanaf het midden van de laagrect (echt, echt). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>De laagrect omvat altijd om het even welke wijziging door `extend=`.

Definieert het uitlijningspunt van de laagrechthoek, die wordt gebruikt om de laagrechthoek te plaatsen ten opzichte van laag 0 via `pos=`. `originN=0,0` Hiermee plaatst u de oorsprong van de laag in het midden van de laagrechthoek. `originN=-0.5,-0.5` en `origin=0,0` is de linkerbovenhoek en `originN=0.5,0.5` is de rechterbenedenhoek van de laagrechthoek.

## Eigenschappen {#section-60f639e36ada43d1abc6bfc100afc925}

Laagkenmerk. Is van toepassing op de huidige laag of op laag 0 als `layer=comp`. Niet beïnvloed door laagtransformaties ( `crop=`, `scale=`, `rotate=`, `flip=`) toegepast op de laagbron. Overschrijvingen `anchor=`. Genegeerd door effectlagen.

## Standaard {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

Als `origin=` dit niet het geval is, wordt de oorsprong van de laag bepaald door de laagtransformaties toe te passen op het afbeeldingsanker. Als het afbeeldingsanker niet bekend is, wordt het midden van de laagrechthoek ( `originN=0,0`) gebruikt.

## Voorbeeld {#section-13e38d6e17be4e6cbc6b27fbde63b291}

Zie voorbeeld A in [sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Zie ook {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
