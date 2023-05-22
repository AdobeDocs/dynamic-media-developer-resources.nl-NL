---
description: Client cache-TTL voor reacties buiten de afbeelding. Verstrekt het vervalinterval voor bepaalde niet-beeldreacties.
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# NonImgExpiration{#nonimgexpiration}

Client cache-TTL voor reacties buiten de afbeelding. Verstrekt het vervalinterval voor bepaalde niet-beeldreacties.

Verstrekt het afloopinterval voor bepaalde niet-beeldreacties, met inbegrip van die verzonden in antwoord op de volgende bevelen:

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## Eigenschappen {#section-d37e3113f4b1468b86b5a14e80d94c83}

Reëel getal, 0 of hoger. Aantal uren tot het verstrijken van de antwoordgegevens. Stel de waarde in op 0 om de antwoordafbeelding altijd onmiddellijk te laten verlopen. Hierdoor wordt het in cache plaatsen van clients voor standaardafbeeldingsreacties uitgeschakeld. Instellen op -1 om te markeren als *nooit verlopen*.

## Standaard {#section-96981360c0234b7f824d2ff7c25a7954}

Overgenomen van `default::NonImgExpiration` indien niet gedefinieerd of leeg.

TTL (Time-to-Live) is de duur voordat de cache vervalt. De standaard TTL is 6 minuten.

## Zie ook {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catalogus::Verlopen](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
