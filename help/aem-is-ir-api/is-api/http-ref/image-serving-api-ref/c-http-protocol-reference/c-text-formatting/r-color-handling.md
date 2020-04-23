---
description: De RTF-specificatie staat RGB-kleurwaarden toe die zijn opgegeven met \colortbl. Elke component wordt afzonderlijk geleverd met de opdrachten \red, \green en \blue.
seo-description: De RTF-specificatie staat RGB-kleurwaarden toe die zijn opgegeven met \colortbl. Elke component wordt afzonderlijk geleverd met de opdrachten \red, \green en \blue.
seo-title: Kleurverwerking
solution: Experience Manager
title: Kleurverwerking
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c51d204-27ca-4fbd-a297-bf1d04b63a3f
translation-type: tm+mt
source-git-commit: 341693d69fc414dacf984d66e2eaeba2418e663b

---


# Kleurverwerking{#color-handling}

De RTF-specificatie staat RGB-kleurwaarden toe die zijn opgegeven met `\colortbl`. Elke component wordt afzonderlijk verstrekt met de `\red`, `\green`, en `\blue` bevelen.

Met de eigen RTF-extensieopdracht `\cmykcolortbl` kunt u CMYK-kleuren opgeven waarbij elke kleurcomponent de opdrachten `\cyan`, `\magenta`, `\yellow`en `\black` opdrachten krijgt.

De waarden van de kleurcomponent voor `\colortbl` liggen in het bereik 0 tot en met 255. Componentwaarden voor `\cmykcolortbl` liggen tussen 0 en 100.

Met de RTF-extensieopdracht `\*\iscolortbl`, ondersteund door `textPs=`, kunt u een kleurentabel opgeven met standaardwaarden voor de kleurserver voor afbeeldingen, met volledige ondersteuning voor RGB, grijs, CMYK en alfa. Deze heeft de volgende syntaxis:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* een of meer IS-kleurwaarden, gescheiden door &#39;;&#39;

Meer dan één type kleurentabel kan in dezelfde `text=` of `textPs=` RTF-tekenreeks worden opgegeven. Elke kleurentabel kan een ander aantal items hebben. Met Image Serving wordt geprobeerd kleuren in deze volgorde te zoeken: `\iscolortbl` voor `\cmykcolortbl` (alleen als het pixeltype van de tekstlaag CMYK is) `\colortbl`. Alleen `textPs=` alleen de kleuren worden op de juiste wijze omgezet tussen CMYK en RGB, als dat nodig is (bijvoorbeeld wanneer RGB-kleuren zijn opgegeven maar CMYK-uitvoer is vereist). Als er geen kleur voor een bepaalde indexwaarde wordt gevonden, wordt de standaardkleur (zwart) gebruikt.

Raadpleeg de [kleur](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) voor een beschrijving van de syntaxis van IS-kleurwaarden.

## Beperkingen {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` biedt geen ondersteuning `\*\iscolortbl`. `textPs=` biedt geen ondersteuning `\cmykcolortbl`.

Kleurselecties worden genegeerd bij het renderen van fotolettertypen.

## Voorbeeld {#section-0f166bb72bd44479be01131077851142}

Laat drie tekstkleuren met variabelen worden bestuurd, terwijl het tonen van de kleur standaardwaarde wanneer het koord RTF in een standaardRTF tekstredacteur wordt geopend.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
