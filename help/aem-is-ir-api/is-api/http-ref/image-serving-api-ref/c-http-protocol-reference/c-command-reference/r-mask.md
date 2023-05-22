---
description: Afbeeldingsmasker. Hiermee geeft u een aparte maskerafbeelding op die als een niet-gekoppeld masker moet worden gebruikt.
solution: Experience Manager
title: masker
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5785844b-945b-4dd0-ac59-efbf1360b7cd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# masker{#mask}

Afbeeldingsmasker. Hiermee geeft u een aparte maskerafbeelding op die als een niet-gekoppeld masker moet worden gebruikt.

`mask= *`object`*|{[is|ir]'{' *`nestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p></td> 
  <td class="stentry"> <p>Afbeeldingsobject dat moet worden gebruikt als afbeeldings- of laagmasker. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>Geneste beeldservers, afbeeldingen renderen of externe verzoeken. </p></td> 
 </tr> 
</table>

*`object`* Dit kan een catalogusitem of een afbeeldings-/SVG-bestand zijn. Kan worden opgegeven voor afbeeldingslagen en effen kleurlagen.

Indien *`object`* wordt omgezet in een afbeeldingscatalogusitem, `catalog::MaskPath` wordt gebruikt, of `catalog::MaskPath` is niet gedefinieerd, dan `catalog::Path` wordt gebruikt. Indien *`object`* wordt niet omgezet in een item in een catalogus. Het wordt dan geïnterpreteerd als een bestandspad.

Als de bronafbeelding een alfakanaal heeft, wordt deze altijd gebruikt. Anders wordt de afbeelding, indien nodig, omgezet in grijswaarden voordat deze als laagmasker wordt gebruikt.

Als een masker op een stevige kleurenlaag wordt vastgemaakt, kan het worden bebouwd en worden geschraapt gebruikend de zelfde regels die voor beelden in beeldlagen worden gebruikt. `size=`, `scale=`, of `res=` kan worden gebruikt om het masker te schalen.

Laagmaskers kunnen ook worden opgegeven in de vorm van een *`nestedRequest`*. Geneste of ingesloten aanvragen worden ingesloten door accolades. Een ingesloten aanvraag voor Beeldbewerking vooraf bevestigen met `is` en een ingesloten aanvraag voor het renderen van afbeeldingen met `ir`. Een verzoek aan een buitenlandse server wordt verondersteld als geen prefix wordt gespecificeerd. Zie [Nesten en insluiten aanvragen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) voor meer informatie.

## Eigenschappen {#section-a093043dc249423b8ae322cefb0d545d}

Kenmerk afbeelding of laag. Is van toepassing op laag 0 als `layer=comp`. Genegeerd door effectlagen.

*`object`* mag niet worden omgezet in een catalogusrecord die een `src=` of `mask=` opdracht in `catalog::Modifier`.

De `is` en `ir` voorvoegsels zijn niet hoofdlettergevoelig.

## Standaard {#section-10cf793c665f49deb1b248faa3b618a9}

Indien `mask=` niet expliciet wordt opgegeven en als de laagafbeelding aan een catalogusitem is gekoppeld, `catalog::MaskPath` wordt gebruikt. Anders wordt het alfakanaal van de laagafbeelding gebruikt, indien aanwezig. Als er geen alfakanaal is, heeft de laag geen masker en wordt de laagrechthoek volledig dekkend weergegeven.

## Voorbeeld {#section-1bbe623f7c744bdf97b596458d8e7ea3}

Gebruik verschillende afzonderlijke maskers om verschillende gebieden van een afbeelding kleur te geven. De ingekleurde, gemaskerde gebieden worden in lagen boven op de oorspronkelijke, ongewijzigde afbeelding geplaatst:

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## Zie ook {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) , [catalogus::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) , [Nesten en insluiten aanvragen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
