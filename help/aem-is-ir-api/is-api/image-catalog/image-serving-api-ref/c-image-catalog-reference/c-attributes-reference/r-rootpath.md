---
description: Pad naar brongegevenstramien. Absoluut of relatief pad voor de hoofdmap voor de brongegevens van deze afbeeldingscatalogus.
solution: Experience Manager
title: RootPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 06662b27-fb10-41d0-a14c-48025d7e9137
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# RootPath{#rootpath}

Pad naar brongegevenstramien. Absoluut of relatief pad voor de hoofdmap voor de brongegevens van deze afbeeldingscatalogus.

De `RootPath` is een tekenreekswaarde. Zie [Brongegevens beheren](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) voor meer informatie over hoofdpaden van servers.

## Eigenschappen {#section-b41d7e0ea63143eb8034569706cad0c0}

Tekstreeks. Moet leeg zijn, een geldig relatief mappad of een geldig absoluut pad dat toegankelijk is voor de afbeeldingsserver.

## Standaard {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

Overgenomen van `default::RootPath` indien niet gedefinieerd. Als deze wel is gedefinieerd maar leeg is, levert dit geen bijdrage aan het hoofdpad van het bronbestand.

## Zie ook {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catalogus::pad](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catalogus::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),  [ruleset:PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [Brongegevens beheren](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
