---
description: Standaardtijdstempel voor aanpassing. Verstrekt een standaardwaarde voor catalogus TimeStamp en vignet TimeStamp. Als deze waarde niet wordt opgegeven, gebruikt de server de wijzigingsdatum/-tijd van het bestand catalog.ini.
seo-description: Standaardtijdstempel voor aanpassing. Verstrekt een standaardwaarde voor catalogus TimeStamp en vignet TimeStamp. Als deze waarde niet wordt opgegeven, gebruikt de server de wijzigingsdatum/-tijd van het bestand catalog.ini.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 10ceb600-1ed9-46a1-ae07-889d601ac0f4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---


# TimeStamp{#timestamp}

Standaardtijdstempel voor aanpassing. Geeft een standaardwaarde voor catalog::TimeStamp en vignet::TimeStamp. Als deze waarde niet wordt opgegeven, gebruikt de server de wijzigingsdatum/-tijd van het bestand catalog.ini.

## Eigenschappen {#section-910e2562b41c47b78ee6216deeabbbd5}

Datum-/tijdwaarde in Java-indeling. Kan het gehele getal van milliseconden zijn dat is verstreken sinds middernacht, 1 januari 1970 UTC/GMT of een datum-/tijdtekenreekswaarde met een van de volgende notaties:

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* GMT  *[!DNL offset]*

*[!DNL hh]* ligt tussen 0 en 23.

*[!DNL zzz]* is een tijdzonecode van 3 of 4 tekens, zoals &#39;GMT&#39; of &#39;PST&#39;. De zomertijd moet in de tijdzonecode (bijvoorbeeld, &quot;PST&quot;voor de StandaardTijd van de Stille Oceaan, tegenover &quot;PDT&quot;voor de Besparing van het Daglicht van de Stille Oceaan) worden rekenschap gegeven.

*[!DNL offset]* is een verschuiving van de tijdzone in uren of uren:minuten ten opzichte van GMT. &#39;PDT&#39; is bijvoorbeeld gelijk aan &#39;GMT -7&#39;.

Alle elementen van tekenreeksopgemaakte datum-/tijdwaarden moeten aanwezig zijn. Als de datum-/tijdwaarde niet correct is opgemaakt, wordt deze genegeerd en wordt in plaats daarvan de wijzigingstijd van het bestand [!DNL *[!DNL catalog]*.ini] gebruikt.

## Standaard {#section-65fb29a9ea2044df8cb9fe295eb14872}

Als het bestand leeg is of niet is gedefinieerd, gebruikt de server de wijzigingstijd van dit bestand [!DNL *[!DNL catalog]*.ini].

## Zie ook {#section-764188f9b1734ad1a6270f5fecd28532}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [vignet::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1),  [kenmerk::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d),  [kenmerk::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
