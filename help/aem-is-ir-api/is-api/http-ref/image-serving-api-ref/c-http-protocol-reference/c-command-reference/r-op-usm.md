---
description: Onscherp masker. Onscherp maskeert de laag of de definitieve meningsafbeelding, na al het schrapen, als layer=comp.
solution: Experience Manager
title: op_usm
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: a83d6326-9029-4c5c-a069-92bc81120866
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# op_usm{#op-usm}

Onscherp masker. Onscherp maskeert de laag of de definitieve meningsafbeelding, na al het schrapen, als layer=comp.

De parameters worden verondersteld op het volledige resolutiebeeld van toepassing te zijn en worden geschraapt wanneer het verwerken van een gedownsampled beeld.

`op_usm= *``*[, *``*[, *``*[, *`hoeveelheid tradiusdoroldmonochroom`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> bedrag</span></span> </p></td> 
  <td class="stentry"> <p>Filter Sterkte-factor (reëel 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p></td> 
  <td class="stentry"> <p>De kernel-straal van de filter in pixel (echt 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> drempel</span></span> </p></td> 
  <td class="stentry"> <p>Filter drempelniveau (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monochroom</span></span> </p></td> 
  <td class="stentry"> <p>Stel de waarde in op 0 om deze op elke kleurcomponent afzonderlijk toe te passen of op 1 om alleen de helderheid (intensiteit) van de afbeelding toe te passen. </p> <p> <span class="codeph"><span class="varname"> </span></span> monochrome afbeeldingen worden genegeerd. </p></td> 
 </tr> 
</table>

Het laagmasker of het samengestelde masker wordt ook verscherpt.

## Eigenschappen {#section-fb5311b34d164946b74dadb32359518a}

Kenmerk of weergavekenmerk van laag. Wordt toegepast op de huidige laag of op de uiteindelijke afbeelding in de weergave als `layer=comp`. Genegeerd door effectlagen.

## Standaard {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` voor geen onscherp maskerend effect.

## Zie ook {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
