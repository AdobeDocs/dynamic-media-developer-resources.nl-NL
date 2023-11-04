---
title: UseLastModified
description: Schakel laatst gewijzigde reactiekoppen in. Schakelt het opnemen van de header met laatste wijziging in of uit in cacheable HTTP responses die worden gegenereerd door Afbeelding renderen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# UseLastModified{#uselastmodified}

Schakel laatst gewijzigde reactiekoppen in. Schakelt het opnemen van de header met laatste wijziging in of uit in cacheable HTTP responses die worden gegenereerd door Afbeelding renderen.

De server gebruikt de meest recente `vignette::TimeStamp` en `catalog::TimeStamp` De waarde van alle vignet- en materiaalcatalogi/catalogusrecords die bij een reactie zijn betrokken als de laatst gewijzigde headerwaarde.

Deze optie moet alleen worden ingeschakeld als een gedistribueerd cachenetwerk, zoals Akamai, wordt gebruikt dat geen ondersteuning biedt voor etagkoppen.

>[!NOTE]
>
>Voorzichtigheid moet worden betracht wanneer het gebruiken van Laatst-Gewijzigde kopballen in een lading-evenwichtig milieu dat veelvoudige het Serven/Renderen van Beeld gastheren omvat. Het in cache plaatsen van clients kan worden overgeslagen en het laden van de server kan toenemen als de servers om een of andere reden verschillende tijdstempels voor dezelfde catalogusvermeldingen hebben. Een dergelijke situatie kan zich als volgt voordoen:

* `catalog::TimeStamp`, `vignette::TimeStamp`, of `attribute::TimeStamp` niet is gedefinieerd, zodat de wijzigingstijd van de [!DNL catalog.ini] bestand wordt gebruikt als standaard voor `catalog::TimeStamp`.

* In plaats van de materiaalcatalogusbestanden te delen via een netwerkmontage, heeft elke server een eigen instantie van de catalogusbestanden op een lokaal bestandssysteem.
* Twee of meer instanties van hetzelfde [!DNL catalog.ini] bestanden hebben andere wijzigingsdatums voor het bestand, mogelijk veroorzaakt door het onjuist kopiëren van de bestanden.

## Eigenschappen {#section-453952244193452caccfaf7f601007c1}

Markering. 0 om uit te schakelen, 1 om Laatst gewijzigde HTTP-headers in te schakelen.

## Standaard {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Overgenomen van `default::UseLastModified` indien niet gedefinieerd of leeg.

## Zie ook {#section-1536715169da48b0aecc4ab7326c86db}

[catalogus::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignet::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
