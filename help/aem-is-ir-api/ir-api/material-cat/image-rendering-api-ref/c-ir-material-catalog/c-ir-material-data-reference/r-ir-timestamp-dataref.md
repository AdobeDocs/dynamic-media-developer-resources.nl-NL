---
description: Tijdstempel voor bestandswijziging. Hiermee geeft u de datum/tijd op waarop de afbeeldings- en/of gegevensbestanden die bij deze catalogusrecord horen voor het laatst zijn gewijzigd.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---


# TimeStamp{#timestamp}

Tijdstempel voor bestandswijziging. Hiermee geeft u de datum/tijd op waarop de afbeeldings- en/of gegevensbestanden die bij deze catalogusrecord horen voor het laatst zijn gewijzigd.

Wanneer `attribute::UseLastModified` is ingesteld, wordt de meest recente van de waarden `catalog::TimeStamp` en `vignette::TimeStamp` van alle materialen en het vignet dat bij de aanvraag is betrokken, geretourneerd in de HTTP-reactie als een laatst gewijzigde header.

>[!NOTE]
>
>De werkelijke bestandstijden van de afbeelding of gegevensbestanden die aan deze catalogusrecord zijn gekoppeld, worden hiervoor nooit gebruikt.

`catalog::TimeStamp` wordt ook gebruikt voor cachevalidatie op basis van catalogi (zie  ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`).

## Eigenschappen {#section-42f09e375e72492b87a3a486da7df808}

Datum-/tijdwaarde in Java-indeling. Kan het gehele getal van milliseconden zijn dat is verstreken sinds middernacht, 1 januari 1970 UTC/GMT of een datum-/tijdtekenreekswaarde met een van de volgende notaties:

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* GMT  *[!DNL offset]*

* *[!DNL hh]* ligt tussen 0 en 23.
* *[!DNL zzz]* is een tijdzonecode van 3 of 4 tekens, zoals &#39;GMT&#39; of &#39;PST&#39;. De zomertijd moet in de tijdzonecode (bijvoorbeeld, &quot;PST&quot;voor de StandaardTijd van de Stille Oceaan, tegenover &quot;PDT&quot;voor de Besparing van het Daglicht van de Stille Oceaan) worden rekenschap gegeven.
* *[!DNL offset]* is een verschuiving van de tijdzone in uren of uren:minuten ten opzichte van GMT. &#39;PDT&#39; is bijvoorbeeld gelijk aan &#39;GMT -7&#39;.

Alle elementen van tekenreeksopgemaakte datum-/tijdwaarden moeten aanwezig zijn. Als de datum-/tijdwaarde niet correct is opgemaakt, wordt deze genegeerd en wordt in plaats daarvan de wijzigingstijd van het bestand *catalog*.ini gebruikt.

## Standaard {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` is het veld leeg of niet aanwezig.

## Zie ook {#section-876f1d1b50dc4501b605820015a29451}

[kenmerk::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ,  [kenmerk::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d),  [kenmerk::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4),  [vignet::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
