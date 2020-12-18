---
description: Tekstpad. Geeft het pad aan dat moet worden gebruikt als basislijn voor de tekst die bij textPs= wordt geleverd.
seo-description: Tekstpad. Geeft het pad aan dat moet worden gebruikt als basislijn voor de tekst die bij textPs= wordt geleverd.
seo-title: textPath
solution: Experience Manager
title: textPath
topic: Scene7 Image Serving - Image Rendering API
uuid: a2f0047b-ad62-4605-a723-b43d53fbea56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---


# textPath{#textpath}

Tekstpad. Geeft het pad aan dat moet worden gebruikt als basislijn voor de tekst die bij textPs= wordt geleverd.

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Padgegevens. </p></td> 
 </tr> 
</table>

Zie [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) voor aanvullende informatie, inclusief een beschrijving van *`pathDefinition`*.

>[!NOTE]
>
>In tegenstelling tot `clipPath=` worden tekstpaden niet automatisch gesloten wanneer &#39;z&#39; of &#39;Z&#39; niet is opgegeven aan het einde van een subpad.

*`pathDefinition`* kunnen meerdere subpaden bevatten. Tekst wordt op de subpaden weergegeven in de opgegeven volgorde.

De RTF-opdrachten `\ql`, `\qc`, `\qr`, `\li` en `\ri` kunnen worden gebruikt om de weergegeven tekst langs het pad te plaatsen.

## Eigenschappen {#section-068137df436c46b9b55d271eb60e7285}

Kenmerk tekstlaag (alleen `textPs=`). Genegeerd door andere lagen. Is van toepassing op `layer=0` indien opgegeven voor `layer=comp`. Wordt genegeerd als `textPs=` aanwezig is.

Er wordt een fout geretourneerd als een laag zowel `textPath=` als `textFlowPath=` bevat.

## Standaard {#section-697b1f2cfc43498080a31327e6eb173d}

Geen, voor standaardtekstrendering.

## Zie ook {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [Text Layers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
