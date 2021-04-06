---
description: De Interactive Video Viewer ondersteunt het renderen van interactieve stalen op basis van interactieve gegevens die als configuratieparameter aan de viewer worden doorgegeven.
solution: Experience Manager
title: Interactieve gegevensondersteuning
feature: Dynamic Media Classic,Viewers,SDK/API,Interactieve video's
role: Ontwikkelaar,zakelijke praktiserer
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Interactieve gegevensondersteuning{#interactive-data-support}

De Interactive Video Viewer ondersteunt het renderen van interactieve stalen op basis van interactieve gegevens die als configuratieparameter aan de viewer worden doorgegeven.

Het momenteel zichtbare staal komt overeen met het videotijdgebied waaraan het is gekoppeld. Wanneer u op het interactieve staal klikt of erop tikt, wordt de desbetreffende handeling tijdens het ontwerpen geactiveerd.

Met interactief staal kunt u een Snelle weergave op de hostwebpagina activeren door een JavaScript-callback te activeren, of de gebruiker omleiden naar een externe webpagina.

## Info Snelle weergave {#section-7990e44f641042d2a38ba20c9413b3f8}

Deze typen interactieve stalen moeten worden gemaakt met het actietype &quot;quickview&quot; in AEM Assets, op aanvraag. Wanneer een gebruiker een dergelijk staal activeert, voert de viewer `quickViewActivate` JavaScript-callback uit en geeft deze de staalgegevens eraan door. Verwacht wordt dat de insluitingswebpagina luistert naar deze callback en dat de pagina een eigen Quick View-implementatie opent wanneer deze wordt geactiveerd.

## Omleiden naar een externe webpagina {#section-32ebe3c3a7f74892a428c5d48801de4d}

Stalen die zijn geschreven voor het actietype &quot;quickview&quot; in AEM Assets - leiden de gebruiker op verzoek om naar een externe URL. Afhankelijk van de instellingen op het moment van ontwerpen kan de URL worden geopend in een nieuw browsertabblad, in hetzelfde venster of in het benoemde browservenster.
