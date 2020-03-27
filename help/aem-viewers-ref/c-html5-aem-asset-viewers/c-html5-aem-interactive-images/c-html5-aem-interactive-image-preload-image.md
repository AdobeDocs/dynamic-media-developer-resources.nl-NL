---
description: Afbeelding vooraf laden is een voorbeeldafbeelding van statische elementen die direct wordt geladen nadat de methode init() is aangeroepen en die wordt weergegeven terwijl de SDK-bibliotheken van de viewer, de elementen en de voorinstellingen worden gedownload. Het doel van de vooraf geladen afbeelding is om de laadtijd van de viewer visueel te verbeteren en inhoud snel aan de gebruiker voor te stellen.
seo-description: Afbeelding vooraf laden is een voorbeeldafbeelding van statische elementen die direct wordt geladen nadat de methode init() is aangeroepen en die wordt weergegeven terwijl de SDK-bibliotheken van de viewer, de elementen en de voorinstellingen worden gedownload. Het doel van de vooraf geladen afbeelding is om de laadtijd van de viewer visueel te verbeteren en inhoud snel aan de gebruiker voor te stellen.
seo-title: Afbeelding vooraf laden
solution: Experience Manager
title: Afbeelding vooraf laden
topic: Dynamic media
uuid: cb5db16d-b496-40e4-b8ef-5573c42d2850
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Afbeelding vooraf laden{#preload-image}

Afbeelding vooraf laden is een voorbeeldafbeelding van statische elementen die direct wordt geladen nadat de methode init() is aangeroepen en die wordt weergegeven terwijl de SDK-bibliotheken van de viewer, de elementen en de voorinstellingen worden gedownload. Het doel van de vooraf geladen afbeelding is om de laadtijd van de viewer visueel te verbeteren en inhoud snel aan de gebruiker voor te stellen.

Afbeelding vooraf laden werkt goed voor de meest gebruikte insluitingsmethode voor viewers, die reageert op insluiten met onbeperkte hoogte. Zie de kop [Responsief insluiten van ontwerp met onbeperkte hoogte](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

De functie heeft echter bepaalde beperkingen wanneer andere insluitingsmethoden of specifieke configuratieopties worden gebruikt. Vooraf geladen afbeelding wordt mogelijk niet goed gerenderd in de volgende gevallen:

* Wanneer de viewer een vaste grootte heeft en de grootte is gedefinieerd met gebruik van het `stagesize` configuratiekenmerk in de record met de viewervoorinstelling of in het CSS-bestand voor de externe viewer voor het containerelement op het hoogste niveau.
* Wanneer de flexibele insluiting van grootte wordt gebruikt met de door breedte en hoogte gedefinieerde insluitingsmethode voor viewers. Zie de kop [Flexible size embedding with width and height defined](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Mogelijk moet u de functie Afbeeldingen vooraf laden uitschakelen met het `preloadImage` configuratiekenmerk als u de viewer gebruikt in een van de bovenstaande bewerkingsmodi.

Afbeelding voor vooraf laden wordt ook niet gebruikt, zelfs niet als deze in de configuratie is ingeschakeld. Als de viewer in het DOM-element is ingesloten, wordt deze verborgen met behulp van de `display:none` CSS-instelling of wordt deze losgekoppeld van de DOM-structuur.
