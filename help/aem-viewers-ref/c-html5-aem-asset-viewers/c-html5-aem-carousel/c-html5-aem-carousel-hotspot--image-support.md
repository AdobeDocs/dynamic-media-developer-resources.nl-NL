---
description: 'null'
seo-description: 'null'
seo-title: Ondersteuning voor hotspot en afbeeldingen met hyperlinks
solution: Experience Manager
title: Ondersteuning voor hotspot en afbeeldingen met hyperlinks
topic: Dynamic media
uuid: 839b6a7f-4f6f-43ad-8eb8-254959c7fbac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Ondersteuning voor hotspot en afbeeldingen met hyperlinks{#hotspot-and-image-maps-support}

De viewer ondersteunt het renderen van hotspot-pictogrammen en gebieden met afbeeldingen met hyperlinks boven op de hoofdweergave. De weergave van hotspots en -gebieden wordt bepaald door CSS, zoals wordt beschreven in de sectie Hotspots en afbeeldingen met hyperlinks aanpassen.

Zie [Hotspots en afbeeldingen met hyperlinks](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Hotspots en regio&#39;s kunnen een functie Snelle weergave activeren op de hostwebpagina door een JavaScript-callback te activeren of een gebruiker om te leiden naar een externe webpagina.

## Hotspots in Snelle weergave {#section-cda48fc9730142d0bb3326bac7df3271}

Deze typen hotspots of afbeeldingen met hyperlinks moeten worden ontworpen met het actietype Snelle weergave in Dynamische media van AEM. Wanneer een gebruiker een dergelijke hotspot of afbeelding met hyperlinks activeert, voert de viewer de JavaScript-callback uit en geeft deze de hotspot- of afbeeldingskaartgegevens door. `quickViewActivate` Er wordt verwacht dat de ingesloten webpagina luistert naar deze callback. Wanneer de pagina wordt geactiveerd, wordt een eigen Quick View-implementatie geopend.

## Omleiden naar externe webpagina {#section-ef820c71251e4215800bb99c0c9ebe16}

Hotspots of afbeeldingen met hyperlinks die zijn ontworpen voor het actietype &quot;Snelle weergave&quot; in dynamische media van AEM leiden de gebruiker om naar een externe URL. Afhankelijk van de instellingen die tijdens het ontwerpen zijn gemaakt, wordt de URL geopend in een nieuw browsertabblad, in hetzelfde venster of in het benoemde browservenster.
