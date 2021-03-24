---
description: Pad naar brongegevenstramien. Tekstreeks. Absoluut pad of relatief padsegment voor de hoofdmap voor alle vignet-, structuur-, afbeeldings- en ICC-gegevensbestanden waarnaar in deze afbeeldingscatalogus wordt verwezen.
solution: Experience Manager
title: RootPath *
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# RootPath *{#rootpath}

Pad naar brongegevenstramien. Tekstreeks. Absoluut pad of relatief padsegment voor de hoofdmap voor alle vignet-, structuur-, afbeeldings- en ICC-gegevensbestanden waarnaar in deze afbeeldingscatalogus wordt verwezen.

## Eigenschappen {#section-5ff1cf592dd24dfc8cfa470c753ab828}

Tekstreeks. Moet leeg zijn, een geldig padsegment relatief ten opzichte van de configuratie-instelling `ir.resourceRootPaths` van de server voor het renderen van afbeeldingen, of een geldig absoluut bestandspad. Dient geen scheidingstekens voor regelafstandelementen en volgelementen te bevatten.

## Standaard {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

Overgenomen van `default::RootPath` indien niet gedefinieerd. Als deze wel gedefinieerd maar leeg zijn, wordt dit niet gebruikt voor het hoofdpad van het bronbestand.

## Zie ook {#section-92012cc1ce32448ea977e7e0484857e2}

[catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) ,  [catalog::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969),  `ir.resourceRootPaths`
