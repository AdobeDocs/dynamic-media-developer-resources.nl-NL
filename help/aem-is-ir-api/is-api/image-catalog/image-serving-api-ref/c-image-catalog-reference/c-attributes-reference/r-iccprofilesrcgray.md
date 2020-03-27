---
description: Standaardinvoerkleurprofiel voor grijswaarden. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor bronafbeeldingen in grijswaarden die geen kleurprofiel insluiten en voor bepaalde kleurwaarden in grijswaarden die zijn opgegeven met diverse opdrachten in de afbeeldingsserver, zoals color=.
seo-description: Standaardinvoerkleurprofiel voor grijswaarden. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor bronafbeeldingen in grijswaarden die geen kleurprofiel insluiten en voor bepaalde kleurwaarden in grijswaarden die zijn opgegeven met diverse opdrachten in de afbeeldingsserver, zoals color=.
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
topic: Scene7 Image Serving - Image Rendering API
uuid: 823c0e33-8bb7-4754-81cf-61a5ed6f45ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcGray{#iccprofilesrcgray}

Standaardinvoerkleurprofiel voor grijswaarden. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor bronafbeeldingen in grijswaarden die geen kleurprofiel insluiten en voor bepaalde kleurwaarden in grijswaarden die zijn opgegeven met diverse opdrachten in de afbeeldingsserver, zoals color=.

## Eigenschappen {#section-8cbb316df6eb463aaca7b308d3568086}

Tekstreeks. Indien opgegeven, moet dit een geldige `icc::Name` waarde zijn uit de ICC-profielkaart van deze afbeeldingscatalogus of de standaardcatalogus, of een bestandspad dat relatief is ten opzichte van `attribute::RootPath`. Het ICC-profiel waarnaar wordt verwezen, moet een grijswaardenprofiel zijn.

## Standaard {#section-bcc7250715884412bd0780f60d1cce7b}

Overgenomen van `default::IccProfileSrcGray` indien niet gedefinieerd of indien leeg. Als de resolutie `attribute::IccProfileSrcGray` niet wordt omgezet naar een geldig profiel, wordt in plaats daarvan `attribute::IccProfileGray` gebruikt.

## Zie ook {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [kenmerk::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [kenmerk::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35), [kenmerk::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
