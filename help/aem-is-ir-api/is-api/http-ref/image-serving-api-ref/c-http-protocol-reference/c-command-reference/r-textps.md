---
description: Laagtekst (compatibel met Adobe Photoshop). Geeft de teksthoofdtekst voor een tekstlaag aan.
solution: Experience Manager
title: textPs
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# textPs{#textps}

Laagtekst (compatibel met Adobe Photoshop). Geeft de teksthoofdtekst voor een tekstlaag aan.

`textPs= *`string`*`

<table id="simpletable_4E2D08FD4EEC4EDC9EFE9F6F2E22DB0C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> string</span> </span> </p> </td> 
  <td class="stentry"> <p>RTF-tekenreeks (Rich-text-formatted). </p></td> 
 </tr> 
</table>

Alle besturingselementen voor lettertype-, lettertypekleur- en alineaopmaak worden bereikt met RTF-opdrachten.

Zie [Tekstopmaak](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c).

`textPs=` ondersteunt uitgebreide functies, zoals uitvulling, tekstdoorloop in niet-rechthoekige gebieden die zijn gedefinieerd met  `textFlowPath=` en/of  `textFlowXPath=`, en rendering van tekst langs willekeurige paden die zijn gedefinieerd met  `textPath=`.

## Eigenschappen {#section-a289dc26b6534b41998b1e241d5f2f92}

Laagkenmerk. Is van toepassing op `layer=0` als `layer=comp`. Enkel en alleen `src=` en `text=` in dezelfde laag. De laatste instantie van `text=`, `textPs=` en `src=` heeft voorrang en bepaalt of dit een afbeelding of een tekstlaag is. Genegeerd door effectlagen.

## Standaard {#section-11c2ae2c96d64a0a9c207252df663e4d}

Geen.

## Zie ook {#section-5c2b25767d2b47b5be817271ab12e13c}

[Tekstopmaak](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d),  [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowxpath.md#reference-c55d4e41a28f40aca6a24ca218c28542)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)  [textFlowXPath=,textPath=,textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)
