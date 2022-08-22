---
title: Verlopen
description: De standaardtijd voor de clientcache om te live gaan.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# Verlopen{#expiration}

De standaardtijd voor de clientcache om te live gaan. Biedt een standaardvervalinterval voor het geval dat een bepaalde catalogusrecord geen geldige waarde bevat `catalog::Expiration` of `vignette::Expiration` waarde. Of als een vignetbestand of materiaalbestand rechtstreeks wordt benaderd in plaats van via een catalogusrecord.

## Eigenschappen {#section-8e2bade105ec4905ae5c4911f500279f}

Reëel nummer `0` of hoger. Aantal uren tot het verstrijken van de antwoordgegevens. Instellen op `0` om altijd het antwoordbeeld onmiddellijk te verlopen, dat effectief cliënt caching onbruikbaar maakt. Instellen op `-1` om te markeren als *nooit verlopen*.

## Standaard {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Overgenomen van `default::Expiration` indien niet gedefinieerd of leeg.

## Zie ook {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalogus::Verlopen](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) , [vignet::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
