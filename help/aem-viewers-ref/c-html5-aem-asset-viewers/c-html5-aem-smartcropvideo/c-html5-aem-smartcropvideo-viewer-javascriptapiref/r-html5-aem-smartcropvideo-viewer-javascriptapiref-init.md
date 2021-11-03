---
description: JavaScript API-referentie voor SmartCrop Video Viewer.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: d46a9c8b-064a-4928-b30e-885b12d287ab
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# init{#init}

JavaScript API-referentie voor SmartCrop Video Viewer.

`init()`

Start de initialisatie van de SmartCrop Video-viewer. Tegen deze tijd moet het container-DOM-element worden gemaakt, zodat de viewercode het met zijn id kan vinden.

Als het containerelement bijvoorbeeld nog geen deel uitmaakt van de webpaginalay-out, kan het worden verborgen met `display:none` de stijl die aan het wordt toegewezen de kijker onderbreekt zijn initialisatieproces tot het ogenblik dat de Web-pagina het containerelement terug naar de lay-out brengt. Wanneer dit gebeurt, wordt het laden van de viewer automatisch hervat.

Roep deze methode slechts eenmaal aan tijdens de levenscyclus van de kijker; volgende aanroepen worden genegeerd.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Geen.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Een verwijzing naar de viewerinstantie.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
