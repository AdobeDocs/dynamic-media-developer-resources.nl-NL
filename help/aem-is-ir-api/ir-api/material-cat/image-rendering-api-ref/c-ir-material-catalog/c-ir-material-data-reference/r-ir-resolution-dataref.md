---
description: Resolutie. De "real-world"beeldresolutie, typisch uitgedrukt als pixel per duim, maar kan ook in andere eenheden, zoals pixel per meter zijn.
seo-description: Resolutie. De "real-world"beeldresolutie, typisch uitgedrukt als pixel per duim, maar kan ook in andere eenheden, zoals pixel per meter zijn.
seo-title: Resolutie
solution: Experience Manager
title: Resolutie
topic: Scene7 Image Serving - Image Rendering API
uuid: 281c7ff6-8f78-4654-98ec-0db4299b80d9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# Resolutie{#resolution}

Resolutie. De &quot;real-world&quot;beeldresolutie, typisch uitgedrukt als pixel per duim, maar kan ook in andere eenheden, zoals pixel per meter zijn.

## Eigenschappen {#section-985ca2ad858c4e9c9cbb303f55447553}

Reëel getal, groter dan 0. Vereist voor structuur- en decal-materialen, tenzij de afbeeldingsresolutie gelijk is aan het kenmerk:Resolution. Genegeerd door effen kleuren en kastmaterialen.

## Standaard {#section-b1d044e211194242a900aaef4a8c8e6f}

`attribute::Resolution` wordt gebruikt als het veld niet aanwezig is, als de waarde 0 of negatief is of als het veld leeg is.

## Zie ook {#section-2d04df523d7345f6929178cbc637da78}

[kenmerk::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) ,  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
