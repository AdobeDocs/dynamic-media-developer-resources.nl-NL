---
description: RGB standaarduitvoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor RGB-responafbeeldingen als er geen uitvoerkleurruimte is opgegeven met icc= en voor bepaalde RGB-kleurwaarden die zijn opgegeven met diverse opdrachten voor afbeeldingsservers, zoals color=.
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 861c7b54-6d18-47c8-a08d-970f29b63962
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---

# IccProfileRgb{#iccprofilergb}

RGB standaarduitvoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor RGB-responafbeeldingen als er geen uitvoerkleurruimte is opgegeven met icc= en voor bepaalde RGB-kleurwaarden die zijn opgegeven met diverse opdrachten voor afbeeldingsservers, zoals color=.

## Eigenschappen {#section-3dd55c954d4d4ad4bb715ed7cee31025}

Tekstreeks. Indien opgegeven, moet dit een geldige `icc::Name`-waarde zijn uit de ICC-profieltoewijzing van deze afbeeldingscatalogus of de standaardcatalogus, of een bestandspad ten opzichte van `attribute::RootPath`. Het ICC-profiel waarnaar wordt verwezen, moet een RGB-profiel zijn.

## Standaard {#section-dfe08dd7b851453ca816623a4179955b}

Overgenomen van `default::IccProfileRgb` indien niet gedefinieerd of indien leeg.

## Zie ook {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
