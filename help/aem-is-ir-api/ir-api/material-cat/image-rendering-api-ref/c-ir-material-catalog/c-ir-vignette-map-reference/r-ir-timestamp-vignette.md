---
description: Tijdstempel voor wijziging. Hiermee geeft u de datum/tijd op waarop dit vignet voor het laatst is gewijzigd.
seo-description: Tijdstempel voor wijziging. Hiermee geeft u de datum/tijd op waarop dit vignet voor het laatst is gewijzigd.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: d2649e86-8a6f-4f63-ab6a-8b2d8c03f8c0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TimeStamp{#timestamp}

Tijdstempel voor wijziging. Hiermee geeft u de datum/tijd op waarop dit vignet voor het laatst is gewijzigd.

Als `attribute::UseLastModified` wordt geplaatst, zijn de meest recente `vignette::TimeStamp` en de `catalog::TimeStamp`waarde van vignet en alle materialen betrokken bij het verzoek teruggekeerd in de reactie van HTTP als laatste-gewijzigde kopbal.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>De werkelijke bestandstijd van het vignetbestand wordt hiervoor nooit gebruikt.

`catalog::TimeStamp` wordt ook gebruikt voor cachevalidatie op basis van catalogi (zie ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`).

## Eigenschappen {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Datum-/tijdwaarde in Java-indeling. Kan het gehele getal van milliseconden zijn dat is verstreken sinds middernacht, 1 januari 1970 UTC/GMT of een datum-/tijdtekenreekswaarde met een van de volgende notaties:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]*GMT *[!DNL offset]*

* *[!DNL hh]* ligt tussen 0 en 23.
* *[!DNL zzz]* is een tijdzonecode van 3 of 4 tekens, zoals &#39;GMT&#39; of &#39;PST&#39;. De zomertijd moet in de tijdzonecode (bijvoorbeeld, &quot;PST&quot;voor de StandaardTijd van de Stille Oceaan, tegenover &quot;PDT&quot;voor de Besparing van het Daglicht van de Stille Oceaan) worden rekenschap gegeven.
* *[!DNL offset]* is een verschuiving van de tijdzone in uren of uren:minuten ten opzichte van GMT. &#39;PDT&#39; is bijvoorbeeld gelijk aan &#39;GMT -7&#39;.

Alle elementen van tekenreeksopgemaakte datum-/tijdwaarden moeten aanwezig zijn. Als de datum-/tijdwaarde niet correct is opgemaakt, wordt deze genegeerd en wordt in plaats daarvan de wijzigingstijd van het bestand [!DNL *[!DNL catalog]*.ini] gebruikt.

## Standaard {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` is het veld leeg of niet aanwezig.

## Zie ook {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[kenmerk::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [catalogus::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [kenmerk::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
