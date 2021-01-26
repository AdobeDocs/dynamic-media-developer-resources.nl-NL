---
description: JavaScript API-referentie voor eCatalog Viewer.
seo-description: JavaScript API-referentie voor eCatalog Viewer.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic Media
uuid: b01f1497-8bee-4e01-8f92-272b324cb2dd
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# init{#init}

JavaScript API-referentie voor eCatalog Viewer.

[!DNL `init()`]

Start de initialisatie van de eCatalog Viewer. Tegen deze tijd moet het DOM-element van de container worden gemaakt, zodat de viewercode het met zijn id kan vinden.

Als het containerelement nog geen deel uitmaakt van de webpaginalay-out (het kan bijvoorbeeld worden verborgen met de eraan toegewezen stijl [!DNL `display:none`]), onderbreekt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer dit gebeurt, wordt het laden van de viewer automatisch hervat.

Roep deze methode slechts eenmaal aan tijdens de levenscyclus van de viewer; volgende aanroepen worden genegeerd.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Geen.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] Een verwijzing naar een viewerinstantie.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

