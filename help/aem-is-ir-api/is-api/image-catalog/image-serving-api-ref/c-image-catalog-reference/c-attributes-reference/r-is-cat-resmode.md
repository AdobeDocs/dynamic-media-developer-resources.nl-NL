---
description: Standaardmodus voor opnieuw berekenen van pixels. Hiermee geeft u de standaardkenmerken voor resampling en interpolatie op die moeten worden gebruikt voor het schalen van afbeeldingsgegevens.
seo-description: Standaardmodus voor opnieuw berekenen van pixels. Hiermee geeft u de standaardkenmerken voor resampling en interpolatie op die moeten worden gebruikt voor het schalen van afbeeldingsgegevens.
seo-title: ResMode
solution: Experience Manager
title: ResMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 14d184bd-6664-4f8f-b551-a92cb92a0d84
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '95'
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
