---
title: init
description: JavaScript API-referentie voor de Spin Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 5217a02a-6092-4cb9-b4fb-f959cdc85a6e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# init{#init}

JavaScript API-referentie voor de Spin Viewer.

`init()`

Start de initialisatie van de Spin Viewer. Tegen deze tijd is de container `DOM` -element moet worden gemaakt, zodat de viewercode het met de id kan vinden.

Als het containerelement nog geen deel uitmaakt van de webpaginalay-out, kan het bijvoorbeeld worden verborgen met `display:none` style - de viewer onderbreekt het initialisatieproces. De bewerking wordt onderbroken tot het moment dat de webpagina het containerelement weer in de lay-out plaatst, waarna het laden van de viewer automatisch wordt hervat.

Roep deze methode slechts eenmaal aan tijdens de levenscyclus van de viewer; volgende aanroepen worden genegeerd.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Geen.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Een verwijzing naar de viewerinstantie.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
