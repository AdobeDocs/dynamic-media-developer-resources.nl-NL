---
description: De intermediaire beeldgegevens die door genestelde/ingebedde het Dienende Beeld en het Teruggeven van het Beeld verzoeken kunnen worden geproduceerd in het voorgeheugen ondergebracht door cache=on in het genestelde/ingebedde verzoek te specificeren. Dit gegeven wordt opgeslagen in merkgebonden formaat in het geheime voorgeheugen van reactiegegevens.
seo-description: De intermediaire beeldgegevens die door genestelde/ingebedde het Dienende Beeld en het Teruggeven van het Beeld verzoeken kunnen worden geproduceerd in het voorgeheugen ondergebracht door cache=on in het genestelde/ingebedde verzoek te specificeren. Dit gegeven wordt opgeslagen in merkgebonden formaat in het geheime voorgeheugen van reactiegegevens.
seo-title: Extra gegevenscaches
solution: Experience Manager
title: Extra gegevenscaches
uuid: 10ce998e-e300-4d24-9d92-a8693dade327
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder,praktijkgericht
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Extra gegevenscaches{#auxiliary-data-caches}

De intermediaire beeldgegevens die door genestelde/ingebedde het Dienende Beeld en het Teruggeven van het Beeld verzoeken kunnen worden geproduceerd in het voorgeheugen ondergebracht door cache=on in het genestelde/ingebedde verzoek te specificeren. Dit gegeven wordt opgeslagen in merkgebonden formaat in het geheime voorgeheugen van reactiegegevens.

Afbeeldingen die worden opgehaald van externe HTTP-servers, worden ook opgeslagen in de cache met responsgegevens. Dergelijke afbeeldingen worden automatisch gevalideerd met het hulpprogramma validate voordat de cachevermelding wordt gegenereerd.

De server van het Platform compileert de gegevens van de beeldcatalogus voor efficiënte toegang. Deze gegevens worden opgeslagen in `CS::CatalogCacheFolder`.
