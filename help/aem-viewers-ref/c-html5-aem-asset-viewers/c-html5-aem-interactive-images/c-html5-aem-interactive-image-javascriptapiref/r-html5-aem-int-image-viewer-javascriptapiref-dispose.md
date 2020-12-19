---
description: JavaScript API-referentie voor Video Image Viewer.
seo-description: JavaScript API-referentie voor Video Image Viewer.
seo-title: weggooien
solution: Experience Manager
title: weggooien
topic: Dynamic media
uuid: d9698486-8ffd-4b12-844b-e80b929675ec
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# dispose{#dispose}

JavaScript API-referentie voor Video Image Viewer.

`dispose()`

Hiermee wordt deze viewerinstantie verwijderd door alle bronnen die door de viewerlogica worden gebruikt vrij te geven en alle binnenobjecten en componenten die door de viewer in runtime zijn gemaakt, te verwijderen.

De webpaginacode moet ook de viewerinstantievariabele verwijderen om de viewer volledig uit het webbrowsergeheugen te verwijderen.

Als de webpaginacode gebeurtenislisteners rechtstreeks heeft geregistreerd in Viewer SDK-componenten die worden gebruikt door de viewer of opgeslagen externe referenties naar dergelijke componenten, moeten deze listeners expliciet niet zijn geregistreerd door de webpaginacode en moeten deze externe componentverwijzingen worden verwijderd voordat `dispose()` wordt aangeroepen.

Open de viewer-API niet meer nadat `dispose()` is aangeroepen.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Geen.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

