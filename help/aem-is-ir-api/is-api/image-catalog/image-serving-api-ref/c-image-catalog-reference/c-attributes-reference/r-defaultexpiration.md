---
description: Client cache TTL voor standaardreacties op afbeeldingen. Verstrekt het afloopinterval voor standaardbeeldreacties (reacties die een standaardbeeld terugkeren dat of defaultImage= of attribuut DefaultImage wordt gespecificeerd).
solution: Experience Manager
title: DefaultExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 99103681-c00c-4648-8dee-2314e7e614af
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# DefaultExpiration{#defaultexpiration}

Client cache TTL voor standaardreacties op afbeeldingen. Verstrekt het afloopinterval voor standaardbeeldreacties (reacties die een standaardbeeld terugkeren dat of defaultImage= of attribuut wordt gespecificeerd::DefaultImage).

Wordt alleen toegepast als de standaardafbeelding niet is gekoppeld aan een catalogusrecord of als de standaardafbeeldingscatalogusrecord geen specifieke afbeelding bevat `catalog::Expiration` waarde.

## Eigenschappen {#section-e564512476604fd7b964f9f2903d6d33}

Reëel getal, 0 of hoger. Aantal uren tot het verstrijken van de antwoordgegevens. Stel de waarde in op 0 om de antwoordafbeelding altijd onmiddellijk te laten verlopen. Hierdoor wordt het in cache plaatsen van clients voor standaardafbeeldingsreacties uitgeschakeld. Instellen op `-1` om te markeren als `never expire`.

## Standaard {#section-131cd32c2e214391857dba5af321f8cd}

Overgenomen van `default::DefaultExpiration` indien niet gedefinieerd of leeg.

TTL (Time-to-Live) is de duur voordat de cache vervalt. De standaard TTL is 1 uur.

## Zie ook {#section-d8642c22e3d947129367dd76366963d6}

[catalogus::Verlopen](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
