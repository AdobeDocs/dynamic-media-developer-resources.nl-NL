---
title: weggooien
description: JavaScript API-referentie voor eCatalog Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fda6d50f-0e1b-436c-af2e-1ccc9cd51c39
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# weggooien{#dispose}

JavaScript API-referentie voor eCatalog Viewer.

[!DNL `dispose()`]

Hiermee wordt deze viewerinstantie verwijderd door alle bronnen die door de viewerlogica worden gebruikt vrij te geven en alle binnenobjecten en componenten die door de viewer in runtime zijn gemaakt, te verwijderen.

De code van de webpagina moet ook de instantievariabele van de viewer verwijderen om de viewer volledig uit het webbrowsergeheugen te verwijderen.

Als de webpaginacode gebeurtenislisteners rechtstreeks heeft geregistreerd in Viewer SDK-componenten die door de viewer worden gebruikt, of als externe referenties naar dergelijke componenten zijn opgeslagen, moeten deze listeners expliciet door de webpaginacode niet worden geregistreerd. En, moeten dergelijke externe componentenverwijzingen alvorens te roepen worden geschrapt [!DNL `dispose()`].

Geen toegang meer tot de viewer-API na [!DNL `dispose()`] wordt aangeroepen.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Geen.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
