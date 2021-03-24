---
description: Omgekeerd pad voor laagclip. Hiermee geeft u een pad voor de uitsluitingsclip op voor de huidige laag. Alle delen van de laag die zich binnen het gebied bevinden dat wordt gedefinieerd door clipXPath=, worden transparant gerenderd.
solution: Experience Manager
title: clipXPath
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---


# clipXPath{#clipxpath}

Omgekeerd pad voor laagclip. Hiermee geeft u een pad voor de uitsluitingsclip op voor de huidige laag. Alle delen van de laag die zich binnen het gebied bevinden dat wordt gedefinieerd door clipXPath=, worden transparant gerenderd.

`clipXPath= *`pathDefinition`*`

`clipXPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Padgegevens. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span> </span> </p> </td> 
  <td class="stentry"> <p>Naam van pad dat is ingesloten in bronafbeelding van laag (alleen ASCII). </p></td> 
 </tr> 
</table>

Zie [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) voor extra informatie, met inbegrip van een beschrijving van `*`pathName`*` en `*`pathDefinition`*`.

## Eigenschappen {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Laagkenmerk. Wordt toegepast op de huidige laag of op de samengestelde afbeelding als `layer=comp`. Wordt genegeerd als `clipPath=` niet is opgegeven. Genegeerd door effectlagen.

## Standaard {#section-d1986aa31af14767aeb1b4a57add67f4}

Geen.

## Zie ook {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
