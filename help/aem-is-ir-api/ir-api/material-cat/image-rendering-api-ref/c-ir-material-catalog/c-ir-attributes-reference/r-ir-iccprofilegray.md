---
title: IccProfileGray
description: Standaardkleurruimte voor grijswaarden. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor grijswaardenresponsafbeeldingen wanneer er geen uitvoerkleurruimte is opgegeven met icc=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 21f37090-a68c-4d86-a807-bda243a8f99e
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# IccProfileGray{#iccprofilegray}

Standaardkleurruimte voor grijswaarden. Hiermee wordt de naam opgegeven van het ICC-kleurprofiel dat moet worden gebruikt voor grijswaardenresponsafbeeldingen wanneer er geen uitvoerkleurruimte is opgegeven met `icc=`.

## Eigenschappen {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

Tekstreeks. Indien opgegeven, moet dit een geldige waarde zijn `icc::Name` waarde in de ICC-profielkaart van deze materiaalcatalogus of de standaardcatalogus, of een bestandspad dat relatief is ten opzichte van `attribute::RootPath`. Het ICC-profiel waarnaar wordt verwezen, moet een grijswaardenprofiel zijn.

## Standaard {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

Overgenomen van `default::IccProfileGray` indien niet gedefinieerd of leeg.

## Zie ook {#section-cd43189611f4426aacddcc604eb02a10}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [kenmerk:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [kenmerk::IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2), [kenmerk::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
