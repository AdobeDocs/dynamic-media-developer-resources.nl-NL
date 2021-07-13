---
description: Standaard kleurenprofiel voor grijswaarden. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor grijswaardenresponsafbeeldingen wanneer er geen uitvoerkleurruimte is opgegeven met icc= en voor bepaalde grijswaardenwaarden die zijn opgegeven met diverse opdrachten voor afbeeldingsservers, zoals color=.
solution: Experience Manager
title: IccProfileGray
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 4964c3b3-799d-40cb-bc5f-d08acfd41ed9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---

# IccProfileGray{#iccprofilegray}

Standaard kleurenprofiel voor grijswaarden. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor grijswaardenresponsafbeeldingen wanneer er geen uitvoerkleurruimte is opgegeven met icc= en voor bepaalde grijswaardenwaarden die zijn opgegeven met diverse opdrachten voor afbeeldingsservers, zoals color=.

## Eigenschappen {#section-03f090ee2acf4537b83f78840d23ecab}

Tekstreeks. Indien opgegeven, moet dit een geldige `icc::Name`-waarde zijn uit de ICC-profieltoewijzing van deze afbeeldingscatalogus of de standaardcatalogus, of een bestandspad ten opzichte van `attribute::RootPath`. Het ICC-profiel waarnaar wordt verwezen, moet een grijswaardenprofiel zijn.

## Standaard {#section-95ba3ab15edc4259b657c6ebf8783d61}

Overgenomen van `default::IccProfileGray` indien niet gedefinieerd of indien leeg.

## Zie ook {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
