---
description: Preload image is a static asset preview image which loads right after calling init() method and shows while Viewer SDK libraries, asset and preset information is downloaded. The purpose of the preload image is to visually improve viewer load time and present content to the user quickly.
seo-description: Preload image is a static asset preview image which loads right after calling init() method and shows while Viewer SDK libraries, asset and preset information is downloaded. The purpose of the preload image is to visually improve viewer load time and present content to the user quickly.
seo-title: Afbeelding vooraf laden
solution: Experience Manager
title: Preload image
topic: Dynamic media
uuid: bae99269-fd55-485e-b78e-873b77541d91
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Preload image{#preload-image}

Preload image is a static asset preview image which loads right after calling init() method and shows while Viewer SDK libraries, asset and preset information is downloaded. The purpose of the preload image is to visually improve viewer load time and present content to the user quickly.

Preload image works well for the most common viewer embedding method, which is responsive embedding with unrestricted height. See the heading [Responsive design embedding with unrestricted height](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

De functie heeft echter bepaalde beperkingen wanneer andere insluitingsmethoden of specifieke configuratieopties worden gebruikt. Vooraf geladen afbeelding wordt mogelijk niet goed gerenderd in de volgende gevallen:

* Wanneer de viewer een vaste grootte heeft en de grootte is gedefinieerd met gebruik van het `stagesize` configuratiekenmerk in de record met de viewervoorinstelling of in het CSS-bestand voor de externe viewer voor het containerelement op het hoogste niveau.
* Wanneer de flexibele insluiting van grootte wordt gebruikt met de door breedte en hoogte gedefinieerde insluitingsmethode voor viewers. Zie de kop [Flexible size embedding with width and height defined](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Mogelijk moet u de functie Afbeeldingen vooraf laden uitschakelen met het `preloadImage` configuratiekenmerk als u de viewer gebruikt in een van de bovenstaande bewerkingsmodi.

Afbeelding voor vooraf laden wordt ook niet gebruikt, zelfs niet als deze in de configuratie is ingeschakeld. Als de viewer in het DOM-element is ingesloten, wordt deze verborgen met behulp van de `display:none` CSS-instelling of wordt deze losgekoppeld van de DOM-structuur.
