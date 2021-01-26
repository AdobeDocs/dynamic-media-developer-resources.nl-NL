---
description: De RTF-specificatie staat RGB-kleurwaarden toe die zijn opgegeven met &bsol;colortbl. Elke component wordt afzonderlijk voorzien van de &bsol;rood, &bsol;groen, en &bsol;blauw bevelen.
solution: Experience Manager
title: Kleurverwerking
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6c51d204-27ca-4fbd-a297-bf1d04b63a3f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---


# Kleurverwerking{#color-handling}

De RTF-specificatie staat RGB-kleurwaarden toe die zijn opgegeven met `\colortbl`. Elke component wordt afzonderlijk geleverd met de opdrachten `\red`, `\green` en `\blue`.

Met de eigen RTF-extensieopdracht `\cmykcolortbl` kunt u CMYK-kleuren opgeven, waarbij elke kleurcomponent wordt geleverd met de opdrachten `\cyan`, `\magenta`, `\yellow` en `\black`.

De kleurcomponentwaarden voor `\colortbl` liggen in het bereik 0 tot en met 255. Componentwaarden voor `\cmykcolortbl` liggen tussen 0 en 100.

Met de RTF-extensieopdracht `\*\iscolortbl`, ondersteund door `textPs=`, kunt u een kleurentabel opgeven met standaardwaarden voor de kleurserver voor afbeeldingen met volledige RGB-, grijs-, CMYK- en alpha-ondersteuning. Deze heeft de volgende syntaxis:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* een of meer IS-kleurwaarden, gescheiden door &#39;;&#39;

Er kunnen meer dan één type kleurentabel worden opgegeven in dezelfde RTF-tekenreeks `text=` of `textPs=`. Elke kleurentabel kan een ander aantal items hebben. Met Image Serving wordt geprobeerd kleuren in deze volgorde te zoeken: `\iscolortbl` voor `\cmykcolortbl` (alleen als het pixeltype van de tekstlaag CMYK is) vóór `\colortbl`. Alleen voor `textPs=` worden kleuren nauwkeurig omgezet tussen CMYK en RGB, indien dat nodig is (bijvoorbeeld wanneer RGB-kleuren zijn opgegeven maar CMYK-uitvoer is vereist). Als er geen kleur voor een bepaalde indexwaarde wordt gevonden, wordt de standaardkleur (zwart) gebruikt.

Raadpleeg [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) voor een beschrijving van de syntaxis van IS-kleurwaarden.

## Beperkingen {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` biedt geen ondersteuning  `\*\iscolortbl`. `textPs=` biedt geen ondersteuning  `\cmykcolortbl`.

Kleurselecties worden genegeerd bij het renderen van fotolettertypen.

## Voorbeeld {#section-0f166bb72bd44479be01131077851142}

Laat drie tekstkleuren met variabelen worden bestuurd, terwijl het tonen van de kleur standaardwaarde wanneer het koord RTF in een standaardRTF tekstredacteur wordt geopend.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
