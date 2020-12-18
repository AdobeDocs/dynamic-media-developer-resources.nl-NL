---
description: CMYK-standaarduitvoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor CMYK-responafbeeldingen als er geen uitvoerkleurruimte is opgegeven met icc= en voor bepaalde CMYK-kleurwaarden die zijn opgegeven met diverse opdrachten voor afbeeldingsservers, zoals color=.
seo-description: CMYK-standaarduitvoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor CMYK-responafbeeldingen als er geen uitvoerkleurruimte is opgegeven met icc= en voor bepaalde CMYK-kleurwaarden die zijn opgegeven met diverse opdrachten voor afbeeldingsservers, zoals color=.
seo-title: IccProfileCmyk
solution: Experience Manager
title: IccProfileCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: b22b6ed1-615f-4241-b4d4-c3aa70351458
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---


# IccProfileCmyk{#iccprofilecmyk}

CMYK-standaarduitvoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor CMYK-responafbeeldingen als er geen uitvoerkleurruimte is opgegeven met icc= en voor bepaalde CMYK-kleurwaarden die zijn opgegeven met diverse opdrachten voor afbeeldingsservers, zoals color=.

## Eigenschappen {#section-d8b6102cc1c744d482f99808ccfcaa24}

Tekstreeks. Indien opgegeven, moet dit een geldige `icc::Name`-waarde zijn uit de ICC-profieltoewijzing van deze afbeeldingscatalogus of de standaardcatalogus, of een bestandspad ten opzichte van `attribute::RootPath`. Het ICC-profiel waarnaar wordt verwezen, moet een CMYK-profiel zijn.

## Standaard {#section-62442df09a724950bfbdd0640b3e6678}

Overgenomen van `default::IccProfileCmyk` indien niet gedefinieerd of indien leeg.

## Zie ook {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
