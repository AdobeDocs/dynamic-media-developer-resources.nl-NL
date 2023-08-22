---
title: textFlowPath
description: Tekststroomgebied. Geeft een of meer gebieden op waarin tekst die met textPs= is opgegeven, moet worden doorlopen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b5575d17-150b-421c-b298-077b577eb95c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# textFlowPath{#textflowpath}

Tekststroomgebied. Geeft een of meer gebieden op waarin tekst die met textPs= is opgegeven, moet worden doorlopen.

` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pathDefinition </span> </p> </td> 
  <td class="stentry"> <p>Padgegevens. </p> </td> 
 </tr> 
</table>

Zie [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) voor aanvullende informatie, waaronder een beschrijving van *`pathDefinition`*.

De opdrachten voor de RTF-marge `\margl`, `\margr`, `\margt`, en `\margb` worden genegeerd wanneer `textFlowPath=` aanwezig is. Als er geen paddefinitie is opgegeven, `textFlowPath=` wordt genegeerd.

## Eigenschappen {#section-b68dc887c6534ce8982cad740b3aeaa4}

Kenmerk tekstlaag ( `textPs=` alleen). Genegeerd door andere lagen. Van toepassing op `layer=0` indien gespecificeerd voor `layer=comp`.

## Standaard {#section-68c4559b9e8242059b82e5a39a455dfc}

Hetzelfde als de laagrechthoek; tekst vult de volledige laagrechthoek.

## Zie ook {#section-592b0039cf99471188db6a7df44b450a}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15), [Tekstlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
