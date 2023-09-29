---
title: init
description: JavaScript API-referentie voor initialisatie van de Flyout-viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: e86f8c0f-c130-43c5-8c3a-07c6bc49e2f7
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# init{#init}

JavaScript API-referentie voor Flyout Viewer.

`init()`

Start de initialisatie van de Flyout Viewer. Tegen deze tijd moet het container-DOM-element worden gemaakt, zodat de viewercode het met zijn id kan vinden.

Als het containerelement bijvoorbeeld nog geen deel uitmaakt van de webpaginalay-out, kan het worden verborgen met `display:none` stijl die aan de viewer is toegewezen, onderbreekt het initialisatieproces. Dit gebeurt totdat de webpagina het containerelement weer in de layout plaatst. Wanneer dit gebeurt, wordt het laden van de viewer automatisch hervat.

Deze methode moet slechts eenmaal worden aangeroepen tijdens de levenscyclus van de viewer, waarna de aanroepen worden genegeerd.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Geen.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Een verwijzing naar de viewerinstantie.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
