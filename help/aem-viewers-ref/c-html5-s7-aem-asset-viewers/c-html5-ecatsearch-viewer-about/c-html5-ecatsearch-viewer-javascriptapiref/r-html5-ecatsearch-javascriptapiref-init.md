---
title: init
description: JavaScript API-referentie voor eCatalog Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4d71062c-fee7-4339-bd7f-1b7f778465c4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# init{#init}

JavaScript API-referentie voor eCatalog Viewer.

[!DNL `init()`]

Start de initialisatie van de eCatalog Viewer. Tegen deze tijd, moet het containerDOM element worden gecreeerd zodat de kijkerscode het door zijn identiteitskaart kan vinden.

Als het containerelement nog geen deel uitmaakt van de webpaginalay-out, kan het bijvoorbeeld worden verborgen met [!DNL `display:none`] stijl die eraan is toegewezen. De viewer schorst het initialisatieproces. Dit gebeurt totdat de webpagina het containerelement weer in de layout plaatst. Wanneer deze gebeurtenis plaatsvindt, wordt de viewer automatisch opnieuw geladen.

Roep deze methode slechts eenmaal aan tijdens de levenscyclus van de viewer; volgende aanroepen worden genegeerd.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Geen.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] Een verwijzing naar een viewerinstantie.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
