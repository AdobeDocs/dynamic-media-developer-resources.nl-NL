---
description: JavaScript API-referentie voor SmartCrop Video Viewer.
solution: Experience Manager
title: weggooien
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: c4bcccdc-6f23-4213-a1d1-03c5c62ba484
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# weggooien{#dispose}

JavaScript API-referentie voor SmartCrop Video Viewer.

`dispose()`

Hiermee wordt deze viewerinstantie verwijderd door alle bronnen die door de viewerlogica worden gebruikt vrij te geven en alle binnenobjecten en componenten die door de viewer in runtime zijn gemaakt, te verwijderen.

De webpaginacode moet ook de viewerinstantievariabele verwijderen om de viewer volledig uit het webbrowsergeheugen te verwijderen.

Als de webpaginacode gebeurtenislisteners rechtstreeks heeft geregistreerd in Viewer SDK-componenten die door de viewer worden gebruikt of externe referenties naar dergelijke componenten zijn opgeslagen, moet de webpaginacode deze listeners expliciet niet registreren en moeten deze externe componentverwijzingen worden verwijderd voordat deze worden aangeroepen `dispose()`.

Geen toegang meer tot de viewer-API na `dispose()` wordt aangeroepen.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Geen.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
