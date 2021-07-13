---
description: De intermediaire beeldgegevens die door genestelde/ingebedde het Dienende Beeld en het Teruggeven van het Beeld verzoeken kunnen worden geproduceerd in het voorgeheugen ondergebracht door cache=on in het genestelde/ingebedde verzoek te specificeren. Dit gegeven wordt opgeslagen in merkgebonden formaat in het geheime voorgeheugen van reactiegegevens.
solution: Experience Manager
title: Extra gegevenscaches
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Extra gegevenscaches{#auxiliary-data-caches}

De intermediaire beeldgegevens die door genestelde/ingebedde het Dienende Beeld en het Teruggeven van het Beeld verzoeken kunnen worden geproduceerd in het voorgeheugen ondergebracht door cache=on in het genestelde/ingebedde verzoek te specificeren. Dit gegeven wordt opgeslagen in merkgebonden formaat in het geheime voorgeheugen van reactiegegevens.

Afbeeldingen die worden opgehaald van externe HTTP-servers, worden ook opgeslagen in de cache met responsgegevens. Dergelijke afbeeldingen worden automatisch gevalideerd met het hulpprogramma validate voordat de cachevermelding wordt gegenereerd.

De server van het Platform compileert de gegevens van de beeldcatalogus voor efficiënte toegang. Deze gegevens worden opgeslagen in `CS::CatalogCacheFolder`.
