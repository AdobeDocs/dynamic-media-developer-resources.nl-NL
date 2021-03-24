---
description: Afbeeldingsanker. Hiermee geeft u het ankerpunt (hotspot) van een herhaalbare structuur, wandrand of decimale afbeelding op.
solution: Experience Manager
title: Anker
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---


# Anker{#anchor}

Afbeeldingsanker. Hiermee geeft u het ankerpunt (hotspot) van een herhaalbare structuur, wandrand of decimale afbeelding op.

Er wordt een herhaalbare structuur toegepast op een vignetobject, zodat het structuurankerpunt zich op het oorsprongpunt van de structuur van het object bevindt. Er wordt een decimale afbeelding toegepast op een vignetobject, zodat het decale ankerpunt zich op het decimale oorsprongpunt van het object bevindt. Voor wandranden wordt alleen de x-waarde gebruikt; de y-waarde wordt genegeerd.

## Eigenschappen {#section-bc4bc8b897c64535b88681e57d72942f}

Twee gehele getallen, gescheiden door een komma. Pixelverschuiving ten opzichte van de linkerbovenhoek van de afbeelding. Genegeerd als `catalog::Alignment=3` en door effen kleur en kast materiaal.

## Standaard {#section-b7ccc419a356415294706cd295ae96c9}

Als het veld leeg is of niet aanwezig is, wordt de linkerbovenhoek (0,0) van de afbeelding voor herhaalbare structuurmaterialen gebruikt, of het midden van de afbeelding voor decimale materialen.

## Zie ook {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[catalogus::Uitlijning](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [anker=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
