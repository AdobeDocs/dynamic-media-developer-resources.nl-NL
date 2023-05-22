---
description: De RTF-specificatie staat RGB-kleurwaarden toe die zijn opgegeven met &bsol;colortbl. Elke component wordt afzonderlijk voorzien van de &bsol;rood, &bsol;groen, en &bsol;blauw bevelen.
solution: Experience Manager
title: Kleurverwerking
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Kleurverwerking{#color-handling}

De RTF-specificatie staat RGB-kleurwaarden toe die zijn opgegeven met `\colortbl`. Elke component wordt afzonderlijk geleverd bij de `\red`, `\green`, en `\blue` opdrachten.

De RTF-extensie-opdracht `\cmykcolortbl` staat het specificeren van CMYK kleuren met elke kleurencomponent toe die met wordt voorzien `\cyan`, `\magenta`, `\yellow`, en `\black` opdrachten.

Waarden van kleurcomponenten voor `\colortbl` liggen in het bereik 0-255. Componentwaarden voor `\cmykcolortbl` liggen in het bereik 0 tot en met 100.

De opdracht RTF-extensie `\*\iscolortbl`, ondersteund door `textPs=`, biedt een manier om een kleurentabel op te geven met standaardwaarden voor afbeeldingsservers, met volledige RGB-, grijs-, CMYK- en alpha-ondersteuning. Deze heeft de volgende syntaxis:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* een of meer IS-kleurwaarden, gescheiden door &#39;;&#39;

Er kunnen meerdere typen kleurentabel worden opgegeven in hetzelfde `text=` of `textPs=` RTF-tekenreeks. Elke kleurentabel kan een ander aantal items hebben. Met Image Serving wordt geprobeerd kleuren in deze volgorde te zoeken: `\iscolortbl` voor `\cmykcolortbl` (alleen als het pixeltype van de tekstlaag CMYK is) voor `\colortbl`. Voor `textPs=` alleen, worden kleuren nauwkeurig omgezet tussen CMYK en RGB, als dat nodig is (bijvoorbeeld wanneer RGB-kleuren zijn opgegeven maar CMYK-uitvoer is vereist). Als er geen kleur voor een bepaalde indexwaarde wordt gevonden, wordt de standaardkleur (zwart) gebruikt.

Zie [kleur](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) voor een beschrijving van de syntaxis van IS-kleurwaarden.

## Beperkingen {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` ondersteunt niet `\*\iscolortbl`. `textPs=` ondersteunt niet `\cmykcolortbl`.

Kleurselecties worden genegeerd bij het renderen van fotolettertypen.

## Voorbeeld {#section-0f166bb72bd44479be01131077851142}

Laat drie tekstkleuren met variabelen worden bestuurd, terwijl het tonen van de kleur standaardwaarde wanneer het koord RTF in een standaardRTF tekstredacteur wordt geopend.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
