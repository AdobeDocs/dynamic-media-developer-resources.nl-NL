---
description: RGB standaard invoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor RGB-bronafbeeldingen die geen kleurprofiel insluiten en voor bepaalde RGB-kleurwaarden die zijn opgegeven met verschillende opdrachten voor afbeeldingsservers, zoals color=.
seo-description: RGB standaard invoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor RGB-bronafbeeldingen die geen kleurprofiel insluiten en voor bepaalde RGB-kleurwaarden die zijn opgegeven met verschillende opdrachten voor afbeeldingsservers, zoals color=.
seo-title: IccProfileSrcRgb
solution: Experience Manager
title: IccProfileSrcRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 4f6f19ec-3524-403e-9c79-1e2b25cd74ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB standaard invoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor RGB-bronafbeeldingen die geen kleurprofiel insluiten en voor bepaalde RGB-kleurwaarden die zijn opgegeven met verschillende opdrachten voor afbeeldingsservers, zoals color=.

## Eigenschappen {#section-3cd753196959462e9e674dab0b033d08}

Tekstreeks. Indien opgegeven, moet dit een geldige `icc::Name` waarde zijn uit de ICC-profielkaart van deze afbeeldingscatalogus of de standaardcatalogus, of een bestandspad dat relatief is ten opzichte van `attribute::RootPath`. Het ICC-profiel waarnaar wordt verwezen, moet een RGB-profiel zijn.

## Standaard {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

Overgenomen van `default::IccProfileSrcRgb` indien niet gedefinieerd of indien leeg. Als de resolutie `attribute::IccProfileSrcRgb` niet wordt omgezet naar een geldig profiel, wordt in plaats daarvan `attribute::IccProfileRgb` gebruikt.

## Zie ook {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
