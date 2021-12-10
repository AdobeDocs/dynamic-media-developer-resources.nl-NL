---
title: weggooien
description: JavaScript API-naslaggids voor Zoom Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: c796943e-8ea8-4a97-a1ff-09676204150a
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# weggooien{#dispose}

JavaScript API-naslaggids voor Zoom Viewer.

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
