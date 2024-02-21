---
title: Ondersteuning voor hotspot en afbeeldingen met hyperlinks
description: Ondersteuning voor hotspot en afbeeldingen met hyperlinks
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 8d5dbc2d2b5e228f8496fd71633bf1cb96218226
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Ondersteuning voor hotspot en afbeeldingen met hyperlinks{#hotspot-and-image-maps-support}

De viewer ondersteunt het renderen van hotspot-pictogrammen en gebieden met afbeeldingen met hyperlinks boven op de hoofdweergave. De weergave van hotspots en -gebieden wordt bepaald door CSS, zoals wordt beschreven in de sectie Hotspots en afbeeldingen met hyperlinks aanpassen.

Zie [Hotspots en afbeeldingen met hyperlinks](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Hotspots en regio&#39;s kunnen een functie van de Snelle weergave op de het ontvangen Web-pagina activeren door een callback JavaScript te teweegbrengen of een gebruiker aan een externe Web-pagina om te leiden.

## Hotspots voor Snelle weergave {#section-cda48fc9730142d0bb3326bac7df3271}

Deze typen hotspots of afbeeldingen met hyperlinks moeten worden ontworpen met het actietype &quot;QuickView&quot; in Dynamic Media, Adobe Experience Manager. Wanneer een gebruiker een dergelijke hotspot of afbeelding met hyperlinks activeert, voert de viewer de opdracht `quickViewActivate` JavaScript-callback en geeft de hotspot- of afbeeldingskaartgegevens eraan door. Er wordt verwacht dat de ingesloten webpagina luistert naar deze callback. Wanneer de pagina wordt geactiveerd, wordt een eigen Quickview-implementatie geopend.

## Omleiden naar externe webpagina {#section-ef820c71251e4215800bb99c0c9ebe16}

Hotspots of afbeeldingen met hyperlinks die zijn ontworpen voor het actietype &quot;QuickView&quot; in Dynamic Media of Experience Manager leiden de gebruiker om naar een externe URL. Afhankelijk van de instellingen die tijdens het ontwerpen zijn gemaakt, wordt de URL geopend in een nieuw browsertabblad, in hetzelfde venster of in het benoemde browservenster.
