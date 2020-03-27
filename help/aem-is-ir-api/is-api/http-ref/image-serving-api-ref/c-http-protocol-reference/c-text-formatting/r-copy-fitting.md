---
description: textPs= implementeert een eigen algoritme voor het passend maken van kopieën die automatisch de tekengrootte(s) aanpassen om het tekstgebied optimaal te vullen met tekst, waardoor extra ruimte aan de onderkant wordt geminimaliseerd en overloop wordt voorkomen.
seo-description: textPs= implementeert een eigen algoritme voor het passend maken van kopieën die automatisch de tekengrootte(s) aanpassen om het tekstgebied optimaal te vullen met tekst, waardoor extra ruimte aan de onderkant wordt geminimaliseerd en overloop wordt voorkomen.
seo-title: Kopiëren
solution: Experience Manager
title: Kopiëren
topic: Scene7 Image Serving - Image Rendering API
uuid: c3ddbf1f-c724-4436-96ff-2c616dfd355d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Kopiëren{#copy-fitting}

textPs= implementeert een eigen algoritme voor het passend maken van kopieën die automatisch de tekengrootte(s) aanpassen om het tekstgebied optimaal te vullen met tekst, waardoor extra ruimte aan de onderkant wordt geminimaliseerd en overloop wordt voorkomen.

Het passend maken van kopieën kan op alineastijl en zelfs voor een afzonderlijk tekstbereik gezamenlijk worden ingeschakeld en beheerd voor de gehele tekstlaag.

Geef de minimale tekengrootte met `\fs` en de maximale tekengrootte met `\copyfit`. Een willekeurig aantal bereiken is toegestaan in dezelfde RTF-tekenreeks. De grootten voor alle bereiken worden proportioneel gevarieerd, zodat de gewenste verhoudingen van de tekengrootte behouden blijven.

`\copyfit` wordt beschouwd als een tekenopmaakopdracht en heeft bereikregels zoals `\fs` en `\b`.

Het passend maken van kopieën wordt uitgeschakeld door `\copyfit` een grootte op te geven die gelijk is aan of kleiner is dan de grootte die met `\fs`is opgegeven.

## Het aantal regels beperken {#section-e5aee0f039e04842afc3d6884ed681ac}

Naast het specificeren van de waaier van doopvontgrootte, kan het gedrag van het exemplaar-passend algoritme verder met de `\copyfitlines` of `\copyfitmaxlines` bevelen worden gecontroleerd, die het aantal lijnen beperken het algoritme zal produceren. Beide bevelen aanvaarden een parameter van de lijntelling of 0, om het aantal lijnen in het gekopieerde gebied niet te beperken.

`\copyfitlines` Hiermee staat u toe dat tekst overloopt op extra regels wanneer deze niet in het opgegeven aantal regels past. Expliciete regeleinden in het tekstsegment dat moet worden gekopieerd, worden altijd toegepast.

`\copyfitmaxlines` Hiermee worden extra uitvoerlijnen die de opgegeven limiet overschrijden, altijd afgebroken. Het opgegeven aantal regels wordt nooit overschreden, zelfs niet als er expliciete regeleinden aanwezig zijn. Bij deze release van Image Serving mogen in het tekstbereik dat op een kopie is aangesloten, niet meer dan N-1 `\line` -markeringen aanwezig zijn. Gedrag is ongedefinieerd als deze limiet wordt overschreden.

## Voorbeelden {#section-f4ddbbfade444560be30a813d90c2c1b}

In de volgende voorbeelden wordt ervan uitgegaan dat tekstlichamen worden voorzien van variabelen met de naam *[!DNL $A$]*, *[!DNL $B$]* en *[!DNL $C$]*.

**Houd dezelfde verhouding tussen de tekengrootten in het hele bereik:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* wordt altijd twee keer zo groot weergegeven als de rest van de tekst. Wanneer er veel tekst is opgegeven *[!DNL $A$]* en *[!DNL $C$]* wordt weergegeven met `\fs10` en *[!DNL $B$]* met `\fs20`. Met weinig tekst, *[!DNL $A$]* en *[!DNL $C$]* zal gebruiken `\fs100` en *[!DNL $B$]* `\fs200`.

**Converteren naar een algemene grote tekengrootte als slechts een kleine hoeveelheid tekst wordt getekend:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

Aan het kleinste einde van het bereik wordt *[!DNL $B$]* het bereik weergegeven met `\fs20`, twee keer zo groot als *[!DNL $A$]* en *[!DNL $C$]* bij `\fs10`. Alle tekst wordt getekend bij `\fs100` (50 punten) aan het tegenovergestelde einde van het bereik.

**Omzetten in een algemene kleine tekengrootte als er veel tekst moet worden weergegeven:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Alle tekst wordt met \fs10 getekend aan het kleine uiteinde van het bereik, terwijl het grootste is, *[!DNL $A$]* en *[!DNL $C$]* wordt gerenderd met `\fs100` en *[!DNL $B$]* met `\fs200`.

**Kopiëren uitschakelen voor een tekstbereik binnen:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

De tekengrootte voor *[!DNL $A$]* en *[!DNL $C$]* kan variëren tussen 10 en 100, terwijl *[!DNL $B$]* deze altijd wordt gerenderd met `\fs50`.

**Beperk de uitvoer tot één regel, zelfs als er meer verticale ruimte beschikbaar is, maar laat deze over naar extra regels als er te veel tekst is opgegeven om in één regel te passen bij`\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Beperk de uitvoer tot één regel, zelfs als er meer verticale ruimte beschikbaar is. Als er te veel tekst is opgegeven om in één regel te passen, wordt`\fs10`deze afgebroken:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
