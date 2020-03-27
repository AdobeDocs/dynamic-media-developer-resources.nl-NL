---
description: Compatibiliteitsnotities voor besturingssystemen, browsers en mobiele apparaten.
seo-description: Compatibiliteitsnotities voor besturingssystemen, browsers en mobiele apparaten.
seo-title: Compatibiliteitsnotities
solution: Experience Manager
title: Compatibiliteitsnotities
topic: Dynamic media
uuid: cf732a03-bfaa-4838-862f-73343cefbd67
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Compatibiliteitsnotities{#compatibility-notes}

Compatibiliteitsnotities voor besturingssystemen, browsers en mobiele apparaten.

## Blackberry {#section-0c465ac3775d47fd838e2695a00abc45}

* Incompatibiliteit met oudere adaptieve videosets. Mogelijk moet u Adaptive Video Sets opnieuw uploaden om het afspelen mogelijk te maken.

## Algemeen {#section-7b9a9fcba85148d1802b7b3016b48e02}

* Schalen aan de browserzijde kan de interface en afbeeldingen vervagen als de gebruiker inzoomt op de pagina. UI-opmaak wordt mogelijk ook onjuist weergegeven, afhankelijk van zoomen. Dit gaat over op het volledige scherm.
* Vanwege de groottebeperking op mobiele apparaten gebruikt de gemengde Media Viewer een diabeweging om frames in ingesloten afbeeldingssets te wisselen in plaats van te tikken op de ingesloten staalcomponent. De component is er als visuele indicator.
* In Internet Explorer-browsers en sommige aanraakapparaten neemt de modus Volledig scherm niet het volledige apparaatscherm in beslag. In plaats daarvan wordt de grootte van de toepassing aangepast aan het browservenster.
* De knop Sluiten werkt niet onder iOS 8.0 en iOS 8.1, maar onder iOS 8.2.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Geheugenlek gezien met Zoom- en eCatalog-viewers. Herhaalde navigatie door frames kan ertoe leiden dat de browser vastloopt.
* Dubbeltikken op een viewer kan ertoe leiden dat de gehele pagina in- en uitzoomen in plaats van alleen de viewer waarvoor schaling aan de browserzijde is ingeschakeld.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Apparaat gedetecteerd als tablet in de staande modus met Volledig scherm ingeschakeld in de browserinstellingen.

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Dubbeltikken op een viewer kan ertoe leiden dat de gehele pagina in- en uitzoomen in plaats van alleen de viewer, waarbij schaling aan de browserzijde is ingeschakeld.

## Galaxy Nexus 10 en Galaxy tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* In eCatalog wordt een onjuiste paginaspread weergegeven met de stand Staand en Liggend.

## HTC mobiele apparaten {#section-dc42c80414c842e488738fc157c55b01}

* Het onvermogen om inheems knijpzoem onbruikbaar te maken is een &quot;eigenschap&quot;van de omslag van HTML UI (van HTC Sense). Deze functie kan ertoe leiden dat op een gehele pagina wordt ingezoomd wanneer een zoombeweging met een knijpbeweging in de viewer wordt gebruikt. Gebruik in plaats hiervan een dubbeltikbeweging.
* Pictogrammen met afbeeldingen met hyperlinks kunnen elkaar overlappen als de afbeeldingen met hyperlinks klein zijn en dicht bij elkaar liggen.

## HTML5 Video Viewer {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` modifier wordt alleen ondersteund bij het afspelen van software-HLS en flash HDS. Dit werkt niet wanneer het afspelen de native speler gebruikt.
* OGG en WebM progressief afspelen niet ondersteund.
* Schalen in de browser kan ertoe leiden dat de videospeler op een onjuiste grootte wordt weergegeven (inclusief de weergave-instellingen van het besturingsvenster van Windows OS).
* Videozoekopdrachten waarbij gebruik wordt gemaakt van HLS-streaming op Safari kunnen inconsistent zijn.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* De modus Kwarten wordt niet ondersteund.
* De compatibiliteitsmodus wordt niet ondersteund.
* Internet Explorer op mobiel wordt niet ondersteund.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Grote eCatalogs kunnen ertoe leiden dat de browser vastloopt op iPad 2.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 of hoger: Instellingen voor de insteekmodule Internet kunnen het afspelen van Flash-video voorkomen.
* Videozoekopdrachten waarbij gebruik wordt gemaakt van HLS-streaming op Safari kunnen inconsistent zijn.
* Kan niet zoeken tot einde van video in Safari 6 met gebruik van HLS-streaming.

