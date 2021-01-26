---
description: Client cache-TTL voor reacties buiten de afbeelding. Verstrekt het vervalinterval voor bepaalde niet-beeldreacties.
seo-description: Client cache-TTL voor reacties buiten de afbeelding. Verstrekt het vervalinterval voor bepaalde niet-beeldreacties.
seo-title: NonImgExpiration
solution: Experience Manager
title: NonImgExpiration
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 19b37bd4-f7cf-4b5f-be1a-b2d9fda5b4b1
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '132'
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

Reëel getal, 0 of hoger. Aantal uren tot het verstrijken van de antwoordgegevens. Stel de waarde in op 0 om de antwoordafbeelding altijd onmiddellijk te laten verlopen. Hierdoor wordt het in cache plaatsen van clients voor standaardafbeeldingsreacties uitgeschakeld. Stel de waarde in op -1 om te markeren als *never expired*.

## Standaard {#section-96981360c0234b7f824d2ff7c25a7954}

Overgenomen van `default::NonImgExpiration` indien niet gedefinieerd of indien leeg.

TTL (Time-to-Live) is de duur voordat de cache vervalt. De standaard TTL is 6 minuten.

## Zie ook {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
