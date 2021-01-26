---
description: De intermediaire beeldgegevens die door genestelde/ingebedde het Dienende Beeld en het Teruggeven van het Beeld verzoeken kunnen worden geproduceerd in het voorgeheugen ondergebracht door cache=on in het genestelde/ingebedde verzoek te specificeren. Dit gegeven wordt opgeslagen in merkgebonden formaat in het geheime voorgeheugen van reactiegegevens.
seo-description: De intermediaire beeldgegevens die door genestelde/ingebedde het Dienende Beeld en het Teruggeven van het Beeld verzoeken kunnen worden geproduceerd in het voorgeheugen ondergebracht door cache=on in het genestelde/ingebedde verzoek te specificeren. Dit gegeven wordt opgeslagen in merkgebonden formaat in het geheime voorgeheugen van reactiegegevens.
seo-title: Extra gegevenscaches
solution: Experience Manager
title: Extra gegevenscaches
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 10ce998e-e300-4d24-9d92-a8693dade327
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# Extra gegevenscaches{#auxiliary-data-caches}

De intermediaire beeldgegevens die door genestelde/ingebedde het Dienende Beeld en het Teruggeven van het Beeld verzoeken kunnen worden geproduceerd in het voorgeheugen ondergebracht door cache=on in het genestelde/ingebedde verzoek te specificeren. Dit gegeven wordt opgeslagen in merkgebonden formaat in het geheime voorgeheugen van reactiegegevens.

Afbeeldingen die worden opgehaald van externe HTTP-servers, worden ook opgeslagen in de cache met responsgegevens. Dergelijke afbeeldingen worden automatisch gevalideerd met het hulpprogramma validate voordat de cachevermelding wordt gegenereerd.

De server van het Platform compileert de gegevens van de beeldcatalogus voor efficiënte toegang. Deze gegevens worden opgeslagen in `CS::CatalogCacheFolder`.
