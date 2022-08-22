---
title: IccProfileRgb
description: RGB standaard uitvoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor afbeeldingen met RGB-respons wanneer geen uitvoerkleurruimte is opgegeven met icc=. Ook voor bepaalde RGB-kleurwaarden die zijn opgegeven met verschillende opdrachten voor het renderen van afbeeldingen, zoals bgc= en color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4057e968-24de-41af-9901-a6cb5ed9ea63
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# IccProfileRgb{#iccprofilergb}

RGB standaard uitvoerkleurprofiel. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor RGB-responafbeeldingen als er geen uitvoerkleurruimte is opgegeven met `icc=`. Ook voor bepaalde RGB-kleurwaarden die zijn opgegeven met verschillende opdrachten voor het renderen van afbeeldingen, zoals `bgc=` en `color=`.

## Eigenschappen {#section-b4a1bd92e99047479a5036413525a6d9}

Tekstreeks. Indien opgegeven, moet dit een geldige waarde zijn `icc::Name` waarde in de ICC-profielkaart van deze materiaalcatalogus of de standaardcatalogus, of een bestandspad dat relatief is ten opzichte van `attribute::RootPath`. Het ICC-profiel waarnaar wordt verwezen, moet een RGB-profiel zijn.

## Standaard {#section-5809772f8e96438ab7626d323c66a4ba}

Overgenomen van `default::IccProfileRgb` indien niet gedefinieerd of leeg.

## Zie ook {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [kenmerk:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [kenmerk::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49), [kenmerk::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
