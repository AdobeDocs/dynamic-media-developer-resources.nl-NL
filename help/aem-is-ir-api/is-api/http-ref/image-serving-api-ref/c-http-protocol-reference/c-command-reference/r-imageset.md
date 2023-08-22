---
title: imageSet
description: Afbeeldingsset. Hiermee wordt een waarde voor de afbeeldingsset opgegeven die moet worden gebruikt bij het genereren van de reactie req=set.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 318c658d-7126-40f6-870b-11294a3f6f5f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# imageSet{#imageset}

Afbeeldingsset. Hiermee wordt een waarde voor de afbeeldingsset opgegeven die moet worden gebruikt bij het genereren van de reactie req=set.

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Tekenreeks voor afbeeldingsset. </p></td> 
 </tr> 
</table>

Om aan de waarde te ontsnappen en ervoor te zorgen dat om het even welke inbegrepen bepalingen niet als deel van het URL vraagkoord worden geïnterpreteerd, zou de volledige waarde in krullende steunen moeten worden ingesloten. Als de catalogusrecord wordt opgegeven in het netto pad, overschrijft deze wijzigingwaarde `catalog::ImageSet` uit het hoofdrecord. Voor een beschrijving van de geldige syntaxis van een afbeeldingsset raadpleegt u `catalog::ImageSet` documentatie.

## Eigenschappen {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

Request-kenmerk. Optioneel. Overschrijvingen `catalog::ImageSet` uit het hoofdrecord.

## Standaard {#section-e8622ff40408450fb79d028f8d37fa6b}

Geen.

## Voorbeeld {#section-68513d3c601f477399602a0741dab390}

Afbeeldingsset opgeven voor gebruik met `req=set` verzoek:

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## Zie ook {#section-7e0320b2e09d475897082711a8f023a9}

[catalogus::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) , [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Verzoeken voor mediaset](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
