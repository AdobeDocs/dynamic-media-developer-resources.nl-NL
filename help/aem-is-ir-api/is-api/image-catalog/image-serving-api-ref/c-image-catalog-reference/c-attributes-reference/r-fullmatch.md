---
description: Overeenkomende optie voor catalogi.
solution: Experience Manager
title: FullMatch
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# FullMatch{#fullmatch}

Overeenkomende optie voor catalogi.

Een catalogusitem wordt opgegeven als een `*`rootId`*/ *`imageId`*` paar in HTTP-aanvragen. Bij het parseren wordt een catalogus geselecteerd als `*`rootId`*` komt overeen met de `attribute::RootId` waarde van de catalogus en de catalogusrecord wordt geïdentificeerd door overeenkomende `*`imageId`*` met een `catalog::Id` waarde. Als een catalogus wordt gevonden, maar er geen overeenkomende catalogus-items zijn `*`imageId`*`De server kan echter een van de volgende twee dingen doen:

Indien `attribute::FullMatch` niet is ingesteld, gebruikt de server de kenmerken van de overeenkomende catalogus. In dit geval: `*`rootId`*` wordt vervangen door `attribute::RootPath` (of `default::RootPath`, indien niet opgegeven in deze catalogus).

Indien `attribute::FullMatch` wordt ingesteld, negeert de server de catalogus volledig, alsof er geen overeenkomende catalogus is gevonden, en gaat u verder met de standaardcataloguskenmerken. In dit geval: `*`rootId`*` blijft deel uitmaken van het pad (wordt voorafgegaan door `default::RootPath`).

## Eigenschappen {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Markering. Stel dit in op 0 voor standaardgedrag of op 1 om gedrag bij volledige overeenkomst in te schakelen.

## Standaard {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Overgenomen van `default::FullMatch` indien niet gedefinieerd of leeg.

## Zie ook {#section-42da0ba53e0b4c089c62108785faf5a9}

[kenmerk::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catalogus::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
