---
description: Afbeeldingsset. Hiermee wordt een waarde voor de afbeeldingsset opgegeven die moet worden gebruikt bij het genereren van de reactie req=set.
seo-description: Afbeeldingsset. Hiermee wordt een waarde voor de afbeeldingsset opgegeven die moet worden gebruikt bij het genereren van de reactie req=set.
seo-title: imageSet
solution: Experience Manager
title: imageSet
topic: Scene7 Image Serving - Image Rendering API
uuid: ecfb3905-e3ef-4ab8-a2c4-2c3f200e0f0f
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# imageSet{#imageset}

Afbeeldingsset. Hiermee wordt een waarde voor de afbeeldingsset opgegeven die moet worden gebruikt bij het genereren van de reactie req=set.

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Tekenreeks afbeeldingsset. </p></td> 
 </tr> 
</table>

Om aan de waarde te ontsnappen en ervoor te zorgen dat om het even welke inbegrepen bepalingen niet als deel van het URL vraagkoord worden geïnterpreteerd, zou de volledige waarde in krullende steunen moeten worden ingesloten. Als de catalogusrecord wordt opgegeven in het netto pad, overschrijft deze wijzigingwaarde `catalog::ImageSet` van de hoofdrecord. Raadpleeg de documentatie `catalog::ImageSet` voor een beschrijving van de geldige syntaxis van de afbeeldingsset.

## Eigenschappen {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

Request-kenmerk. Optioneel. Overschrijft `catalog::ImageSet` uit hoofdrecord.

## Standaard {#section-e8622ff40408450fb79d028f8d37fa6b}

Geen.

## Voorbeeld {#section-68513d3c601f477399602a0741dab390}

Geef een afbeeldingsset op voor gebruik met het `req=set`-verzoek:

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## Zie ook {#section-7e0320b2e09d475897082711a8f023a9}

[catalogus::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) ,  [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [Mediasetverzoeken](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
