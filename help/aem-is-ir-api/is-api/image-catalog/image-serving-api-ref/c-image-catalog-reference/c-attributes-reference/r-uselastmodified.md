---
description: Schakel laatst gewijzigde reactiekoppen in. Hiermee schakelt u het opnemen van de header met laatste wijziging in in cacheable HTTP-reacties die worden gegenereerd door Image Serving in of uit.
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# UseLastModified{#uselastmodified}

Schakel laatst gewijzigde reactiekoppen in. Hiermee schakelt u het opnemen van de header met laatste wijziging in in cacheable HTTP-reacties die worden gegenereerd door Image Serving in of uit.

De server gebruikt de meest recente `catalog::TimeStamp` De waarde van alle catalogi/catalogusrecords die bij een reactie zijn betrokken, als Laatst gewijzigd koptekstwaarde.

Deze optie moet alleen worden ingeschakeld als een gedistribueerd cachenetwerk of een ander cachesysteem wordt gebruikt dat geen ondersteuning biedt voor labelkoppen.

>[!NOTE]
>
>Voorzichtigheid moet worden betracht wanneer het gebruiken van Laatst-Gewijzigde kopballen in een lading-evenwichtig milieu dat veelvoudige gastheren van de Beelddienst impliceert. Het in cache plaatsen van clients kan worden overgeslagen en het laden van de server kan toenemen als de servers om een of andere reden verschillende tijdstempels voor dezelfde catalogusvermeldingen hebben. Een dergelijke situatie kan zich als volgt voordoen:
>
>* Geen `catalog::TimeStamp` noch `attribute::TimeStamp`, zodat de wijzigingstijd van de [!DNL catalog.ini] bestand wordt gebruikt als standaard voor `catalog::TimeStamp`.
>
>* In plaats van de bestanden met de afbeeldingscatalogus te delen via een netwerkmontage, heeft elke server een eigen instantie van de catalogusbestanden op een lokaal bestandssysteem.
>* Twee of meer instanties van hetzelfde [!DNL catalog.ini] bestanden hebben andere wijzigingsdatums voor het bestand, mogelijk veroorzaakt door het onjuist kopiëren van de bestanden.
>

## Eigenschappen {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Markering. 0 om uit te schakelen, 1 om Laatst gewijzigde HTTP-headers in te schakelen.

## Standaard {#section-4eb47aadab8b41609bef296a4115f9f4}

Overgenomen van `default::UseLastModified` indien niet gedefinieerd of leeg.

## Zie ook {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalogus::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
