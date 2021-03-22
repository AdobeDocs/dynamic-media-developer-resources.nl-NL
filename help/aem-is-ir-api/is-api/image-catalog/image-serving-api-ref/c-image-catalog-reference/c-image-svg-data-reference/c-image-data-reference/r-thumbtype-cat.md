---
description: Miniatuurtype. Beschrijft hoe een duimnagel voor dit beeld moet worden geproduceerd.
seo-description: Miniatuurtype. Beschrijft hoe een duimnagel voor dit beeld moet worden geproduceerd.
seo-title: ThumbType
solution: Experience Manager
title: ThumbType
uuid: b737b5a4-ad6d-4a9c-b48f-81cf170dd210
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---


# ThumbType{#thumbtype}

Miniatuurtype. Beschrijft hoe een duimnagel voor dit beeld moet worden geproduceerd.

De volgende miniatuurtypen worden ondersteund:

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Uitsnijden (1) </p></td> 
  <td class="stentry"> <p>Snijd de afbeelding uit naar de hoogte-breedteverhouding van de miniatuur. Tenzij de hoogte-breedteverhouding van de miniatuurrechthoek en de afbeelding exact gelijk zijn, wordt een deel van de afbeelding bijgesneden, zodat de volledige miniatuurrechthoek met afbeeldingsgegevens wordt gevuld. De uitsnijdrechthoek wordt in de afbeelding geplaatst met het kenmerk <span class="codeph">::ThumbHorizAlign</span> en <span class="codeph">::ThumbVertAlign</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Passend (2) </p></td> 
  <td class="stentry"> <p>Plaats de hele afbeelding in de miniatuurrechthoek. De afbeelding wordt in de miniatuurrechthoek geplaatst met het volgende <span class="codeph">-kenmerk::ThumbHorizAlign</span> en <span class="codeph">-kenmerk::ThumbVertAlign</span> en eventuele extra witruimte wordt gevuld met het volgende <span class="codeph">-kenmerk::ThumbBkgColor</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Structuur (3) </p></td> 
  <td class="stentry"> <p>Snijd de afbeelding uit op basis van resolutie. De afbeelding wordt geschaald naar de verhouding van de catalogus <span class="codeph">::ThumbRes</span> tot <span class="codeph">::Resolution</span>. Als de resulterende afbeelding groter is dan de miniatuur, wordt deze bijgesneden om passend te maken. Als de geschaalde afbeelding kleiner is dan de miniatuur, wordt het resterende gebied gevuld met het kenmerk <span class="codeph">::ThumbBkgColor</span>. <span class="codeph"> kenmerk::</span> ThumbHorizAlignand- <span class="codeph"> kenmerk::</span> ThumbVertAlignment wordt gebruikt om de positie van de uitsnijdrechthoek binnen een grotere afbeelding of positie van een kleinere afbeelding binnen de miniatuur te bepalen. </p></td> 
 </tr> 
</table>

Clients vragen om afbeeldingsminiaturen met `req=tmb` verzoeken.

## Eigenschappen {#section-c58a8e67c2134ca3a0edd21b20dd3052}

Enum Value. Geldige waarden zijn 1, 2 of 3, die overeenkomen met respectievelijk de typen Uitsnijden, Passend en Structuur.

## Standaard {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` wordt gebruikt als het veld niet aanwezig is, als de waarde 0 is of als het veld leeg is.

## Zie ook {#section-fc1a79d3e6274b4381a17da159649a07}

[kenmerk::ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) ,  [kenmerk::ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e),  [kenmerk::ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691),  [kenmerk::ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f),  [catalogus::ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69),  [ ](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)  [ ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)  [catalogus:Resolutionreq=tmb, Thumes Schalen](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
