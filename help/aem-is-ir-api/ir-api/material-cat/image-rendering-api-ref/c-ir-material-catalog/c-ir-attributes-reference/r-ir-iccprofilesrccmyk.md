---
title: IccProfileSrcCmyk
description: Standaard CMYK-invoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor CMYK-materiaalafbeeldingen die geen kleurprofiel insluiten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 09be34c8-facc-40c3-ba15-c48bd93b3be1
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

Standaard CMYK-invoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor CMYK-materiaalafbeeldingen die geen kleurprofiel insluiten.

## Eigenschappen {#section-0cee77438d914c319ec876edb3490821}

Tekstreeks. Indien opgegeven, moet dit een geldige waarde zijn `icc::Name` waarde in de ICC-profielkaart van deze afbeeldingscatalogus of de standaardcatalogus, of een bestandspad dat relatief is ten opzichte van `attribute::RootPath`. Het ICC-profiel waarnaar wordt verwezen, moet een CMYK-profiel zijn.

## Standaard {#section-11f6239e0dd14827abf4a95c1b30161c}

Overgenomen van `default::IccProfileSrcCmyk` indien niet gedefinieerd of leeg. Indien `attribute::IccProfileSrcCmyk` niet wordt omgezet in een geldig profiel, `attribute::IccProfileCmyk` wordt in plaats daarvan gebruikt.

## Zie ook {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [kenmerk:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [kenmerk::IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [kenmerk::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
