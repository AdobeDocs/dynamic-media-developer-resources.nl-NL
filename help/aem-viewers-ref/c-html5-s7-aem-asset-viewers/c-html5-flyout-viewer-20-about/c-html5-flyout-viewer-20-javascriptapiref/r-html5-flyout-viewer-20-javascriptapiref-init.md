---
description: JavaScript API-referentie voor Flyout Viewer.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---


# init{#init}

JavaScript API-referentie voor Flyout Viewer.

`init()`

Start de initialisatie van de Flyout Viewer. Tegen deze tijd moet het container-DOM-element worden gemaakt, zodat de viewercode het met zijn id kan vinden.

Als het containerelement nog geen deel uitmaakt van de webpaginalay-out (het kan bijvoorbeeld worden verborgen met de eraan toegewezen stijl `display:none`), onderbreekt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer dit gebeurt, wordt het laden van de viewer automatisch hervat.

Deze methode moet slechts eenmaal worden aangeroepen tijdens de levenscyclus van de viewer, waarna de aanroepen worden genegeerd.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Geen.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Een verwijzing naar de viewerinstantie.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

