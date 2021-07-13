---
description: RGB standaard invoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor RGB-materiaalafbeeldingen en -vignetten die geen kleurprofiel insluiten en voor RGB-kleurwaarden die zijn opgegeven met verschillende opdrachten voor het renderen van afbeeldingen, zoals bgc= en color=.
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB standaard invoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor RGB-materiaalafbeeldingen en -vignetten die geen kleurprofiel insluiten en voor RGB-kleurwaarden die zijn opgegeven met verschillende opdrachten voor het renderen van afbeeldingen, zoals bgc= en color=.

## Eigenschappen {#section-c22966bba03e43c08e9d3fb91bfdd465}

Tekstreeks. Indien opgegeven, moet dit een geldige `icc::Name`-waarde zijn uit de ICC-profieltoewijzing van deze afbeeldingscatalogus of de standaardcatalogus, of een bestandspad ten opzichte van `attribute::RootPath`. Het ICC-profiel waarnaar wordt verwezen, moet een RGB-profiel zijn.

## Standaard {#section-0171cd6680284bfa9844b9cc3644ca61}

Overgenomen van `default::IccProfileSrcRgb` indien niet gedefinieerd of indien leeg. Als `attribute::IccProfileSrcRgb` niet wordt omgezet in een geldig profiel, wordt `attribute::IccProfileRgb` in plaats daarvan gebruikt.

## Zie ook {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
