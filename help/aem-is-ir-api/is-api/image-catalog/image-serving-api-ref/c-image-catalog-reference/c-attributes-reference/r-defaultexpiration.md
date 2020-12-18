---
description: Client cache TTL voor standaardreacties op afbeeldingen. Verstrekt het afloopinterval voor standaardbeeldreacties (reacties die een standaardbeeld terugkeren dat of defaultImage= of attribuut DefaultImage wordt gespecificeerd).
seo-description: Client cache TTL voor standaardreacties op afbeeldingen. Verstrekt het afloopinterval voor standaardbeeldreacties (reacties die een standaardbeeld terugkeren dat of defaultImage= of attribuut DefaultImage wordt gespecificeerd).
seo-title: DefaultExpiration
solution: Experience Manager
title: DefaultExpiration
topic: Scene7 Image Serving - Image Rendering API
uuid: 5266bff9-f20b-4b3b-9566-8a3f5ba0777a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---


# DefaultExpiration{#defaultexpiration}

Client cache TTL voor standaardreacties op afbeeldingen. Verstrekt het afloopinterval voor standaardbeeldreacties (reacties die een standaardbeeld terugkeren dat of defaultImage= of attribuut wordt gespecificeerd::DefaultImage).

Wordt alleen toegepast wanneer de standaardafbeelding niet is gekoppeld aan een catalogusrecord of wanneer de standaardrecord voor de afbeeldingscatalogus geen specifieke `catalog::Expiration`-waarde bevat.

## Eigenschappen {#section-e564512476604fd7b964f9f2903d6d33}

Reëel getal, 0 of hoger. Aantal uren tot het verstrijken van de antwoordgegevens. Stel de waarde in op 0 om de antwoordafbeelding altijd onmiddellijk te laten verlopen. Hierdoor wordt het in cache plaatsen van clients voor standaardafbeeldingsreacties uitgeschakeld. Stel in op `-1` om te markeren als `never expire`.

## Standaard {#section-131cd32c2e214391857dba5af321f8cd}

Overgenomen van `default::DefaultExpiration` indien niet gedefinieerd of indien leeg.

TTL (Time-to-Live) is de duur voordat de cache vervalt. De standaard TTL is 1 uur.

## Zie ook {#section-d8642c22e3d947129367dd76366963d6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
