---
description: XML toevoegen aan een s7 elementID.
solution: Experience Manager
title: appendElement
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# appendElement{#appendelement}

XML toevoegen aan een s7:elementID.

`appendElement.elementID=<XML>`

Als een FXG-knoopelement een `s7:elementID` de `<XML>` waarde wordt toegevoegd als een onderliggend element. De `<XML>` moet gecodeerd zijn.

## Voorbeeld {#section-4368570aa198485d91b73b4d0741478f}

Stel een `s7:elementID="group1"` Het attribuut wordt bepaald voor een knoop van de Groep dan is het volgende geldig:

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

In dit voorbeeld wordt een onderliggende tekstafbeelding toegevoegd aan `group1`.
