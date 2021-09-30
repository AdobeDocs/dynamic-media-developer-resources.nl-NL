---
title: Ondersteuning voor hotspots
description: Ondersteuning voor hotspots
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Ondersteuning voor hotspots{#hotspot-support}

De viewer ondersteunt het renderen van hotspots boven op de hoofdweergave. De weergave van hotspots wordt bepaald door CSS, zoals beschreven in de sectie Hotspots.

Zie [Hotspots](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Hotspots kunnen een Quickview-functie activeren op de hostwebpagina door een JavaScript-callback te activeren of een gebruiker om te leiden naar een externe webpagina.

## Hotspots voor Snelle weergave {#section-cda48fc9730142d0bb3326bac7df3271}

Deze typen hotspots moeten worden ontworpen met het actietype &quot;QuickView&quot; in Dynamic Media, Adobe Experience Manager Assets - On-demand. Wanneer een gebruiker een dergelijke hotspot activeert, voert de viewer de JavaScript-callback `quickViewActivate` uit en geeft hij de hotspot-gegevens eraan door. Er wordt verwacht dat de ingesloten webpagina luistert naar deze callback. Wanneer de pagina wordt geactiveerd, wordt een eigen Quickview-implementatie geopend.

## Omleiden naar externe webpagina {#section-ef820c71251e4215800bb99c0c9ebe16}

Hotspots die zijn ontworpen voor het actietype &quot;Snelle weergave&quot; in Dynamic Media of Experience Manager Assets - Op aanvraag leidt de gebruiker om naar een externe URL. Afhankelijk van de instellingen die tijdens het ontwerpen zijn gemaakt, wordt de URL geopend in een nieuw browsertabblad, in hetzelfde venster of in het benoemde browservenster.
