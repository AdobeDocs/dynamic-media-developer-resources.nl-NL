---
description: textPs= implementeert een eigen algoritme voor het passend maken van kopieën die automatisch de tekengrootte(s) aanpassen om het tekstgebied optimaal te vullen met tekst, waardoor extra ruimte aan de onderkant wordt geminimaliseerd en overloop wordt voorkomen.
solution: Experience Manager
title: Kopiëren
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1a560f3-f92c-4143-b80a-e1674c8a4207
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Kopiëren{#copy-fitting}

textPs= implementeert een eigen algoritme voor het passend maken van kopieën die automatisch de tekengrootte(s) aanpassen om het tekstgebied optimaal te vullen met tekst, waardoor extra ruimte aan de onderkant wordt geminimaliseerd en overloop wordt voorkomen.

Het passend maken van kopieën kan op alineastijl en zelfs voor een afzonderlijk tekstbereik gezamenlijk worden ingeschakeld en beheerd voor de gehele tekstlaag.

Geef de minimale tekengrootte op met `\fs` en de maximale tekengrootte met `\copyfit`. Een willekeurig aantal bereiken is toegestaan in dezelfde RTF-tekenreeks. De grootten voor alle bereiken worden proportioneel gevarieerd, zodat de gewenste verhoudingen van de tekengrootte behouden blijven.

`\copyfit` wordt beschouwd als een opdracht voor het opmaken van tekens en heeft werkingsgebiedregels zoals `\fs` en `\b`.

Aanpassen van kopiëren is uitgeschakeld door op te geven `\copyfit` met een grootte die gelijk is aan of kleiner is dan de grootte die is opgegeven met `\fs`.

## Het aantal regels beperken {#section-e5aee0f039e04842afc3d6884ed681ac}

Naast het opgeven van het bereik van tekengrootten, kunt u het gedrag van het algoritme voor het passend maken van kopieën verder bepalen met het `\copyfitlines` of `\copyfitmaxlines` bevelen, die het aantal lijnen beperken het algoritme zal produceren. Beide bevelen aanvaarden een parameter van de lijntelling of 0, om het aantal lijnen in het gekopieerde gebied niet te beperken.

`\copyfitlines` Hiermee staat u toe dat tekst overloopt op extra regels wanneer deze niet in het opgegeven aantal regels past. Expliciete regeleinden in het tekstsegment dat moet worden gekopieerd, worden altijd toegepast.

`\copyfitmaxlines` Hiermee worden extra uitvoerlijnen die de opgegeven limiet overschrijden, altijd afgebroken. Het opgegeven aantal regels wordt nooit overschreden, zelfs niet als er expliciete regeleinden aanwezig zijn. Voor deze release van Image Serving, niet meer dan N-1 `\line` in het tekstbereik waarin de kopie is gemonteerd, mogen markeringen aanwezig zijn. Gedrag is ongedefinieerd als deze limiet wordt overschreden.

## Voorbeelden {#section-f4ddbbfade444560be30a813d90c2c1b}

In de volgende voorbeelden wordt ervan uitgegaan dat tekstlichamen worden voorzien van variabelen met de naam *[!DNL $A$]*, *[!DNL $B$]*, en *[!DNL $C$]*.

**Houd dezelfde verhouding tussen de tekengrootten in het hele bereik:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* wordt altijd twee keer zo groot weergegeven als de rest van de tekst. Wanneer er veel tekst is opgegeven, *[!DNL $A$]* en *[!DNL $C$]* wordt weergegeven met `\fs10` en *[!DNL $B$]* with `\fs20`. Met weinig tekst, *[!DNL $A$]* en *[!DNL $C$]* gebruikt `\fs100` en *[!DNL $B$]* `\fs200`.

**Converteren naar een algemene grote tekengrootte als slechts een kleine hoeveelheid tekst wordt getekend:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

Aan het kleinste uiteinde van het bereik *[!DNL $B$]* wordt weergegeven met `\fs20`, twee keer zo groot als *[!DNL $A$]* en *[!DNL $C$]* om `\fs10`. Alle tekst wordt getekend bij `\fs100` (50 punten) aan het tegenovergestelde eind van de waaier.

**Omzetten in een algemene kleine tekengrootte als er veel tekst moet worden weergegeven:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Alle tekst wordt getekend met \fs10 aan de kleine zijde van het bereik, terwijl de tekst het grootst is, *[!DNL $A$]* en *[!DNL $C$]* worden weergegeven met `\fs100` en *[!DNL $B$]* with `\fs200`.

**Kopieeraanpassing voor een tekstbereik binnen uitschakelen:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

De tekengrootte voor *[!DNL $A$]* en *[!DNL $C$]* kan variëren tussen 10 en 100, terwijl *[!DNL $B$]* wordt altijd weergegeven met `\fs50`.

**Beperk de uitvoer tot één regel, zelfs als er meer verticale ruimte beschikbaar is, maar laat deze over naar extra regels als er te veel tekst is opgegeven om in één regel te passen bij `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Beperk de uitvoer tot één regel, zelfs als er meer verticale ruimte beschikbaar is. Als er te veel tekst is opgegeven om in één regel te passen bij `\fs10` het is afgekapt:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
