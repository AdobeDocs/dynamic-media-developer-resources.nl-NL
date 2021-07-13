---
description: Materiaalresolutie. Hiermee bepaalt u de resolutie van de herhaalbare structuur- of decale afbeelding.
solution: Experience Manager
title: res
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: f207355d-5819-47fc-bda5-27a411449569
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---

# res{#res}

Materiaalresolutie. Hiermee bepaalt u de resolutie van de herhaalbare structuur- of decale afbeelding.

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Resolutie; materiaalresolutie-eenheden (doorgaans pixels per inch) (reëel). </p> </td> 
 </tr> 
</table>

In het geval van een decal material heeft `size=` voorrang als zowel `size=` als `res=` worden gespecificeerd.

## Eigenschappen {#section-6a458ddc202f46e0b668c9f040a65cef}

Materiaalkenmerk. Genegeerd door effen kleurmaterialen. Alleen door materiaal voor de bekleding van de behuizing en vensterbekleding als ook een structuur wordt gebruikt.

## Standaard {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`, als het materiaal op een catalogusitem is gebaseerd, anders  `attribute::Resolution`indien  `res= is` niet opgegeven of ingesteld op een waarde kleiner dan of gelijk aan 0.

## Zie ook {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[Materiële resolutie](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b),  [size=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988),  [catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7),  [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
