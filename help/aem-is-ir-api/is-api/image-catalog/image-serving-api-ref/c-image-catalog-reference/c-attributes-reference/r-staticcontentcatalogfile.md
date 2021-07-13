---
description: Statische gegevenspaden van inhoudscatalogus. Hiermee geeft u de bestanden op die de statische inhoudsgegevens voor deze catalogus bevatten.
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# StaticContentCatalogFile{#staticcontentcatalogfile}

Statische gegevenspaden van inhoudscatalogus. Hiermee geeft u de bestanden op die de statische inhoudsgegevens voor deze catalogus bevatten.

De statische gegevensdossiers van de inhoudscatalogus worden geladen in de gespecificeerde orde. Als dezelfde `static::Id`-waarde voorkomt in meer dan één record (in dezelfde of in verschillende catalogusbestanden), heeft de laatste instantie voorrang.

## Eigenschappen {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Een of meer tekenreekswaarden, gescheiden door komma&#39;s. Optioneel. Elke waarde moet een absoluut bestandspad of pad zijn ten opzichte van de catalogusmap.

## Standaard {#section-702edfbc00c54fc29e412a3ff99fef2b}

Leeg, wat aangeeft dat deze afbeeldingscatalogus geen statische inhoudsgegevens bevat.

## Zie ook {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Catalogusgegevens](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
