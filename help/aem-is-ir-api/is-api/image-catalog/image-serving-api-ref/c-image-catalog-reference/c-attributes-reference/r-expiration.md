---
description: De standaardtijd voor de clientcache om te live gaan. Biedt een standaardvervalinterval voor het geval een bepaalde catalogusrecord geen geldige waarde voor Verlopen catalogus bevat.
seo-description: De standaardtijd voor de clientcache om te live gaan. Biedt een standaardvervalinterval voor het geval een bepaalde catalogusrecord geen geldige waarde voor Verlopen catalogus bevat.
seo-title: Verlopen
solution: Experience Manager
title: Verlopen
topic: Scene7 Image Serving - Image Rendering API
uuid: 26b2abee-8bd1-4011-90ff-f5143826ac0d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Verlopen{#expiration}

De standaardtijd voor de clientcache om te live gaan. Biedt een standaardvervalinterval voor het geval dat een bepaalde catalogusrecord geen geldige catalogus bevat::Expiration value.

## Eigenschappen {#section-063be3b2f13a48a3a5ab8080718e9812}

Reëel getal, 0 of hoger. Aantal uren tot het verstrijken van de antwoordgegevens. Reeks aan 0 om altijd het antwoordbeeld onmiddellijk te verlopen, dat effectief cliënt caching onbruikbaar maakt. Ingesteld op -1 om te markeren als `never expire`.

## Standaard {#section-f55308b195c04083996f6717c8537634}

Overgenomen van `default::Expiration` indien niet gedefinieerd of indien leeg.

TTL (Time-to-Live) is de duur voordat de cache vervalt. De standaard TTL is 10 uren.

## Zie ook {#section-b2411d99ddb14115ad475d506efd8967}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
