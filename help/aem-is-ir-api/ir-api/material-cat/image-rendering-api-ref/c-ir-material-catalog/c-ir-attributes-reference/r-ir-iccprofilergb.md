---
description: RGB standaarduitvoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor RGB-responafbeeldingen als er geen uitvoerkleurruimte is opgegeven met icc= en voor bepaalde RGB-kleurwaarden die zijn opgegeven met diverse opdrachten voor het renderen van afbeeldingen, zoals bgc= en color=.
seo-description: RGB standaarduitvoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor RGB-responafbeeldingen als er geen uitvoerkleurruimte is opgegeven met icc= en voor bepaalde RGB-kleurwaarden die zijn opgegeven met diverse opdrachten voor het renderen van afbeeldingen, zoals bgc= en color=.
seo-title: IccProfileRgb
solution: Experience Manager
title: IccProfileRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 0fe63607-c328-468a-aa55-0c4d16cf9f0f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---


# IccProfileRgb{#iccprofilergb}

RGB standaarduitvoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor RGB-responafbeeldingen als er geen uitvoerkleurruimte is opgegeven met icc= en voor bepaalde RGB-kleurwaarden die zijn opgegeven met diverse opdrachten voor het renderen van afbeeldingen, zoals bgc= en color=.

## Eigenschappen {#section-b4a1bd92e99047479a5036413525a6d9}

Tekstreeks. Indien opgegeven, moet dit een geldige `icc::Name`-waarde zijn uit de ICC-profielkaart van deze materiaalcatalogus of de standaardcatalogus, of een bestandspad ten opzichte van `attribute::RootPath`. Het ICC-profiel waarnaar wordt verwezen, moet een RGB-profiel zijn.

## Standaard {#section-5809772f8e96438ab7626d323c66a4ba}

Overgenomen van `default::IccProfileRgb` indien niet gedefinieerd of indien leeg.

## Zie ook {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
