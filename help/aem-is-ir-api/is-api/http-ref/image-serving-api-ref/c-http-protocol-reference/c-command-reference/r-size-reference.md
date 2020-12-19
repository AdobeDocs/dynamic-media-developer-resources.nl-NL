---
description: Laaggrootte. Geeft de grootte of maximale laaggrootte voor een laag op, voordat rotate=, perspective= en extend= worden toegepast op de laag.
seo-description: Laaggrootte. Geeft de grootte of maximale laaggrootte voor een laag op, voordat rotate=, perspective= en extend= worden toegepast op de laag.
seo-title: size
solution: Experience Manager
title: size
topic: Scene7 Image Serving - Image Rendering API
uuid: c9c13062-7974-4dd9-aff4-f9502bcf442e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---


# size{#size}

Laaggrootte. Geeft de grootte of maximale laaggrootte voor een laag op, voordat rotate=, perspective= en extend= worden toegepast op de laag.

` size= *``*, *`Breedte`*`

` sizeN= *``*, *`widthNheightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> breedte  </span>,  <span class="varname"> hoogte  </span> </span> </p> </td> 
  <td class="stentry"> <p>Beperking voor laaggrootte in pixels (int, int, 0 of hoger). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN  </span>,  <span class="varname"> heightN  </span> </span> </p> </td> 
  <td class="stentry"> <p>Beperking voor laaggrootte is genormaliseerd ten opzichte van de grootte 0 van de laag (reëel, reëel, 0.0...1.0). </p> </td> 
 </tr> 
</table>

Als size= is opgegeven voor een afbeeldingslaag, beperkt dit de breedte, hoogte of beide van de laagafbeelding. De afbeelding wordt geschaald tot maximaal `size=`. Als een genormaliseerde grootte wordt gespecificeerd, is het met betrekking tot de grootte van laag 0. Als zowel *`width`* als *`height`* worden gespecificeerd, wordt het bronbeeld geschraapt (nadat `crop=` wordt toegepast) zodat geen van beide afmeting de gespecificeerde grootte overschrijdt. De hoogte-breedteverhouding van de bronrechthoek blijft in alle gevallen behouden. Of *`width`* of *`height`* kan aan 0 worden geplaatst; in dit geval wordt de waarde door de server berekend op basis van de hoogte-breedteverhouding van de afbeelding.

Wanneer opgegeven voor een tekstlaag, geeft `size=` de grootte van het tekstvak aan. *`width`* is vereist;  *`height`* kan worden ingesteld op 0, in welk geval de hoogte van de opgemaakte tekst wordt gebruikt als de laaghoogte. De tekstlay-outengines voegen standaard regeleinden in zodat tekst altijd horizontaal in de beschikbare ruimte past. Als *`height`* wordt gespecificeerd, zullen de lijnen die niet in de beschikbare ruimte passen worden geknipt ( `text=`) of weggelaten ( `textPs=`). `text=` ondersteunt aanvullende montagemodi; Zie  `textAttr=` voor meer informatie.

Wanneer gespecificeerd voor een stevige kleurenlaag, `size=` bepaalt de nauwkeurige laaggrootte; beide waarden moeten worden opgegeven (tenzij een masker is opgegeven). Als `mask=` ook is opgegeven, wordt de grootte van de maskerafbeelding aangepast aan `size=`, net zoals bij het schalen van afbeeldingen in afbeeldingslagen.

## Eigenschappen {#section-5f254b66fcba49bcb63f9c9ea40b230c}

Laagkenmerk. Is op laag 0 van toepassing als `layer=comp`. `sizeN=` is niet toegestaan voor  `layer=0` of  `layer=comp`. `sizeN=` is toegestaan voor  `layer=0` en  `layer=comp` alleen in catalogusrecords die watermerkafbeeldingen definiëren. In dit geval definieert `sizeN` de schaling van de watermerkafbeelding ten opzichte van de samengestelde afbeelding waarop het watermerk wordt toegepast. Als `size=` wordt gespecificeerd, `res=` en `scale=` worden genegeerd voor deze laag. Genegeerd door effectlagen.

## Standaard {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`, de laaggrootte is onbeperkt. Voor afbeeldingslagen wordt de laaggrootte vervolgens bepaald op basis van de afbeeldingsgrootte van de laag nadat een bewerking `crop=`, `scale=` of `res=` is toegepast. Als `size=` niet is opgegeven voor tekstlagen, wordt de grootte van de laag automatisch aangepast aan de gerenderde tekst.

Voor effen kleurlagen is een volledig opgegeven `size=`, een `mask=` of `clipPath=` vereist.

## Voorbeeld {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

Zie [Voorbeeld A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Zie ook {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) ,  [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [Text Layers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
