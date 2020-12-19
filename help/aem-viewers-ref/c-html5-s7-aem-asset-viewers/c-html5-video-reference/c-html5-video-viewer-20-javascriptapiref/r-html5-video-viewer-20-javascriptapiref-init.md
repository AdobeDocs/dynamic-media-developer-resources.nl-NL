---
description: JavaScript API-referentie voor Video Viewer.
seo-description: JavaScript API-referentie voor Video Viewer.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: 2ee5bddc-957c-4813-9285-d64b9ac7d590
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# init{#init}

JavaScript API-referentie voor Video Viewer.

`init()`

Start de initialisatie van de Video Viewer. Tegen deze tijd moet het container-DOM-element worden gemaakt, zodat de viewercode het met zijn id kan vinden.

Als het containerelement bijvoorbeeld nog geen deel uitmaakt van de webpaginalay-out, kan het worden verborgen met de stijl `display:none` die eraan is toegewezen. De viewer onderbreekt het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer dit gebeurt, wordt het laden van de viewer automatisch hervat.

Roep deze methode slechts eenmaal aan tijdens de levenscyclus van de kijker; volgende aanroepen worden genegeerd.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Geen.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Een verwijzing naar de viewerinstantie.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

