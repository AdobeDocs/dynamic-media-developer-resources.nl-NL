---
description: Error response image. Bij rendering van afbeeldingen wordt doorgaans een foutstatus met een tekstbericht geretourneerd wanneer een fout optreedt. kenmerk ErrorImage maakt het mogelijk een afbeelding te configureren die moet worden geretourneerd in het geval van een fout.
seo-description: Error response image. Bij rendering van afbeeldingen wordt doorgaans een foutstatus met een tekstbericht geretourneerd wanneer een fout optreedt. kenmerk ErrorImage maakt het mogelijk een afbeelding te configureren die moet worden geretourneerd in het geval van een fout.
seo-title: ErrorImage *
solution: Experience Manager
title: ErrorImage *
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c8801d0-8cd0-4477-9a60-ccbb343a0747
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---


# ErrorImage *{#errorimage}

Error response image. Bij rendering van afbeeldingen wordt doorgaans een foutstatus met een tekstbericht geretourneerd wanneer een fout optreedt. kenmerk::ErrorImage maakt het mogelijk een afbeelding te configureren die moet worden geretourneerd in het geval van een fout.

Wanneer een fout optreedt, probeert de server eerst de waarde van `ImageRendering::attribute::ErrorImage`te interpreteren als een eenvoudig pad naar een afbeeldingsbestand. Als het bestand niet kan worden geopend, worden de kenmerkwaarde en de foutdetails naar Image Serving verzonden, die zoals beschreven in `ImageServing::attribute::ErrorImage` verwerkt. Als Image Serving geen geldige reactieafbeelding retourneert, worden de standaard HTTP-foutstatus en het tekstbericht naar de client verzonden.

Foutafbeeldingen worden geretourneerd met HTTP-status 200.

## Eigenschappen {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Tekstreeks. Indien opgegeven, moet het ofwel een **`ImageServing::catalog::id`**-waarde zijn, een relatief pad (naar **`ImageServing::attribute::RootPath`** of **`ImageRendering::attribute::RootPath`**) of een absoluut pad naar een afbeeldingsbestand dat toegankelijk is voor de Image Server.

## Standaard {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Overgenomen van `default::ErrorImage` als deze niet is gedefinieerd. Als het wordt bepaald maar leeg, is het gedrag van het foutenbeeld gehandicapt, zelfs als `default::ErrorImage` wordt bepaald, en een de foutenstatus van HTTP is teruggekeerd.

## Zie ook {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3),  [catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
