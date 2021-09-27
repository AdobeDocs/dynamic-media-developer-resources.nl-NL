---
title: Interactieve gegevensondersteuning
description: De Interactive Video Viewer ondersteunt het renderen van interactieve stalen op basis van interactieve gegevens die als configuratieparameter aan de viewer worden doorgegeven.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Interactieve gegevensondersteuning{#interactive-data-support}

De Interactive Video Viewer ondersteunt het renderen van interactieve stalen op basis van interactieve gegevens die als configuratieparameter aan de viewer worden doorgegeven.

Het momenteel zichtbare staal komt overeen met het videotijdgebied waaraan het is gekoppeld. Wanneer u op het interactieve staal klikt of erop tikt, wordt de desbetreffende handeling tijdens het ontwerpen geactiveerd.

Met interactief staal kunt u een QuickView activeren op de hostwebpagina door een JavaScript-callback te starten, of de gebruiker omleiden naar een externe webpagina.

## Over QuickView {#section-7990e44f641042d2a38ba20c9413b3f8}

Deze typen interactieve stalen moeten worden gemaakt met het actietype &quot;quickview&quot; in Adobe Experience Manager Assets - On-demand. Wanneer een gebruiker een dergelijk staal activeert, voert de viewer `quickViewActivate` JavaScript-callback uit en geeft deze de staalgegevens eraan door. Verwacht wordt dat de insluitende webpagina luistert naar deze callback en dat de pagina een eigen Quickview-implementatie opent wanneer deze wordt geactiveerd.

## Omleiden naar een externe webpagina {#section-32ebe3c3a7f74892a428c5d48801de4d}

Stalen die zijn geschreven voor het actietype &quot;quickview&quot; in Experience Manager Assets - op verzoek sturen de gebruiker om naar een externe URL. Afhankelijk van de instellingen op het moment van ontwerpen kan de URL worden geopend in een nieuw browsertabblad, in hetzelfde venster of in het benoemde browservenster.
