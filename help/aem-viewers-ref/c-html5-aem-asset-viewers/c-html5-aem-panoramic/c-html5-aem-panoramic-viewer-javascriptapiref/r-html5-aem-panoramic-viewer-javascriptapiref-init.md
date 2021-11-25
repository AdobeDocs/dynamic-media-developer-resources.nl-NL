---
title: init
description: JavaScript API-referentie voor Panoramische Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: cb543620-e774-407b-bf33-bfd2261511c4
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# init{#init}

JavaScript API-referentie voor Panoramische Viewer.

`init()`

Start de initialisatie van de Panoramische Viewer. Tegen deze tijd moet het container-DOM-element worden gemaakt, zodat de viewercode het met zijn id kan vinden.

Als het containerelement nog geen deel uitmaakt van de webpaginalay-out (bijvoorbeeld `display:none` stijl toegewezen), onderbreekt de viewer het initialisatieproces. Dit gebeurt totdat de webpagina het containerelement weer in de layout plaatst. Wanneer deze gebeurtenis plaatsvindt, wordt het laden van de viewer automatisch hervat.

Deze methode moet slechts eenmaal worden aangeroepen tijdens de levenscyclus van de viewer, volgende aanroepen worden genegeerd.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Geen.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Een verwijzing naar de viewerinstantie.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
