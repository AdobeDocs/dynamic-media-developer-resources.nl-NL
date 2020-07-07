---
description: Schakel laatst gewijzigde reactiekoppen in. Schakelt het opnemen van de header met laatste wijziging in of uit in cacheable HTTP responses die worden gegenereerd door Afbeelding renderen.
seo-description: Schakel laatst gewijzigde reactiekoppen in. Schakelt het opnemen van de header met laatste wijziging in of uit in cacheable HTTP responses die worden gegenereerd door Afbeelding renderen.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: f2ce2e04-4133-40af-ac82-cae57b253fe9
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---


# UseLastModified{#uselastmodified}

Schakel laatst gewijzigde reactiekoppen in. Schakelt het opnemen van de header met laatste wijziging in of uit in cacheable HTTP responses die worden gegenereerd door Afbeelding renderen.

De server gebruikt de meest recente `vignette::TimeStamp` en `catalog::TimeStamp` waarde van alle vignet- en materiaalcatalogi/catalogusrecords die bij een reactie zijn betrokken als de laatst gewijzigde headerwaarde.

Deze optie moet alleen worden ingeschakeld als een gedistribueerd cachenetwerk, zoals Akamai, wordt gebruikt dat geen ondersteuning biedt voor etagkoppen.

>[!NOTE]
>
>Voorzichtigheid moet worden betracht wanneer het gebruiken van Laatst-Gewijzigde kopballen in een lading-evenwichtig milieu dat veelvoudige het Serven/Renderen van Beeld gastheren omvat. Het in cache plaatsen van clients kan worden overgeslagen en het laden van de server kan toenemen als de servers om een of andere reden verschillende tijdstempels voor dezelfde catalogusvermeldingen hebben. Een dergelijke situatie kan zich als volgt voordoen:

* Noch `catalog::TimeStamp`, `vignette::TimeStamp`noch `attribute::TimeStamp` wordt bepaald, zodat de wijzigingstijd van het [!DNL catalog.ini] dossier als gebrek voor `catalog::TimeStamp`wordt gebruikt.

* In plaats van de materiaalcatalogusbestanden via een netwerkmontage te delen, heeft elke server een eigen instantie van de catalogusbestanden op een lokaal bestandssysteem.
* Twee of meer instanties van hetzelfde [!DNL catalog.ini] bestand hebben verschillende wijzigingsdatums voor het bestand, mogelijk veroorzaakt door het onjuist kopiëren van de bestanden.

## Eigenschappen {#section-453952244193452caccfaf7f601007c1}

Markering. 0 om uit te schakelen, 1 om Laatst gewijzigde HTTP-headers in te schakelen.

## Standaard {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Overgenomen van `default::UseLastModified` indien niet gedefinieerd of indien leeg.

## Zie ook {#section-1536715169da48b0aecc4ab7326c86db}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignet::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
