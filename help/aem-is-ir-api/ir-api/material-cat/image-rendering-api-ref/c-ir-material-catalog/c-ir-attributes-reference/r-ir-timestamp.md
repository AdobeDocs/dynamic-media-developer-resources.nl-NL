---
title: TimeStamp
description: Standaardtijdstempel voor aanpassing. Verstrekt een standaardwaarde voor catalogus TimeStamp en vignet TimeStamp. Als deze waarde niet wordt opgegeven, gebruikt de server de wijzigingsdatum/-tijd van dit bestand catalog.ini.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b6d8fa6-0ad9-4f72-8d6d-1427e5d59df3
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# TimeStamp{#timestamp}

Standaardtijdstempel voor aanpassing. Biedt een standaardwaarde voor `catalog::TimeStamp` en `vignette::TimeStamp`. Als deze waarde niet wordt opgegeven, gebruikt de server de wijzigingsdatum/-tijd van dit bestand catalog.ini.

## Eigenschappen {#section-910e2562b41c47b78ee6216deeabbbd5}

Datum-/tijdwaarde in Java™-indeling. Kan het gehele getal van milliseconden zijn dat is verstreken sinds middernacht, 1 januari 1970 UTC/GMT of een datum-/tijdtekenreekswaarde met een van de volgende notaties:

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

*[!DNL hh]* ligt tussen 0 en 23.

*[!DNL zzz]* is een tijdzonecode van drie of vier tekens, zoals &#39;GMT&#39; of &#39;PST&#39;. De zomertijd moet in de tijdzonecode (bijvoorbeeld, &quot;PST&quot;voor de StandaardTijd van de Stille Oceaan, tegenover &quot;PDT&quot;voor de Besparing van het Daglicht van de Stille Oceaan) worden rekenschap gegeven.

*[!DNL offset]* is een verschuiving van de tijdzone in uren of uren:minuten ten opzichte van GMT. &#39;PDT&#39; is bijvoorbeeld gelijk aan &#39;GMT -7&#39;.

Alle elementen van datum-/tijdwaarden met tekenreeksindeling moeten aanwezig zijn. Als de datum-/tijdwaarde niet correct is opgemaakt, wordt deze genegeerd en wordt de wijzigingstijd van de [!DNL *[!DNL catalog]*.ini] bestand wordt in plaats daarvan gebruikt.

## Standaard {#section-65fb29a9ea2044df8cb9fe295eb14872}

Als deze parameter leeg is of niet is gedefinieerd, gebruikt de server de wijzigingstijd van het bestand [!DNL *[!DNL catalog]*.ini]-bestand.

## Zie ook {#section-764188f9b1734ad1a6270f5fecd28532}

[catalogus::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignet::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1), [kenmerk::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [kenmerk:CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
