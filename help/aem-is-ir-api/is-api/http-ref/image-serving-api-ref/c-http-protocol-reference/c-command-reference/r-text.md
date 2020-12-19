---
description: Laagtekst. Geeft tekst en opmaakinhoud voor een tekstlaag op.
seo-description: Laagtekst. Geeft tekst en opmaakinhoud voor een tekstlaag op.
seo-title: text
solution: Experience Manager
title: text
topic: Scene7 Image Serving - Image Rendering API
uuid: 5b4f9282-83a3-488d-b5d2-deb2c92de564
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---


# text{#text}

Laagtekst. Geeft tekst en opmaakinhoud voor een tekstlaag op.

` text= *`string`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> string  </span> </p> </td> 
  <td class="stentry"> <p>RTF-tekenreeks (Rich-text-formatted) of onbewerkte-text tekenreeks. </p> </td> 
 </tr> 
</table>

Alle besturingselementen voor lettertype-, lettertypekleur- en alineaopmaak worden bereikt met RTF-opdrachten. Raadpleeg [Tekstopmaak](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) voor meer informatie.

`text=` ondersteunt automatisch schalen van de tekst om de laagrechthoek te vullen die met is opgegeven  `size=`.

Zie [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d).

`text=` ondersteunt het automatisch aanpassen van de grootte van de tekstlaag aan de gerenderde tekst (wanneer  `size=` geen waarde is opgegeven of wanneer alleen de breedte is opgegeven). Let erop dat in dit geval slechts een van de RTF-uitlijningsopdrachten `\ql`, `\qr` en `\qc` kan worden toegepast. anders wordt een fout geretourneerd.

## Eigenschappen {#section-8c0f020094a44c6b858454ef91ab4edf}

Laagkenmerk. Is van toepassing op `layer=0` als `layer=comp`. wederzijds exclusief met `src=` en `textPs=` in dezelfde laag; de laatste instantie van `text=`, `textPs=` en `src=` heeft voorrang en bepaalt of dit een afbeelding of een tekstlaag is. Genegeerd door effectlagen.

## Standaard {#section-58958671e0ad479e8d5f6c1d41d7dc74}

Geen.

## Voorbeeld {#section-d011f765ec5c418d814a821019b0eef0}

Zie de voorbeelden in [Tekstopmaak](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) en [Voorbeeld A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Zie ook {#section-207b779ab67342a5acd343e6bcc749c4}

[Tekstopmaak](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c),  [Tekstpositionering](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d),  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
