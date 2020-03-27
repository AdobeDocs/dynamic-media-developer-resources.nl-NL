---
description: JavaScript API-referentie voor Flyout Viewer.
seo-description: JavaScript API-referentie voor Flyout Viewer.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: e5d990af-1c5a-4253-8ecd-b51119cee3a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# init{#init}

JavaScript API-referentie voor Flyout Viewer.

`init()`

Start de initialisatie van de Flyout Viewer. Tegen deze tijd moet het container-DOM-element worden gemaakt, zodat de viewercode het met zijn id kan vinden.

Als het containerelement nog geen deel uitmaakt van de webpaginalay-out (het kan bijvoorbeeld worden verborgen met de eraan toegewezen `display:none` stijl), onderbreekt de viewer het initialisatieproces totdat de webpagina het containerelement terugbrengt naar de lay-out. Wanneer dit gebeurt, wordt het laden van de viewer automatisch hervat.

Deze methode moet slechts eenmaal worden aangeroepen tijdens de levenscyclus van de viewer, waarna de aanroepen worden genegeerd.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Geen.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Een verwijzing naar de viewerinstantie.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

