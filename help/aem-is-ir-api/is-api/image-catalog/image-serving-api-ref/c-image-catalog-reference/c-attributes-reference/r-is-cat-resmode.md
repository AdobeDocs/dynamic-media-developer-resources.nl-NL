---
title: ResMode
description: Standaardmodus voor opnieuw berekenen van pixels. Hiermee geeft u de standaardkenmerken voor resampling en interpolatie op die moeten worden gebruikt voor het schalen van afbeeldingsgegevens.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# ResMode{#resmode}

Standaardmodus voor opnieuw berekenen van pixels. Hiermee geeft u de standaardkenmerken voor resampling en interpolatie op die moeten worden gebruikt voor het schalen van afbeeldingsgegevens.

Wordt gebruikt wanneer `resMode=` wordt niet opgegeven in een aanvraag.

## Eigenschappen {#section-493f900be522486f97710cebdc4460c2}

Enum. Instellen op 2 voor `bilin`, 3 voor `bicub`, of 4 voor `sharp2` interpolatiemodus (zie [resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md) voor meer informatie). `sharp` (1) wordt afgekeurd. Gebruiken `sharp2` (4) voor de beste resultaten.

## Standaard {#section-35f980e745fc4d79a2621e8abacc724d}

Overgenomen van `default::ResMode` indien niet gedefinieerd of leeg.

## Zie ook {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
