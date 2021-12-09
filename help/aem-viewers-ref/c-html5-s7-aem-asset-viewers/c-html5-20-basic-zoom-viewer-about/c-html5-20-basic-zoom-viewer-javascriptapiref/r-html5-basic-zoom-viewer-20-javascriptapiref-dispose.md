---
title: weggooien
description: JavaScript API-referentie voor de Basic Zoom Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 49c353f7-deab-43a7-84dd-21fda7864574
source-git-commit: 61e3a1fd0e21d336eaf5232096f5b1b54f2a6353
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# weggooien{#dispose}

JavaScript API-referentie voor de Basic Zoom Viewer.

`dispose()`

Hiermee wordt deze viewerinstantie verwijderd door alle bronnen die door de viewerlogica worden gebruikt vrij te geven en alle binnenobjecten en componenten die door de viewer in runtime zijn gemaakt, te verwijderen.

De webpaginacode moet ook de viewerinstantievariabele verwijderen om de viewer volledig uit het webbrowsergeheugen te verwijderen.

Als de webpaginacode gebeurtenislisteners rechtstreeks heeft geregistreerd in Viewer SDK-componenten die door de viewer worden gebruikt - of externe referenties naar dergelijke componenten heeft opgeslagen - moeten deze listeners expliciet door de webpaginacode worden verwijderd. En, moeten dergelijke externe componentenverwijzingen alvorens te roepen worden geschrapt `dispose()`.

Geen toegang meer tot de viewer-API na `dispose()` wordt aangeroepen.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Geen.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
