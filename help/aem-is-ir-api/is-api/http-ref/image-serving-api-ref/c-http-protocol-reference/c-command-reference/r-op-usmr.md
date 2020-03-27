---
description: Onscherp masker. Onscherp maskeert de laag of de definitieve meningsafbeelding, na al het schrapen, als layer=comp.
seo-description: Onscherp masker. Onscherp maskeert de laag of de definitieve meningsafbeelding, na al het schrapen, als layer=comp.
seo-title: op_usmR
solution: Experience Manager
title: op_usmR
topic: Scene7 Image Serving - Image Rendering API
uuid: 98afd83c-097e-40b4-b0a6-647f70b95fae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_usmR{#op-usmr}

Onscherp masker. Onscherp maskeert de laag of de definitieve meningsafbeelding, na al het schrapen, als layer=comp.

De parameters worden op dezelfde manier toegepast, ongeacht of downsampling heeft plaatsgevonden.

`op_usmR= *``*[, *``*[, *``*[, *`hoeveelhedenRdoroldmonochroom`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> bedrag</span></span> </p></td> 
  <td class="stentry"> <p>Filter Sterkte-factor (reëel 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p></td> 
  <td class="stentry"> <p>De kernel-straal van de filter in pixel (echt 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> drempel</span></span> </p></td> 
  <td class="stentry"> <p>Filter drempelniveau (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monochroom</span></span> </p></td> 
  <td class="stentry"> <p>Stel de waarde in op 0 om deze op elke kleurcomponent afzonderlijk toe te passen of op 1 om alleen de helderheid (intensiteit) van de afbeelding toe te passen. </p> <p><span class="codeph"> monochroom <span class="varname"></span></span> wordt genegeerd voor grijswaardenafbeeldingen. </p> </td> 
 </tr> 
</table>

Het laagmasker of het samengestelde masker wordt ook verscherpt.

## Eigenschappen {#section-fb5311b34d164946b74dadb32359518a}

Kenmerk of weergavekenmerk van laag. Is van toepassing op de huidige laag of op de uiteindelijke weergaveafbeelding, indien van toepassing `layer=comp`. Effectlagen negeren deze.

## Standaard {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` voor geen onscherp maskerend effect.

## Zie ook {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
