---
description: CMYK-standaardkleurruimte. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor grijswaardenresponsafbeeldingen wanneer er geen uitvoerkleurruimte is opgegeven met icc=.
seo-description: CMYK-standaardkleurruimte. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor grijswaardenresponsafbeeldingen wanneer er geen uitvoerkleurruimte is opgegeven met icc=.
seo-title: IccProfileCmyk
solution: Experience Manager
title: IccProfileCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: d923d0fd-f00b-4fce-8ce9-8b177b4dba96
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileCmyk{#iccprofilecmyk}

CMYK-standaardkleurruimte. Hiermee geeft u de naam op van het ICC-kleurprofiel dat moet worden gebruikt voor grijswaardenresponsafbeeldingen wanneer er geen uitvoerkleurruimte is opgegeven met icc=.

## Eigenschappen {#section-849678b272954bdcb236f49aa54f1609}

Tekstreeks. Indien opgegeven, moet dit een geldige `icc::Name` waarde zijn uit de ICC-profielkaart van deze afbeeldingscatalogus of de standaardcatalogus, of een bestandspad dat relatief is ten opzichte van `attribute::RootPath`. Het ICC-profiel waarnaar wordt verwezen, moet een CMYK-profiel zijn.

## Standaard {#section-55026b7454af4d868bcb47f7743c9c5b}

Overgenomen van `default::IccProfileCmyk` indien niet gedefinieerd of indien leeg.

## Zie ook {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
