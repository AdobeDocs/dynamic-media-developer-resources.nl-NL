---
description: Laaggrootte. Geeft de grootte of maximale laaggrootte voor een laag op, voordat rotate=, perspective= en extend= worden toegepast op de laag.
solution: Experience Manager
title: size
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# size{#size}

Laaggrootte. Geeft de grootte of maximale laaggrootte voor een laag op, voordat rotate=, perspective= en extend= worden toegepast op de laag.

` size= *`width`*, *`height`*`

` sizeN= *`widthN`*, *`heightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span>, <span class="varname"> height </span> </span> </p> </td> 
  <td class="stentry"> <p>Beperking voor laaggrootte in pixels (int, int, 0 of hoger). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN </span>, <span class="varname"> heightN </span> </span> </p> </td> 
  <td class="stentry"> <p>Beperking voor laaggrootte is genormaliseerd ten opzichte van de grootte 0 van de laag (reëel, reëel, 0.0...1.0). </p> </td> 
 </tr> 
</table>

Als size= is opgegeven voor een afbeeldingslaag, beperkt dit de breedte, hoogte of beide van de laagafbeelding. De afbeelding wordt geschaald tot maximaal `size=`. Als een genormaliseerde grootte wordt gespecificeerd, is het met betrekking tot de grootte van laag 0. Als beide *`width`* en *`height`* worden opgegeven, wordt de bronafbeelding geschaald (na `crop=` wordt toegepast), zodat geen van beide dimensies de opgegeven grootte overschrijdt. De hoogte-breedteverhouding van de bronrechthoek blijft in alle gevallen behouden. Willekeurig *`width`* of *`height`* kan worden ingesteld op 0; in dit geval wordt de waarde door de server berekend op basis van de hoogte-breedteverhouding van de afbeelding.

Wanneer opgegeven voor een tekstlaag, `size=` geeft de grootte van het tekstvak aan. *`width`* is vereist; *`height`* kan worden ingesteld op 0, in welk geval de hoogte van de opgemaakte tekst wordt gebruikt als de laaghoogte. De tekstlay-outengines voegen standaard regeleinden in zodat tekst altijd horizontaal in de beschikbare ruimte past. Indien *`height`* wordt opgegeven, lijnen die niet in de beschikbare ruimte passen, worden bijgesneden ( `text=`) of weggelaten ( `textPs=`). `text=` ondersteunt aanvullende montagemodi; verwijzen naar `textAttr=` voor meer informatie.

Indien opgegeven voor een effen kleurlaag, `size=` de exacte laaggrootte definieert; beide waarden moeten worden opgegeven (tenzij een masker is opgegeven). Indien `mask=` wordt ook opgegeven, wordt de grootte van de maskerafbeelding aangepast `size=` op dezelfde manier als afbeeldingen worden geschaald in afbeeldingslagen.

## Eigenschappen {#section-5f254b66fcba49bcb63f9c9ea40b230c}

Laagkenmerk. Is van toepassing op laag 0 als `layer=comp`. `sizeN=` is niet toegestaan voor `layer=0` of `layer=comp`. `sizeN=` is toegestaan voor `layer=0` en `layer=comp` alleen in catalogusrecords die watermerkafbeeldingen definiëren. In dit geval: `sizeN` definieert de schaling van de watermerkafbeelding ten opzichte van de samengestelde afbeelding waarop het watermerk wordt toegepast. Indien `size=` is gespecificeerd, `res=` en `scale=` worden genegeerd voor deze laag. Genegeerd door effectlagen.

## Standaard {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`, de laaggrootte is onbeperkt. Voor afbeeldingslagen wordt de laaggrootte vervolgens bepaald op basis van de grootte van de laagafbeelding na elke `crop=`, `scale=`, of `res=` bewerkingen zijn toegepast. Voor tekstlagen, indien `size=` niet is opgegeven, wordt de grootte van de laag automatisch aangepast aan de gerenderde tekst.

Voor effen kleurlagen is een volledig opgegeven kleur vereist `size=`, `mask=`, of `clipPath=`.

## Voorbeeld {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

Zie [Voorbeeld A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Zie ook {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) , [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [Tekstlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
