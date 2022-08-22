---
title: IccProfileSrcRgb
description: RGB standaard invoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor afbeeldingen van RGB-materiaal en vignetten die geen kleurprofiel insluiten. Ook voor RGB-kleurwaarden die zijn opgegeven met verschillende opdrachten voor het renderen van afbeeldingen, zoals bgc= en color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB standaard invoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor afbeeldingen van RGB-materiaal en vignetten die geen kleurprofiel insluiten. Ook voor RGB-kleurwaarden die zijn opgegeven met verschillende opdrachten voor het renderen van afbeeldingen, zoals `bgc=` en `color=`.

## Eigenschappen {#section-c22966bba03e43c08e9d3fb91bfdd465}

Tekstreeks. Indien opgegeven, moet dit een geldige waarde zijn `icc::Name` waarde in de ICC-profielkaart van deze afbeeldingscatalogus of de standaardcatalogus, of een bestandspad dat relatief is ten opzichte van `attribute::RootPath`. Het ICC-profiel waarnaar wordt verwezen, moet een RGB-profiel zijn.

## Standaard {#section-0171cd6680284bfa9844b9cc3644ca61}

Overgenomen van `default::IccProfileSrcRgb` indien niet gedefinieerd of leeg. Indien `attribute::IccProfileSrcRgb` niet wordt omgezet in een geldig profiel, `attribute::IccProfileRgb` wordt in plaats daarvan gebruikt.

## Zie ook {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [kenmerk:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [kenmerk::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30), [kenmerk::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
