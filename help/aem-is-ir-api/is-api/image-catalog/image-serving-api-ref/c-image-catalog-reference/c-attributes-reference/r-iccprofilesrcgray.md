---
description: Standaardinvoerkleurprofiel voor grijswaarden. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor bronafbeeldingen in grijswaarden die geen kleurprofiel insluiten, en voor bepaalde kleurwaarden in grijswaarden die zijn opgegeven met diverse opdrachten in de afbeeldingsserver, zoals color=.
seo-description: Standaardinvoerkleurprofiel voor grijswaarden. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor bronafbeeldingen in grijswaarden die geen kleurprofiel insluiten, en voor bepaalde kleurwaarden in grijswaarden die zijn opgegeven met diverse opdrachten in de afbeeldingsserver, zoals color=.
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
uuid: 823c0e33-8bb7-4754-81cf-61a5ed6f45ce
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---


# IccProfileSrcGray{#iccprofilesrcgray}

Standaardinvoerkleurprofiel voor grijswaarden. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor bronafbeeldingen in grijswaarden die geen kleurprofiel insluiten, en voor bepaalde kleurwaarden in grijswaarden die zijn opgegeven met diverse opdrachten in de afbeeldingsserver, zoals color=.

## Eigenschappen {#section-8cbb316df6eb463aaca7b308d3568086}

Tekstreeks. Indien opgegeven, moet dit een geldige `icc::Name`-waarde zijn uit de ICC-profieltoewijzing van deze afbeeldingscatalogus of de standaardcatalogus, of een bestandspad ten opzichte van `attribute::RootPath`. Het ICC-profiel waarnaar wordt verwezen, moet een grijswaardenprofiel zijn.

## Standaard {#section-bcc7250715884412bd0780f60d1cce7b}

Overgenomen van `default::IccProfileSrcGray` indien niet gedefinieerd of indien leeg. Als `attribute::IccProfileSrcGray` niet wordt omgezet in een geldig profiel, wordt `attribute::IccProfileGray` in plaats daarvan gebruikt.

## Zie ook {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
