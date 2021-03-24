---
description: RGB standaard invoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor RGB-bronafbeeldingen die geen kleurprofiel insluiten en voor bepaalde RGB-kleurwaarden die zijn opgegeven met verschillende opdrachten voor afbeeldingsservers, zoals color=.
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB standaard invoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor RGB-bronafbeeldingen die geen kleurprofiel insluiten en voor bepaalde RGB-kleurwaarden die zijn opgegeven met verschillende opdrachten voor afbeeldingsservers, zoals color=.

## Eigenschappen {#section-3cd753196959462e9e674dab0b033d08}

Tekstreeks. Indien opgegeven, moet dit een geldige `icc::Name`-waarde zijn uit de ICC-profieltoewijzing van deze afbeeldingscatalogus of de standaardcatalogus, of een bestandspad ten opzichte van `attribute::RootPath`. Het ICC-profiel waarnaar wordt verwezen, moet een RGB-profiel zijn.

## Standaard {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

Overgenomen van `default::IccProfileSrcRgb` indien niet gedefinieerd of indien leeg. Als `attribute::IccProfileSrcRgb` niet wordt omgezet in een geldig profiel, wordt `attribute::IccProfileRgb` in plaats daarvan gebruikt.

## Zie ook {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
