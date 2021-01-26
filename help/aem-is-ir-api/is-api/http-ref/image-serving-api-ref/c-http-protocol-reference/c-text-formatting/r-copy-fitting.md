---
description: textPs= implementeert een eigen algoritme voor het passend maken van kopieën die automatisch de tekengrootte(s) aanpassen om het tekstgebied optimaal te vullen met tekst, waardoor extra ruimte aan de onderkant wordt geminimaliseerd en overloop wordt voorkomen.
seo-description: textPs= implementeert een eigen algoritme voor het passend maken van kopieën die automatisch de tekengrootte(s) aanpassen om het tekstgebied optimaal te vullen met tekst, waardoor extra ruimte aan de onderkant wordt geminimaliseerd en overloop wordt voorkomen.
seo-title: Kopiëren
solution: Experience Manager
title: Kopiëren
topic: Dynamic Media Image Serving - Image Rendering API
uuid: c3ddbf1f-c724-4436-96ff-2c616dfd355d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---


# Aanpassen aan kopiëren{#copy-fitting}

textPs= implementeert een eigen algoritme voor het passend maken van kopieën die automatisch de tekengrootte(s) aanpassen om het tekstgebied optimaal te vullen met tekst, waardoor extra ruimte aan de onderkant wordt geminimaliseerd en overloop wordt voorkomen.

Het passend maken van kopieën kan op alineastijl en zelfs voor een afzonderlijk tekstbereik gezamenlijk worden ingeschakeld en beheerd voor de gehele tekstlaag.

Geef de minimale tekengrootte op met `\fs` en de maximale tekengrootte met `\copyfit`. Een willekeurig aantal bereiken is toegestaan in dezelfde RTF-tekenreeks. De grootten voor alle bereiken worden proportioneel gevarieerd, zodat de gewenste verhoudingen van de tekengrootte behouden blijven.

`\copyfit` wordt beschouwd als een tekenopmaakopdracht en heeft werkingsgebiedregels zoals  `\fs` en  `\b`.

Aanpassen van kopiëren is uitgeschakeld door `\copyfit` op te geven met een grootte die gelijk is aan of kleiner is dan de grootte die is opgegeven met `\fs`.

## Het aantal regels beperken {#section-e5aee0f039e04842afc3d6884ed681ac}

Naast het specificeren van de waaier van doopvontgrootte, kan het gedrag van het kopiëren-passend algoritme verder worden gecontroleerd met `\copyfitlines` of `\copyfitmaxlines` bevelen, die het aantal lijnen beperken het algoritme zal produceren. Beide bevelen aanvaarden een parameter van de lijntelling of 0, om het aantal lijnen in het gekopieerde gebied niet te beperken.

`\copyfitlines` Hiermee staat u toe dat tekst overloopt op extra regels wanneer deze niet in het opgegeven aantal regels past. Expliciete regeleinden in het tekstsegment dat moet worden gekopieerd, worden altijd toegepast.

`\copyfitmaxlines` Hiermee worden extra uitvoerlijnen die de opgegeven limiet overschrijden, altijd afgebroken. Het opgegeven aantal regels wordt nooit overschreden, zelfs niet als er expliciete regeleinden aanwezig zijn. Bij deze release van Image Serving mogen er niet meer dan N-1 `\line` markeringen aanwezig zijn in het tekstbereik dat is gekoppeld aan de kopie. Gedrag is ongedefinieerd als deze limiet wordt overschreden.

## Voorbeelden {#section-f4ddbbfade444560be30a813d90c2c1b}

In de volgende voorbeelden wordt ervan uitgegaan dat teksthoofdteksten worden geleverd met variabelen met de namen *[!DNL $A$]*, *[!DNL $B$]* en *[!DNL $C$]*.

**Houd dezelfde verhouding tussen de tekengrootten in het hele bereik:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* wordt altijd twee keer zo groot weergegeven als de rest van de tekst. Wanneer er veel tekst is opgegeven, worden *[!DNL $A$]* en *[!DNL $C$]* weergegeven met `\fs10` en *[!DNL $B$]* met `\fs20`. Met weinig tekst gebruiken *[!DNL $A$]* en *[!DNL $C$]* `\fs100` en *[!DNL $B$]* `\fs200`.

**Converteren naar een algemene grote tekengrootte als slechts een kleine hoeveelheid tekst wordt getekend:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

Aan het kleinste einde van het bereik wordt *[!DNL $B$]* weergegeven met `\fs20`, twee keer zo groot als *[!DNL $A$]* en *[!DNL $C$]* bij `\fs10`. Alle tekst wordt om `\fs100` (50 punten) getekend aan het tegenovergestelde einde van het bereik.

**Omzetten in een algemene kleine tekengrootte als er veel tekst moet worden weergegeven:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Alle tekst wordt getekend met \fs10 op het kleine uiteinde van het bereik, terwijl *[!DNL $A$]* en *[!DNL $C$]* op het grootste punt worden gerenderd met `\fs100` en *[!DNL $B$]* met `\fs200`.

**Kopieeraanpassing voor een tekstbereik binnen uitschakelen:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

De fontgrootte voor *[!DNL $A$]* en *[!DNL $C$]* kan tussen 10 en 100 variëren, terwijl *[!DNL $B$]* altijd met `\fs50` wordt teruggegeven.

**Beperk de uitvoer tot één regel, zelfs als er meer verticale ruimte beschikbaar is, maar laat deze over naar extra regels als er te veel tekst is opgegeven om in één regel te passen bij  `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Beperk de uitvoer tot één regel, zelfs als er meer verticale ruimte beschikbaar is. Als er te veel tekst is opgegeven om in één regel op `\fs10` te passen, wordt deze afgebroken:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
