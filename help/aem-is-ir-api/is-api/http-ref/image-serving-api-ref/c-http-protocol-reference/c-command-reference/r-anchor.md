---
title: anker
description: Afbeeldingsanker. Definieert het ankerpunt van de rechthoek van de afbeelding, effen kleur of het tekstkader voordat transformaties worden toegepast (crop=, scale=, rotate=, flip=). Wordt ook gebruikt als rotatiecentrum voor rotate=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f62ae048-0dcc-4e93-a9f1-2e4db6bef51f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# anker{#anchor}

Afbeeldingsanker. Definieert het ankerpunt van de rechthoek van de afbeelding, effen kleur of het tekstkader voordat transformaties worden toegepast (crop=, scale=, rotate=, flip=). Wordt ook gebruikt als rotatiecentrum voor rotate=.

`anchor= *`coord`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span> </span> </p> </td> 
  <td class="stentry"> <p>pixelverschuiving vanaf de linkerbovenhoek van de bronafbeelding (int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>genormaliseerde verschuiving van het midden van de bronafbeelding (reëel, reëel) </p></td> 
 </tr> 
</table>

Het ankerpunt wordt getransformeerd met de afbeelding en wordt het oorsprongpunt van de laag (tenzij `origin=` wordt ook gespecificeerd, in welk geval `anchor=` wordt alleen gebruikt als rotatiecentrum voor `rotate=`).

`anchorN=0,0` plaatst het afbeeldingsanker in het midden van de bronafbeelding. `anchorN=-0.5,-0.5` of `anchor=0,0` zich in de linkerbovenhoek bevindt, en `anchorN=0.5,0.5` bevindt zich in de rechterbenedenhoek van de bronafbeelding.

## Eigenschappen {#section-f08942bc6aae46a8b5d341faaff80640}

Kenmerk bronafbeelding. Is van toepassing op de huidige laag of op laag 0 als `layer=comp`.

## Standaard {#section-35d369fab1254f1a9b91684a6e169ad1}

Indien `anchor=` is niet opgegeven, catalogus::Anker wordt gebruikt. Indien `catalog::Anchor` niet is gedefinieerd, wordt het midden van de afbeeldingsrechthoek gebruikt (gelijk aan opgeven `anchorN=0,0`).

Tekstlagen die `textPs=` en lagen waarbij `clipPath=` kunnen verschillende standaardankers hebben.

## Voorbeeld {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

Zie &quot;Voorbeeld C&quot; in [Sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Zie ook {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catalogus::Anker](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [oorsprong=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [roteren=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [Tekstlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
