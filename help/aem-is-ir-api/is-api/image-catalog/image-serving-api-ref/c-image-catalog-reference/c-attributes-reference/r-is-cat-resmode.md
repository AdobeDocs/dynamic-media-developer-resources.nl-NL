---
description: Standaardmodus voor opnieuw berekenen van pixels. Hiermee geeft u de standaardkenmerken voor resampling en interpolatie op die moeten worden gebruikt voor het schalen van afbeeldingsgegevens.
solution: Experience Manager
title: ResMode
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# ResMode{#resmode}

Standaardmodus voor opnieuw berekenen van pixels. Hiermee geeft u de standaardkenmerken voor resampling en interpolatie op die moeten worden gebruikt voor het schalen van afbeeldingsgegevens.

Wordt gebruikt wanneer `resMode=` niet is opgegeven in een aanvraag.

## Eigenschappen {#section-493f900be522486f97710cebdc4460c2}

Enum. Stel in op 2 voor `bilin`, 3 voor `bicub` of 4 voor `sharp2` interpolatiemodus (zie ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)` voor meer informatie). `sharp` (1) wordt afgekeurd. Gebruik `sharp2` (4) in plaats daarvan voor de beste resultaten.

## Standaard {#section-35f980e745fc4d79a2621e8abacc724d}

Overgenomen van `default::ResMode` indien niet gedefinieerd of indien leeg.

## Zie ook {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
