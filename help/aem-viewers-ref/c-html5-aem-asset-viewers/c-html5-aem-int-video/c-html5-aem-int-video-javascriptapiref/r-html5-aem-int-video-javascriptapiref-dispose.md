---
title: weggooien
description: JavaScript API-referentie voor Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 55418b97-3d18-4c1d-b0e3-aefd71f46616
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# weggooien{#dispose}

JavaScript API-referentie voor Interactive Video Viewer.

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
