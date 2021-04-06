---
description: Ondersteuning voor hotspots
solution: Experience Manager
title: Ondersteuning voor hotspots
feature: Dynamic Media Classic,Viewers,SDK/API,Interactieve afbeeldingen
role: Ontwikkelaar,zakelijke praktiserer
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# Hotspot-ondersteuning{#hotspot-support}

De viewer ondersteunt het renderen van hotspots boven op de hoofdweergave. De weergave van hotspots wordt bepaald door CSS, zoals beschreven in de sectie Hotspots.

Zie [Hotspots](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Hotspots kunnen een functie Snelle weergave activeren op de hostwebpagina door een JavaScript-callback te activeren of een gebruiker om te leiden naar een externe webpagina.

## Hotspots in Snelle weergave {#section-cda48fc9730142d0bb3326bac7df3271}

Deze typen hotspots moeten worden ontworpen met het actietype &quot;Snelle weergave&quot; in Dynamic Media, AEM Assets - op aanvraag. Wanneer een gebruiker een dergelijke hotspot activeert, voert de viewer de JavaScript-callback `quickViewActivate` uit en geeft hij de hotspot-gegevens eraan door. Er wordt verwacht dat de ingesloten webpagina luistert naar deze callback. Wanneer de pagina wordt geactiveerd, wordt een eigen Quick View-implementatie geopend.

## Omleiden naar externe webpagina {#section-ef820c71251e4215800bb99c0c9ebe16}

Hotspots die zijn ontworpen voor het actietype &quot;Snelle weergave&quot; in Dynamic Media of AEM Assets - leiden de gebruiker op verzoek om naar een externe URL. Afhankelijk van de instellingen die tijdens het ontwerpen zijn gemaakt, wordt de URL geopend in een nieuw browsertabblad, in hetzelfde venster of in het benoemde browservenster.
