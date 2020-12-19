---
description: Standaardtijdstempel voor aanpassing van afbeelding. Geeft een standaardwaarde voor de catalogus TimeStamp.
seo-description: Standaardtijdstempel voor aanpassing van afbeelding. Geeft een standaardwaarde voor de catalogus TimeStamp.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 0670e53a-ad7d-46cf-8e18-4c52a766df6f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---


# TimeStamp{#timestamp}

Standaardtijdstempel voor aanpassing van afbeelding. Geeft een standaardwaarde voor catalog::TimeStamp.

Indien niet opgegeven, gebruikt de server de wijzigingsdatum/-tijd van dit [!DNL *`catalog`*.ini]-bestand.

## Eigenschappen {#section-647066e62ce44a84b627fdd0b2f7cfec}

Datum-/tijdwaarde. Kan het gehele getal van milliseconden zijn dat is verstreken sinds middernacht, 1 januari 1970 UTC/GMT of een datum-/tijdtekenreekswaarde met een van de volgende notaties:

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* GMT  *`offset`*

*`hh`* ligt tussen 0 en 23.

*`zzz`* is een tijdzonecode van 3 of 4 tekens, zoals  `GMT` of  `PST`. De zomertijd moet in de tijdzonecode (bv. `PST` voor Pacific Standard Time, vs `PDT` voor Pacific Daylight Savings Time).

*`offset`* is een verschuiving van de tijdzone in uren of uren:minuten ten opzichte van GMT. `PDT` is bijvoorbeeld gelijk aan `GMT -7`.

Alle elementen van tekenreeksopgemaakte datum-/tijdwaarden moeten aanwezig zijn. Als de datum-/tijdwaarde niet correct is opgemaakt, wordt deze genegeerd en wordt in plaats daarvan de wijzigingstijd van het bestand [!DNL *`catalog`*.ini] gebruikt.

## Standaard {#section-ac465313c97943ed97d41ea852329177}

Als deze parameter leeg is of niet is gedefinieerd, gebruikt de server de wijzigingstijd van het bestand ` *`catalog`*.ini`.

## Zie ook {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) ,  [kenmerk::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [kenmerk::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
