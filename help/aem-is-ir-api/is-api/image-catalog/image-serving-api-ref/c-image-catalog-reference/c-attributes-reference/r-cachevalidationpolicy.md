---
description: Beleid voor validatie van servercache. Hiermee geeft u aan wanneer cachemaringangen op de server worden gevalideerd.
seo-description: Beleid voor validatie van servercache. Hiermee geeft u aan wanneer cachemaringangen op de server worden gevalideerd.
seo-title: CacheValidationPolicy
solution: Experience Manager
title: CacheValidationPolicy
topic: Scene7 Image Serving - Image Rendering API
uuid: 371dadbf-d58e-4214-8050-7e8907b436e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CacheValidationPolicy{#cachevalidationpolicy}

Beleid voor validatie van servercache. Hiermee geeft u aan wanneer cachemaringangen op de server worden gevalideerd.

Bij validatie op basis van vervaldatum worden bronafbeeldingen periodiek gecontroleerd of ze zijn gewijzigd. Bij validatie op basis van een catalogus worden bronafbeeldingen pas gecontroleerd nadat de `catalog::TimeStamp` waarde is gewijzigd.

Validatie op basis van catalogi wordt aanbevolen bij gebruik van afbeeldingscatalogi. Validatie op basis van verlopen moet worden gebruikt wanneer rechtstreeks naar afbeeldingen wordt verwezen, zonder dat een afbeeldingscatalogus wordt gebruikt.

## Eigenschappen {#section-650cbddd81a24c3b8b70479248a45dc9}

Enum. 0 om op vervaldatum gebaseerde validatie te selecteren, 1 om op catalogus gebaseerde cachevalidatie te selecteren.

## Standaard {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

Overgenomen van `default::CacheValidationPolicy` indien niet gedefinieerd of indien leeg.

## Zie ook {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalogus::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
