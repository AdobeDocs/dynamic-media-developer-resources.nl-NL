---
description: Standaard CMYK-invoerkleurprofiel. Hiermee wordt de naam opgegeven van het ICC-kleurprofiel dat moet worden gebruikt voor CMYK-bronafbeeldingen die geen kleurprofiel insluiten en voor bepaalde CMYK-kleurwaarden die zijn opgegeven met diverse opdrachten voor afbeeldingsservice, zoals color=.
seo-description: Standaard CMYK-invoerkleurprofiel. Hiermee wordt de naam opgegeven van het ICC-kleurprofiel dat moet worden gebruikt voor CMYK-bronafbeeldingen die geen kleurprofiel insluiten en voor bepaalde CMYK-kleurwaarden die zijn opgegeven met diverse opdrachten voor afbeeldingsservice, zoals color=.
seo-title: IccProfileSrcCmyk
solution: Experience Manager
title: IccProfileSrcCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: 5f1c2eb6-7f32-4603-9587-d8c1f6a72bb0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

Standaard CMYK-invoerkleurprofiel. Hiermee wordt de naam opgegeven van het ICC-kleurprofiel dat moet worden gebruikt voor CMYK-bronafbeeldingen die geen kleurprofiel insluiten en voor bepaalde CMYK-kleurwaarden die zijn opgegeven met diverse opdrachten voor afbeeldingsservice, zoals color=.

## Eigenschappen {#section-fc2ad12a3c6e4c7cab495f1878638e66}

Tekstreeks. Indien opgegeven, moet dit een geldige `icc::Name`-waarde zijn uit de ICC-profieltoewijzing van deze afbeeldingscatalogus of de standaardcatalogus, of een bestandspad ten opzichte van `attribute::RootPath`. Het ICC-profiel waarnaar wordt verwezen, moet een CMYK-profiel zijn.

## Standaard {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

Overgenomen van `default::IccProfileSrcCmyk` indien niet gedefinieerd of indien leeg. Als `attribute::IccProfileSrcCmyk` niet wordt omgezet in een geldig profiel, wordt `attribute::IccProfileCmyk` in plaats daarvan gebruikt.

## Zie ook {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
