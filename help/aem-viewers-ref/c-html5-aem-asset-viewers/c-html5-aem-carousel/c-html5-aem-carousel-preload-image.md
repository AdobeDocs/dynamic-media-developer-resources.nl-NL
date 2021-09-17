---
title: Afbeelding vooraf laden
description: Afbeelding vooraf laden is een voorbeeldafbeelding van statische elementen die direct wordt geladen nadat de methode init() is aangeroepen en die wordt weergegeven terwijl de bibliotheken, elementen en voorinstellingen van de SDK van de viewer worden gedownload. Het doel van de vooraf geladen afbeelding is om de laadtijd van de viewer visueel te verbeteren en inhoud snel aan de gebruiker voor te stellen.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Afbeelding vooraf laden{#preload-image}

Afbeelding vooraf laden is een voorbeeldafbeelding van statische elementen die direct wordt geladen nadat de methode init() is aangeroepen en die wordt weergegeven terwijl de bibliotheken, elementen en voorinstellingen van de SDK van de viewer worden gedownload. Het doel van de vooraf geladen afbeelding is om de laadtijd van de viewer visueel te verbeteren en inhoud snel aan de gebruiker voor te stellen.

Afbeelding vooraf laden werkt goed voor de meest gebruikte insluitingsmethode voor viewers, die reageert op insluiten met onbeperkte hoogte. Zie de kop [Responsief insluiten van ontwerp met onbeperkte hoogte](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

De functie heeft echter bepaalde beperkingen wanneer andere insluitingsmethoden of specifieke configuratieopties worden gebruikt. Vooraf geladen afbeelding wordt mogelijk niet goed gerenderd in de volgende gevallen:

* Wanneer de viewer een vaste grootte heeft en de grootte is gedefinieerd met het configuratiekenmerk `stagesize` in de record met de viewervoorinstelling of, in het CSS-bestand voor de externe viewer voor het containerelement op het hoogste niveau.
* Als u de flexibele insluiting voor grootte gebruikt met de door breedte en hoogte gedefinieerde insluitingsmethode voor viewers. Zie de kop [Flexibele insluiting van grootte met gedefinieerde breedte en hoogte](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Als u de viewer in een van de bovenstaande bewerkingsmodi gebruikt, schakelt u de functie voor het vooraf laden van afbeeldingen uit met het configuratiekenmerk `preloadImage`.

Bovendien wordt de vooraf geladen afbeelding niet gebruikt, zelfs niet als deze in de configuratie is ingeschakeld. Als de viewer in het DOM-element is ingesloten, wordt deze verborgen met de CSS-instelling `display:none` of wordt deze losgekoppeld van de DOM-structuur.
