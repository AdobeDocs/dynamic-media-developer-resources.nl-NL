---
description: JavaScript API-referentie voor Inline Zoom Viewer.
seo-description: JavaScript API-referentie voor Inline Zoom Viewer.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic Media
uuid: a3bd0cd1-e4cb-4b09-a78f-0958b55a79e4
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# init{#init}

JavaScript API-referentie voor Inline Zoom Viewer.

`init()`

Start de initialisatie van de viewer, zodat de viewercode deze kan vinden met de id. Tegen deze tijd moet het containerDOM-element worden gemaakt.

Als het containerelement nog geen deel uitmaakt van de webpaginalay-out (het kan bijvoorbeeld worden verborgen met de eraan toegewezen stijl `display:none`), onderbreekt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer dit gebeurt, wordt het laden van de viewer automatisch hervat.

Roep deze methode slechts eenmaal aan tijdens de levenscyclus van de viewer; volgende aanroepen worden genegeerd.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Geen.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Een verwijzing naar de viewerinstantie.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

