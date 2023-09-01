---
title: TimeStamp
description: Standaardtijdstempel voor aanpassing van afbeelding. Dit levert een standaardwaarde voor de catalogus TimeStamp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---

# TimeStamp{#timestamp}

Standaardtijdstempel voor aanpassing van afbeelding. Geeft een standaardwaarde voor catalog::TimeStamp.

Indien niet opgegeven, gebruikt de server de wijzigingsdatum/-tijd van dit [!DNL *`catalog`*.ini] bestand.

## Eigenschappen {#section-647066e62ce44a84b627fdd0b2f7cfec}

Datum-/tijdwaarde. Dit kan het gehele getal van milliseconden zijn dat is verstreken sinds middernacht, 1 januari 1970 UTC/GMT of een datum-/tijdtekenreekswaarde met een van de volgende notaties:

De datum-/tijdwaarde *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss zzz`*

De datum-/tijdwaarde *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

De tijdwaarde *`hh`* ligt tussen 0 en 23.

De tijdwaarde *`zzz`* is een tijdzonecode van drie of vier tekens, zoals `GMT` of `PST`. De zomertijd moet in de tijdzonecode (bijvoorbeeld `PST` voor Pacific Standard Time, vs `PDT` voor Pacific Daylight Savings Time).

De tijdwaarde *`offset`* is een verschuiving van de tijdzone in uren of uren:minuten ten opzichte van GMT. Bijvoorbeeld: `PDT` is gelijk aan `GMT -7`.

Alle elementen van datum-/tijdwaarden met tekenreeksindeling moeten aanwezig zijn. Als de datum-/tijdwaarde niet correct is opgemaakt, wordt deze genegeerd en wordt de wijzigingstijd van de [!DNL *`catalog`*.ini] wordt in plaats daarvan gebruikt.

## Standaard {#section-ac465313c97943ed97d41ea852329177}

Als deze parameter leeg is of niet is gedefinieerd, gebruikt de server de wijzigingstijd van dit bestand `*`catalogus`*.ini` bestand.

## Zie ook {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalogus::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) , [kenmerk::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [kenmerk:CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
