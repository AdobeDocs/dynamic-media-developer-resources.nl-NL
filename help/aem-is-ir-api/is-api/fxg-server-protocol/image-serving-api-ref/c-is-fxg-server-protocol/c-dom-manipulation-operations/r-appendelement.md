---
description: XML toevoegen aan een s7 elementID.
solution: Experience Manager
title: appendElement
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---


# appendElement{#appendelement}

XML toevoegen aan een s7:elementID.

`appendElement.elementID=<XML>`

Als voor een FXG-knooppuntelement een `s7:elementID` is gedefinieerd, wordt de waarde `<XML>` toegevoegd als een onderliggend element. De `<XML>` moet worden gecodeerd.

## Voorbeeld {#section-4368570aa198485d91b73b4d0741478f}

Veronderstel een `s7:elementID="group1"` attribuut voor een knoop van de Groep dan het volgende geldig is wordt bepaald:

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

In dit voorbeeld wordt een onderliggende tekstafbeelding toegevoegd aan `group1`.
