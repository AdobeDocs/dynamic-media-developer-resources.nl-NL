---
description: De intermediaire beeldgegevens die door genestelde/ingebedde het Dienende Beeld en het Teruggeven van het Beeld verzoeken kunnen worden geproduceerd in het voorgeheugen ondergebracht door cache=on in het genestelde/ingebedde verzoek te specificeren. Dit gegeven wordt opgeslagen in merkgebonden formaat in het geheime voorgeheugen van reactiegegevens.
solution: Experience Manager
title: Extra gegevenscaches
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# Extra gegevenscaches{#auxiliary-data-caches}

De intermediaire beeldgegevens die door genestelde/ingebedde het Dienende Beeld en het Teruggeven van het Beeld verzoeken kunnen worden geproduceerd in het voorgeheugen ondergebracht door cache=on in het genestelde/ingebedde verzoek te specificeren. Dit gegeven wordt opgeslagen in merkgebonden formaat in het geheime voorgeheugen van reactiegegevens.

Afbeeldingen die worden opgehaald van externe HTTP-servers, worden ook opgeslagen in de cache met responsgegevens. Dergelijke afbeeldingen worden automatisch gevalideerd met het hulpprogramma validate voordat de cachevermelding wordt gegenereerd.

De server van het Platform compileert de gegevens van de beeldcatalogus voor efficiënte toegang. Deze gegevens worden opgeslagen in `CS::CatalogCacheFolder`.
