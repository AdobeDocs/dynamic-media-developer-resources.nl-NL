---
description: Standaardinvoerkleurprofiel voor grijswaarden. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor grijswaardenafbeeldingen die geen kleurprofiel insluiten.
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 8c89f0bb-4912-4838-a9e2-fb5d2f255eae
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---

# IccProfileSrcGray{#iccprofilesrcgray}

Standaardinvoerkleurprofiel voor grijswaarden. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor grijswaardenafbeeldingen die geen kleurprofiel insluiten.

## Eigenschappen {#section-97923d8561b845309442d57d017d91a4}

Tekstreeks. Indien opgegeven, moet dit een geldige `icc::Name`-waarde zijn uit de ICC-profieltoewijzing van deze afbeeldingscatalogus of de standaardcatalogus, of een bestandspad ten opzichte van `attribute::RootPath`. Het ICC-profiel waarnaar wordt verwezen, moet een grijswaardenprofiel zijn.

## Standaard {#section-02c52805ee13483dba7878aeab51f889}

Overgenomen van `default::IccProfileSrcGray` indien niet gedefinieerd of indien leeg. Als `attribute::IccProfileSrcGray` niet wordt omgezet in een geldig profiel, wordt `attribute::IccProfileGray` gebruikt.

## Zie ook {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
