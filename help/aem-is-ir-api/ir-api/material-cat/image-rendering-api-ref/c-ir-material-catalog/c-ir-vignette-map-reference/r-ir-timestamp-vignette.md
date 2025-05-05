---
title: TimeStamp
description: Tijdstempel voor wijziging. Hiermee geeft u de datum/tijd op waarop dit vignet voor het laatst is gewijzigd.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# TimeStamp{#timestamp}

Tijdstempel voor wijziging. Hiermee geeft u de datum/tijd op waarop dit vignet voor het laatst is gewijzigd.

Indien `attribute::UseLastModified` is ingesteld, de meest recente `vignette::TimeStamp` en `catalog::TimeStamp`De waarde van het vignet en alle materialen betrokken bij het verzoek wordt teruggekeerd in de reactie van HTTP als laatste-gewijzigde kopbal.

>[!NOTE]
>
>De werkelijke bestandstijd van het vignetbestand wordt hiervoor nooit gebruikt.

De `catalog::TimeStamp` wordt ook gebruikt voor cachevalidatie op basis van een catalogus. Zie [kenmerk:CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md).

## Eigenschappen {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Datum-/tijdwaarde in Java™-indeling. Dit kan het gehele getal van milliseconden zijn dat is verstreken sinds middernacht, 1 januari 1970 UTC/GMT of een datum-/tijdtekenreekswaarde met een van de volgende notaties:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]*&#x200B;GMT *[!DNL offset]*

* *[!DNL hh]* ligt tussen 0 en 23.
* *[!DNL zzz]* is een tijdzonecode van drie of vier tekens, zoals &#39;GMT&#39; of &#39;PST&#39;. De zomertijd moet in de tijdzonecode (bijvoorbeeld, &quot;PST&quot;voor de StandaardTijd van de Stille Oceaan, tegenover &quot;PDT&quot;voor de Besparing van het Daglicht van de Stille Oceaan) worden rekenschap gegeven.
* *[!DNL offset]* is een verschuiving van de tijdzone in uren of uren:minuten ten opzichte van GMT. &#39;PDT&#39; is bijvoorbeeld gelijk aan &#39;GMT -7&#39;.

Alle elementen van datum-/tijdwaarden met tekenreeksindeling moeten aanwezig zijn. Als de datum-/tijdwaarde niet correct is opgemaakt, wordt deze genegeerd en wordt de wijzigingstijd van de [!DNL *[!DNL catalog]*.ini] bestand wordt in plaats daarvan gebruikt.

## Standaard {#section-562c221d2e8b4a97ab5e9a3605f22140}

De `attribute::TimeStamp` Dit is het veld dat leeg is of niet aanwezig.

## Zie ook {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[kenmerk::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [catalogus::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [kenmerk::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
