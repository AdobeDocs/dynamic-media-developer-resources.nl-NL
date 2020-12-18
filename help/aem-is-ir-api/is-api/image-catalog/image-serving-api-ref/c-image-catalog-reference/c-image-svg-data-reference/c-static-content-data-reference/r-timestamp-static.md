---
description: 'null'
seo-description: 'null'
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: fd60e5db-9219-41a8-947f-0d497b39e727
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---


# TimeStamp{#timestamp}

Wanneer `attribute::UseLastModified` is ingesteld, wordt de waarde `catalog::TimeStamp` in de HTTP-reactie geretourneerd als een Laatst gewijzigde HTTP-header. De header Laatst gewijzigd wordt altijd geretourneerd voor statische inhoud, zelfs als `attribute::UseLastModified` niet is ingesteld.

Voor afbeelding- en SVG-inhoud wordt `catalog::TimeStamp` ook gebruikt voor cachevalidatie op basis van catalogus (zie ` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)`).

## Eigenschappen {#section-2298a384b5cb43929542655c5a49beb2}

Datum-/tijdwaarde in Java-indeling. Kan het gehele getal van milliseconden zijn dat is verstreken sinds middernacht, 1 januari 1970 UTC/GMT of een datum-/tijdtekenreekswaarde met een van de volgende notaties:

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* *`zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* GMT  *`offset`*

*`hh`* ligt tussen 0 en 23.

*`zzz`* is een tijdzonecode van drie of vier tekens, zoals &#39;GMT&#39; of &#39;PST&#39;. Account voor zomertijd in de tijdzonecode. Bijvoorbeeld &#39;PST&#39; voor Pacific Standard Time, versus &#39;PDT&#39; voor Pacific Daylight Savings Time).

*`offset`* is een verschuiving van de tijdzone in uren of  `hours:minutes`, ten opzichte van GMT. &#39;PDT&#39; is bijvoorbeeld gelijk aan &#39;GMT -7&#39;.

Alle elementen van tekenreeksopgemaakte datum-/tijdwaarden moeten aanwezig zijn. Als de datum-/tijdwaarde niet correct is opgemaakt, wordt deze genegeerd en wordt in plaats daarvan de wijzigingstijd van het bestand ` *`catalog`*.ini` gebruikt.

## Standaard {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` als het veld leeg is of niet aanwezig is.

## Zie ook {#section-c42a427aa4794c548408dc4de028d578}

[kenmerk::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296),  [kenmerk::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [kenmerk::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
