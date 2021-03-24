---
description: Standaard CMYK-invoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor CMYK-materiaalafbeeldingen die geen kleurprofiel insluiten.
solution: Experience Manager
title: IccProfileSrcCmyk
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

Standaard CMYK-invoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor CMYK-materiaalafbeeldingen die geen kleurprofiel insluiten.

## Eigenschappen {#section-0cee77438d914c319ec876edb3490821}

Tekstreeks. Indien opgegeven, moet dit een geldige `icc::Name`-waarde zijn uit de ICC-profieltoewijzing van deze afbeeldingscatalogus of de standaardcatalogus, of een bestandspad ten opzichte van `attribute::RootPath`. Het ICC-profiel waarnaar wordt verwezen, moet een CMYK-profiel zijn.

## Standaard {#section-11f6239e0dd14827abf4a95c1b30161c}

Overgenomen van `default::IccProfileSrcCmyk` indien niet gedefinieerd of indien leeg. Als `attribute::IccProfileSrcCmyk` niet wordt omgezet in een geldig profiel, wordt `attribute::IccProfileCmyk` gebruikt.

## Zie ook {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
