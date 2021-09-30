---
title: Afbeelding vooraf laden
description: Afbeelding vooraf laden is een voorbeeldafbeelding van statische elementen die direct wordt geladen nadat de methode init() is aangeroepen en die wordt weergegeven terwijl de bibliotheken, elementen en voorinstellingen van de SDK van de viewer worden gedownload. Het doel van de vooraf geladen afbeelding is om de laadtijd van de viewer visueel te verbeteren en inhoud snel aan de gebruiker voor te stellen.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Afbeelding vooraf laden{#preload-image}

Afbeelding vooraf laden is een voorbeeldafbeelding van statische elementen die direct wordt geladen nadat de methode init() is aangeroepen en die wordt weergegeven terwijl de bibliotheken, elementen en voorinstellingen van de SDK van de viewer worden gedownload. Het doel van de vooraf geladen afbeelding is om de laadtijd van de viewer visueel te verbeteren en inhoud snel aan de gebruiker voor te stellen.

Afbeelding vooraf laden werkt goed voor de meest gebruikte insluitingsmethode voor viewers, die reageert op insluiten met onbeperkte hoogte. Zie de kop [Responsief insluiten van ontwerp met onbeperkte hoogte](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

De functie heeft echter bepaalde beperkingen wanneer andere insluitingsmethoden of specifieke configuratieopties worden gebruikt. Vooraf geladen afbeelding wordt mogelijk niet goed gerenderd in de volgende gevallen:

* Wanneer de viewer een vaste grootte heeft en de grootte is gedefinieerd met het configuratiekenmerk `stagesize` in de record met de viewervoorinstelling. Of u gebruikt het CSS-bestand voor de externe viewer voor het containerelement op het hoogste niveau.
* Als u de flexibele insluiting voor grootte gebruikt met de door breedte en hoogte gedefinieerde insluitingsmethode voor viewers. Zie de kop [Flexibele insluiting van grootte met gedefinieerde breedte en hoogte](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Schakel de functie Afbeelding vooraf laden uit met het configuratiekenmerk `preloadImage` als u de viewer gebruikt in een van de bovenstaande bewerkingsmodi.

Bovendien wordt de vooraf geladen afbeelding niet gebruikt, zelfs niet als deze in de configuratie is ingeschakeld. Als de viewer in het DOM-element is ingesloten, wordt deze verborgen met de CSS-instelling `display:none` of wordt deze losgekoppeld van de DOM-structuur.
