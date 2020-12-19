---
description: Laagafbeelding.
seo-description: Laagafbeelding.
seo-title: src
solution: Experience Manager
title: src
topic: Scene7 Image Serving - Image Rendering API
uuid: b4396848-b992-4371-a8ae-4ff1781ae1be
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---


# src{#src}

Laagafbeelding.

` src= *``*|{[is|ir|fxg]'{' *`objectnestedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> object  </span> </p> </td> 
  <td class="stentry"> <p>Afbeeldingsobject. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest  </span> </p> </td> 
  <td class="stentry"> <p>Geneste beeldservers, afbeeldingen renderen of externe verzoeken. </p> </td> 
 </tr> 
</table>

## Beschrijving {#section-59ec6dc2afcb43efb34dbb0f7733543f}

Hiermee geeft u de bronafbeelding voor een afbeeldingslaag op.

*`object`* Dit kan een catalogus-item of een afbeeldings-/SVG-bestand zijn.

Zie [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

Geneste of ingesloten aanvragen worden ingesloten door accolades. Plaats een voorvoegsel voor een ingesloten aanvraag voor het renderen van afbeeldingen met `is`, een ingesloten aanvraag voor het renderen van afbeeldingen met `ir` en een aanvraag voor het renderen van FXG-afbeeldingen met `fxg`. Een verzoek aan een buitenlandse server wordt verondersteld als geen prefix wordt gespecificeerd.

Zie [Nesten en insluiten aanvragen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

>[!NOTE]
>
>FXG-rendering van afbeeldingen is alleen beschikbaar in de door Scene7 gehoste omgeving en vereist mogelijk extra licenties. Neem contact op met Scene7 Support voor meer informatie.

## Eigenschappen {#section-2c22bb89a35d470f833df8ba898efd93}

Laagkenmerk. Is van toepassing op `layer=0` als `layer=comp`. wederzijds exclusief met `text=` en `textPs=` in dezelfde laag; de laatste instantie van `text=`, `textPs=` of `src=` heeft voorrang en bepaalt of dit een afbeelding of een tekstlaag is. Genegeerd door effectlagen.

*`object`*kan niet aan een andere catalogusverslag oplossen die `src=` of `mask=` bevel in zijn `catalog::Modifier` omvat. (Gebruik nesten van aanvragen om een vergelijkbaar effect te bereiken.)

De voorvoegsels `is`, `ir` en `fxg` zijn hoofdlettergevoelig.

## Standaard {#section-a92f3882041b4d43ae2caf014647165f}

Voor laag 0 wordt het object uit de padcomponent van de URL gebruikt als `src=` niet is opgegeven. Geen standaardwaarde voor andere lagen.

## Zie ook {#section-e467e03330564796932ac081f1c9c1d0}

[catalogus::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [kenmerk::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f),  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)  [object, Templates,Request Nesting en Embedding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
