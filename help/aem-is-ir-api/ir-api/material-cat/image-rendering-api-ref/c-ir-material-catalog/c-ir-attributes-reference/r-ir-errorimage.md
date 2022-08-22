---
title: ErrorImage
description: Error response image. Bij rendering van afbeeldingen wordt doorgaans een foutstatus met een tekstbericht geretourneerd wanneer een fout optreedt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# ErrorImage {#errorimage}

Error response image. Bij rendering van afbeeldingen wordt doorgaans een foutstatus met een tekstbericht geretourneerd wanneer een fout optreedt. De `attribute::ErrorImage` Hiermee kunt u een afbeelding configureren die wordt geretourneerd als er een fout optreedt.

Wanneer een fout optreedt, probeert de server de waarde van `ImageRendering::attribute::ErrorImage`als een eenvoudig pad naar een afbeeldingsbestand. Als het bestand niet kan worden geopend, worden de kenmerkwaarde en de foutgegevens naar de Image Serving verzonden, die de in `ImageServing::attribute::ErrorImage`. Als Image Serving geen geldige reactieafbeelding retourneert, worden de standaard HTTP-foutstatus en het tekstbericht naar de client verzonden.

Foutafbeeldingen worden geretourneerd met HTTP-status 200.

## Eigenschappen {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Tekstreeks. Indien opgegeven, moet het een **`ImageServing::catalog::id`** waarde, een relatief pad (naar **`ImageServing::attribute::RootPath`** of **`ImageRendering::attribute::RootPath`**) of een absoluut pad naar een afbeeldingsbestand dat toegankelijk is voor de afbeeldingsserver.

## Standaard {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Overgenomen van `default::ErrorImage` als deze niet is gedefinieerd. Als deze is gedefinieerd maar leeg is, wordt het gedrag van de afbeelding met foutmeldingen uitgeschakeld, zelfs als `default::ErrorImage` wordt gedefinieerd en wordt een HTTP-foutstatus geretourneerd.

## Zie ook {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [kenmerk::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b), [kenmerk::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3), [catalogus::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
