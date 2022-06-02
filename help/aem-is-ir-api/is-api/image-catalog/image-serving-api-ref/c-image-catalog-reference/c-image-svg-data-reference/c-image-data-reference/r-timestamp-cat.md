---
description: TimeStamp
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5532b182-cc8c-4a51-844f-e70c758f80a1
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# TimeStamp{#timestamp}

Indien `attribute::UseLastModified` is ingesteld, wordt de `catalog::TimeStamp` Deze waarde wordt in de HTTP-reactie geretourneerd als een Laatst gewijzigde HTTP-header. De header Laatst gewijzigd wordt altijd geretourneerd voor statische inhoud, zelfs als `attribute::UseLastModified` is niet ingesteld.

Voor inhoud van afbeelding en SVG, `catalog::TimeStamp` wordt ook gebruikt voor op een catalogus gebaseerde cachevalidatie (zie [kenmerk:CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md).

## Eigenschappen {#section-2298a384b5cb43929542655c5a49beb2}

Datum-/tijdwaarde in Java-indeling. Kan het gehele getal van milliseconden zijn dat is verstreken sinds middernacht, 1 januari 1970 UTC/GMT of een datum-/tijdtekenreekswaarde met een van de volgende notaties:

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* ligt tussen 0 en 23.

*`zzz`* is een tijdzonecode van drie of vier tekens, zoals &#39;GMT&#39; of &#39;PST&#39;. Account voor zomertijd in de tijdzonecode. Bijvoorbeeld &#39;PST&#39; voor Pacific Standard Time, versus &#39;PDT&#39; voor Pacific Daylight Savings Time).

*`offset`* is een verschuiving van de tijdzone in uren of `hours:minutes`, ten opzichte van GMT. &#39;PDT&#39; is bijvoorbeeld gelijk aan &#39;GMT -7&#39;.

Alle elementen van tekenreeksopgemaakte datum-/tijdwaarden moeten aanwezig zijn. Als de datum-/tijdwaarde niet op de juiste wijze is opgemaakt, wordt deze genegeerd en wordt de wijzigingstijd van de `*`catalogus`*.ini` wordt gebruikt.

## Standaard {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` als het veld leeg is of niet aanwezig is.

## Zie ook {#section-c42a427aa4794c548408dc4de028d578}

[kenmerk::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [kenmerk::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [kenmerk:CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
