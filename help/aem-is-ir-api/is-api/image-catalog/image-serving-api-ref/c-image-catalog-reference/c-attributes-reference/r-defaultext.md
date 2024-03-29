---
description: Achtervoegsel standaardafbeeldingsbestand. Toegevoegd aan de veldwaarde voor het pad naar de catalogus (of het catalogusmaskerPath) als het pad geen achtervoegsel voor het bestand bevat
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 43b3e5b8-6374-458d-8503-8e04c8c84233
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# DefaultExt{#defaultext}

Achtervoegsel standaardafbeeldingsbestand. Toegevoegd aan de catalogus::Path (of catalogus::MaskPath)-veldwaarde als het pad geen achtervoegsel voor het bestand bevat

Een achtervoegsel voor een bestand bestaat uit een punt en een of meer tekens tussen de punt en het einde van de tekenreeks. Het achtervoegsel wordt toegevoegd aan de weg van http, als de weg niet aan een catalogusingang oplost, en als het laatste wegelement geen dossierachtervoegsel omvat.

## Eigenschappen {#section-b024e6450b414ccc8b83a48a3b4e00f9}

Tekstreeks. Moet een regelafstand &#39;.&#39; bevatten en een of meer tekens.

## Standaard {#section-1194c36ffe0748c5b9ff7d732a506588}

Overgenomen van `default::DefaultExt` indien niet gedefinieerd. Als deze catalogus is gedefinieerd maar leeg is, wordt er geen standaardachtervoegsel toegepast op namen van afbeeldingen wanneer u deze catalogus gebruikt.

## Zie ook {#section-d7c408b979844643adff8258f500eb7c}

[catalogus::pad](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catalogus::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
