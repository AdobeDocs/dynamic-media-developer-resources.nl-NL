---
description: Afdrukresolutie. Hiermee overschrijft u de waarde voor de afdrukresolutie die is ingesloten in de reactieafbeelding.
seo-description: Afdrukresolutie. Hiermee overschrijft u de waarde voor de afdrukresolutie die is ingesloten in de reactieafbeelding.
seo-title: printRes
solution: Experience Manager
title: printRes
topic: Scene7 Image Serving - Image Rendering API
uuid: 1a62611a-b3b9-4f20-834f-e34e75d33ddd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# printRes{#printres}

Afdrukresolutie. Hiermee overschrijft u de waarde voor de afdrukresolutie die is ingesloten in de reactieafbeelding.

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Afdrukresolutie (dpi). </p></td> 
 </tr> 
</table>

De afdrukresolutie wordt meestal gedefinieerd door `catalog::PrintResolution` in het geval van een catalogusitem, anders door de waarde voor de afdrukresolutie die is ingesloten in de bronafbeelding. In het geval van een sjabloon of een samengestelde afbeelding met lagen is de standaardafdrukresolutie die is ingesloten in het reactiebestand de afdrukresolutie van de laagafbeelding met het laagste laagnummer.

Als u de afdrukresolutie instelt, verandert de pixelgrootte van de antwoordafbeelding niet.

## Eigenschappen {#section-03c7910ebe234804a319e5d0d8ef3a74}

Request-kenmerk. Is van toepassing ongeacht de huidige laaginstelling.

## Standaard {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` of de afdrukresolutie die is ingesloten in de bronafbeelding.

## Zie ook {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalogus::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
