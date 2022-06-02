---
description: Tijdstempel voor bestandswijziging. Hiermee geeft u de datum/tijd op waarop de afbeeldings- en/of gegevensbestanden die bij deze catalogusrecord horen voor het laatst zijn gewijzigd.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# TimeStamp{#timestamp}

Tijdstempel voor bestandswijziging. Hiermee geeft u de datum/tijd op waarop de afbeeldings- en/of gegevensbestanden die bij deze catalogusrecord horen voor het laatst zijn gewijzigd.

Indien `attribute::UseLastModified` is ingesteld, de meest recente van de `catalog::TimeStamp` en `vignette::TimeStamp` De waarden van alle materialen en het vignet betrokken bij het verzoek zijn teruggekeerd in de reactie van HTTP als laatste-gewijzigde kopbal.

>[!NOTE]
>
>De werkelijke bestandstijden van de afbeelding of gegevensbestanden die aan deze catalogusrecord zijn gekoppeld, worden hiervoor nooit gebruikt.

`catalog::TimeStamp` wordt ook gebruikt voor op een catalogus gebaseerde cachevalidatie (zie [kenmerk:CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)).

## Eigenschappen {#section-42f09e375e72492b87a3a486da7df808}

Datum-/tijdwaarde in Java-indeling. Kan het gehele getal van milliseconden zijn dat is verstreken sinds middernacht, 1 januari 1970 UTC/GMT of een datum-/tijdtekenreekswaarde met een van de volgende notaties:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* ligt tussen 0 en 23.
* *[!DNL zzz]* is een tijdzonecode van 3 of 4 tekens, zoals &#39;GMT&#39; of &#39;PST&#39;. De zomertijd moet in de tijdzonecode (bijvoorbeeld, &quot;PST&quot;voor de StandaardTijd van de Stille Oceaan, tegenover &quot;PDT&quot;voor de Besparing van het Daglicht van de Stille Oceaan) worden rekenschap gegeven.
* *[!DNL offset]* is een verschuiving van de tijdzone in uren of uren:minuten ten opzichte van GMT. &#39;PDT&#39; is bijvoorbeeld gelijk aan &#39;GMT -7&#39;.

Alle elementen van tekenreeksopgemaakte datum-/tijdwaarden moeten aanwezig zijn. Als de datum-/tijdwaarde niet op de juiste wijze is opgemaakt, wordt deze genegeerd en wordt de wijzigingstijd van de *catalogus* Het .ini-bestand wordt in plaats daarvan gebruikt.

## Standaard {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` is het veld leeg of niet aanwezig.

## Zie ook {#section-876f1d1b50dc4501b605820015a29451}

[kenmerk::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [kenmerk::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [kenmerk:CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [vignet::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
