---
title: Compatibiliteitsnotities
description: Compatibiliteitsnotities voor besturingssystemen, browsers en mobiele apparaten.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Compatibiliteitsnotities{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Compatibiliteitsnotities voor besturingssystemen, browsers en mobiele apparaten.

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* Incompatibiliteit met oudere adaptieve videosets. Laad Adaptieve videosets opnieuw om het afspelen mogelijk te maken.

## Algemeen {#section-7b9a9fcba85148d1802b7b3016b48e02}

* Schalen aan de browserzijde zorgt ervoor dat de gebruikersinterface en afbeeldingen vaag worden wanneer de gebruiker inzoomt op de pagina. De opmaak van de gebruikersinterface wordt ook onjuist weergegeven, afhankelijk van de zoomfactor en wordt naar het volledige scherm overgedragen.
* Vanwege de groottebeperking op mobiele apparaten gebruikt de gemengde Media Viewer een diabeweging om frames in ingesloten afbeeldingssets te wisselen in plaats van te tikken op de ingesloten staalcomponent. De component is er als visuele indicator.
* In Internet Explorer-browsers en sommige aanraakapparaten neemt de modus Volledig scherm niet het volledige apparaatscherm in beslag. In plaats daarvan wordt de grootte van de toepassing aangepast aan het browservenster.
* De knop Sluiten werkt niet onder iOS 8.0 en iOS 8.1, maar onder iOS 8.2.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Geheugenlek gezien met Zoom- en eCatalog-viewers. Bij herhaalde navigatie door frames loopt de browser vast.
* Dubbeltikken op een viewer zorgt ervoor dat de gehele pagina in- en uitzoomt in plaats van alleen de viewer waarvoor schaling aan de browserzijde is ingeschakeld.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Apparaat gedetecteerd als tablet in de staande modus met volledig scherm ingeschakeld in de browserinstellingen.

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Dubbeltikken op een viewer zorgt ervoor dat de gehele pagina in- en uitzoomt in plaats van alleen de viewer, waarbij schaling aan de browserzijde is ingeschakeld.

## Galaxy Nexus 10 en Galaxy tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* In eCatalog wordt een onjuiste paginaspread weergegeven met de stand Staand en Liggend.

## HTC mobiele apparaten {#section-dc42c80414c842e488738fc157c55b01}

* Het onvermogen om inheems knijpzoem onbruikbaar te maken is een &quot;eigenschap&quot;van de omslag van HTML UI (van HTC Sense). Deze functie kan ertoe leiden dat op een gehele pagina wordt ingezoomd wanneer een zoombeweging met een knijpbeweging in de viewer wordt gebruikt. Gebruik in plaats hiervan een dubbeltikbeweging.
* Pictogrammen met afbeeldingen met hyperlinks overlappen als de afbeeldingen met hyperlinks klein zijn en dicht bij elkaar liggen.

## HTML5 Video Viewer {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` modifier wordt alleen ondersteund bij het afspelen van software-HLS en Flash HDS. Dit werkt niet wanneer het afspelen de native speler gebruikt.
* OGG en WebM progressief afspelen wordt niet ondersteund.
* Browserschaling zorgt ervoor dat de videospeler op een onjuiste grootte wordt weergegeven (inclusief de weergave-instellingen van het Configuratiescherm van Windows®).
* Het gebruik van HLS-streaming op Safari is niet consistent.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* De modus Kwarten wordt niet ondersteund.
* De compatibiliteitsmodus wordt niet ondersteund.
* Internet Explorer op mobiel wordt niet ondersteund.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Grote eCatalogs veroorzaken dat browser op iPad 2 crasht.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 of hoger: instellingen voor de plug-in Internet verhinderen het afspelen van video in de Flash.
* Het gebruik van HLS-streaming op Safari is niet consistent.
* Kan niet zoeken tot einde van video in Safari 6 met gebruik van HLS-streaming.
