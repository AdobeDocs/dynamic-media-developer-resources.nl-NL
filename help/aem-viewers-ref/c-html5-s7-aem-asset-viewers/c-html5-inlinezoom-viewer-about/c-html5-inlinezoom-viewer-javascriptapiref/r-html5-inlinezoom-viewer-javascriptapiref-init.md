---
title: init
description: JavaScript API-referentie voor Inline Zoom Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: c4419728-1e1a-4e11-88fe-24eb0c968c5c
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# init{#init}

JavaScript API-referentie voor Inline Zoom Viewer.

`init()`

Start de initialisatie van de viewer, zodat de viewercode deze kan vinden met de id. Tegen deze tijd moet het containerDOM-element worden gemaakt.

Als het containerelement nog geen deel uitmaakt van de webpaginalay-out, kan het bijvoorbeeld worden verborgen met `display:none` stijl die eraan is toegewezen - de viewer onderbreekt het initialisatieproces. Dit gebeurt totdat de webpagina het containerelement weer in de layout plaatst. Wanneer deze actie wordt uitgevoerd, wordt het laden van de viewer automatisch hervat.

Roep deze methode slechts eenmaal aan tijdens de levenscyclus van de viewer; volgende aanroepen worden genegeerd.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Geen.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Een verwijzing naar de viewerinstantie.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
