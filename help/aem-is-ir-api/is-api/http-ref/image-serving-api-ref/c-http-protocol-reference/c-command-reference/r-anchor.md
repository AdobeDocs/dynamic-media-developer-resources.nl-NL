---
description: Afbeeldingsanker. Definieert het ankerpunt van de rechthoek van de afbeelding, effen kleur of het tekstkader voordat transformaties worden toegepast (crop=, scale=, rotate=, flip=). Wordt ook gebruikt als rotatiecentrum voor rotate=.
seo-description: Afbeeldingsanker. Definieert het ankerpunt van de rechthoek van de afbeelding, effen kleur of het tekstkader voordat transformaties worden toegepast (crop=, scale=, rotate=, flip=). Wordt ook gebruikt als rotatiecentrum voor rotate=.
seo-title: anker
solution: Experience Manager
title: anker
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 3b174360-9bb7-4dc8-83be-6b8c4ea88cd4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---


# anker{#anchor}

Afbeeldingsanker. Definieert het ankerpunt van de rechthoek van de afbeelding, effen kleur of het tekstkader voordat transformaties worden toegepast (crop=, scale=, rotate=, flip=). Wordt ook gebruikt als rotatiecentrum voor rotate=.

`anchor= *`coord`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span> </span> </p> </td> 
  <td class="stentry"> <p>pixelverschuiving ten opzichte van de linkerbovenhoek van de bronafbeelding (int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>genormaliseerde verschuiving van het midden van de bronafbeelding (reëel, reëel) </p></td> 
 </tr> 
</table>

Het ankerpunt wordt getransformeerd met de afbeelding en wordt het oorsprongpunt van de laag (tenzij `origin=` ook wordt opgegeven, in welk geval `anchor=` alleen wordt gebruikt als rotatiepunt voor `rotate=`).

`anchorN=0,0` plaatst het afbeeldingsanker in het midden van de bronafbeelding. `anchorN=-0.5,-0.5` of  `anchor=0,0` bevindt zich in de linkerbovenhoek en  `anchorN=0.5,0.5` bevindt zich in de rechterbenedenhoek van de bronafbeelding.

## Eigenschappen {#section-f08942bc6aae46a8b5d341faaff80640}

Kenmerk bronafbeelding. Wordt toegepast op de huidige laag of op laag 0 als `layer=comp`.

## Standaard {#section-35d369fab1254f1a9b91684a6e169ad1}

Als `anchor=` niet is opgegeven, wordt catalog::Anker gebruikt. Als `catalog::Anchor` niet is gedefinieerd, wordt het midden van de afbeeldingsrechthoek gebruikt (hetzelfde als het opgeven van `anchorN=0,0`).

Tekstlagen met `textPs=` en lagen met `clipPath=` kunnen verschillende standaardankers hebben.

## Voorbeeld {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

Zie &quot;Voorbeeld C&quot; in [Sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Zie ook {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catalogus::Anker](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) ,  [oorsprong=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138),  [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096),  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [Tekstlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
