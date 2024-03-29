---
description: Miniatuurtype. Beschrijft hoe een duimnagel voor dit beeld moet worden geproduceerd.
solution: Experience Manager
title: ThumbType
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a90b587d-6893-44e4-8dce-7676bc7eebe3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# ThumbType{#thumbtype}

Miniatuurtype. Beschrijft hoe een duimnagel voor dit beeld moet worden geproduceerd.

De volgende miniatuurtypen worden ondersteund:

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Uitsnijden (1) </p></td> 
  <td class="stentry"> <p>Snijd de afbeelding uit naar de hoogte-breedteverhouding van de miniatuur. Tenzij de hoogte-breedteverhouding van de miniatuurrechthoek en de afbeelding exact gelijk zijn, wordt een deel van de afbeelding bijgesneden, zodat de volledige miniatuurrechthoek met afbeeldingsgegevens wordt gevuld. De uitsnijdrechthoek wordt in de afbeelding geplaatst met <span class="codeph"> kenmerk:ThumbHorizAlign</span> en <span class="codeph"> kenmerk:ThumbVertAlign</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Passend (2) </p></td> 
  <td class="stentry"> <p>Plaats de hele afbeelding in de miniatuurrechthoek. De afbeelding wordt binnen de miniatuurrechthoek geplaatst met <span class="codeph"> kenmerk:ThumbHorizAlign</span> en <span class="codeph"> kenmerk:ThumbVertAlign</span>en eventuele extra spaties worden gevuld met <span class="codeph"> kenmerk:ThumbBkgColor</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Structuur (3) </p></td> 
  <td class="stentry"> <p>Snijd de afbeelding uit op basis van resolutie. De afbeelding wordt geschaald met de verhouding <span class="codeph"> catalogus::ThumbRes</span> tot <span class="codeph"> catalogus:Resolutie</span>. Als de resulterende afbeelding groter is dan de miniatuur, wordt deze bijgesneden en passend gemaakt. Als de geschaalde afbeelding kleiner is dan de miniatuur, wordt het resterende gebied gevuld met <span class="codeph"> kenmerk:ThumbBkgColor</span>. <span class="codeph"> kenmerk:ThumbHorizAlign</span> en <span class="codeph"> kenmerk:ThumbVertAlign</span> worden gebruikt om de positie van de uitsnijdrechthoek te bepalen binnen een grotere afbeelding of de positie van een kleinere afbeelding binnen de miniatuur. </p></td> 
 </tr> 
</table>

Clients vragen om afbeeldingsminiaturen met `req=tmb` verzoeken.

## Eigenschappen {#section-c58a8e67c2134ca3a0edd21b20dd3052}

Enum Value. Geldige waarden zijn 1, 2 of 3, die overeenkomen met respectievelijk de typen Uitsnijden, Passend en Structuur.

## Standaard {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` wordt gebruikt als het veld niet aanwezig is, als de waarde 0 is of als het veld leeg is.

## Zie ook {#section-fc1a79d3e6274b4381a17da159649a07}

[attribute::ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) , [kenmerk:ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e), [kenmerk:ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691), [kenmerk:ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f), [catalogus::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69), [catalogus:Resolutie](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1), [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Miniatuurschaal](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
