---
title: Kleurbeheer van afbeeldingsserver
description: Image Serving ondersteunt kleurruimteconversies op basis van kleurruimteprofielen die voldoen aan de ICC-specificatie (International Color Consortium).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1202'
ht-degree: 1%

---

# Kleurbeheer van afbeeldingsserver{#image-serving-color-management}

Image Serving ondersteunt kleurruimteconversies op basis van kleurruimteprofielen die voldoen aan de ICC-specificatie (International Color Consortium).

## Standaardkleurruimten {#section-8cfe60808bce49968091995e4e521dba}

Elke afbeeldingscatalogus (en de standaardcatalogus) kunnen een set ICC-profielen definiëren die de standaardkleurruimten voor deze catalogus vormen: één invoer- en één uitvoerprofiel voor grijswaarden-, RGB- en CMYK-gegevens. Zie
[kenmerk::IccProfileRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md)
[kenmerk::IccProfileGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md)
[kenmerk::IccProfileCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md)
[kenmerk::IccProfileSrcRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md)
[kenmerk::IccProfileSrcGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md)
[kenmerk::IccProfileSrcCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md).

## Invoerkleurruimte {#section-9f08e2c1b6aa4fe4815be174972c1944}

Bronafbeeldingen kunnen ICC-profielen insluiten om de invoerkleurruimte te definiëren. Als er geen profiel is ingesloten in een bronafbeelding, `attribute::IccProfileSrc*` van de toepasselijke afbeeldingscatalogus wordt gebruikt die overeenkomt met het pixeltype van de bronafbeelding. Als dit kenmerk niet is gedefinieerd in de afbeeldingscatalogus, `attribute::IccProfile*` wordt gebruikt. Als dat cataloguskenmerk ook niet is gedefinieerd, wordt de afbeelding niet in kleur beheerd en worden alleen naïeve transformaties toegepast.

## Uitvoerkleurruimte {#section-b517bca622b64dcfa7defba6035d0716}

De kleurruimte van het uiteindelijke afbeeldingsresultaat van een aanvraag wordt gedefinieerd met de `icc=` gebruiken. Indien `icc=` niet is opgegeven, wordt de standaarduitvoerkleurruimte (uit de hoofdcatalogus van de aanvraag) die overeenkomt met het pixeltype van de uitvoerafbeelding, gebruikt als de uitvoerkleurruimte. Als er geen uitvoerprofiel is gedefinieerd in de hoofd- of standaardcatalogus en als de basislaag een afbeelding is met een ingesloten profiel dat overeenkomt met het type uitvoerpixel, wordt dat profiel gebruikt voor de uitvoerkleurruimte. Anders blijft de uitvoerkleurruimte ongedefinieerd. Alleen naïeve kleuromzettingen worden toegepast bij het omzetten tussen pixeltypen en er kan geen kleurprofiel in de uitvoerafbeelding worden ingesloten.

De uitvoerkleurruimte van een geneste/ingesloten aanvraag voor het leveren van een afbeeldingsserver is altijd gelijk aan de uitvoerkleurruimte van het buitenste bestand, dat de aanvraag insluit.

## Effen kleuren {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

Kleurwaarden opgegeven met `color=`, `bgcolor=`of de RTF-opdracht `\iscolortbl` worden gekoppeld aan de invoerkleurruimte als de kleurwaarde het achtervoegsel &#39;S&#39; bevat. Als dit niet het geval is, worden de waarden gekoppeld aan de uitvoerkleurruimte. Kleurwaarden opgegeven met `bgc=` of de RTF-opdrachten `\colortbl` en `\cmykcolortbl` worden altijd gekoppeld aan de overeenkomende standaardkleurruimte of de werkelijke uitvoerkleurruimte.

>[!NOTE]
>
>Op dit moment `bgc=` neemt niet volledig deel aan kleurbeheer. Het achtervoegsel &#39;S&#39; wordt genegeerd wanneer het wordt opgegeven met `bgc=`en wordt de omzetting naïef uitgevoerd wanneer het pixeltype van de kleurwaarde die is opgegeven met `bgc=` verschilt van het pixeltype van de uitvoerafbeelding. Anders, `bgc=` wordt gekoppeld aan de werkelijke uitvoerkleurruimte.

## Geneste en ingesloten aanvragen {#section-bdda638c31504f26a77e51ebb1ea6e3b}

De uitvoerkleurruimte voor geneste IS-aanvragen en ingesloten AIR-verzoeken wordt automatisch ingesteld op de uitvoerkleurruimte van het buitenste verzoek, tenzij in het geneste verzoek een expliciete uitvoerkleurruimte wordt opgegeven met `icc=`. Bovendien nemen geneste/ingesloten aanvragen de standaardkleurruimten voor uitvoer over van de hoofdcatalogus van de buitenste aanvraag, zodat de waarden voor effen kleuren op consistente wijze worden verwerkt.

## Kleurruimte converteren {#section-ca87b80b8e364ea59d8a92d87121b0fb}

In afbeeldingsservers wordt doorgaans geprobeerd kleurconversies tijdens de verwerking uit te stellen. Als alle lagen van een afbeelding dezelfde laagkleurruimte hebben, vindt de omzetting in de uitvoerkleurruimte plaats na het samenvoegen en definitief schalen. Als het om meerdere laagkleurruimten gaat, wordt elke laag getransformeerd naar de uitvoerkleurruimte voordat deze wordt samengevoegd.

>[!NOTE]
>
>De opdrachten `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=`, en `op_saturation=` zijn RGB-bewerkingen. Bij deze bewerkingen blijft de kleurgetrouwheid alleen behouden als de kleurruimte van de laag een pixeltype van RGB heeft. Als u een andere kleur dan RGB gebruikt, worden de gegevens geconverteerd naar RGB met naïeve kleurconversie en heeft het resultaat een beperkte kleurgetrouwheid. De laagkleurruimte voor dergelijke lagen moet als onbepaald worden beschouwd.

Opties voor kleurconversie zijn beschikbaar bij `icc=` of, indien `icc=` is niet opgegeven, met `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation`, en `attribute::IccDither`.

## Kleurprofielen insluiten {#section-261ebbae5ce046589a776ca972380052}

Het ICC-kleurprofiel van de uitvoerkleurruimte kan, indien beschikbaar, worden ingesloten in de reactieafbeelding door `iccEmbed=`.

## ICC-profielen beheren {#section-eb210e4b44e64e2c8b80ee59216c5555}

Alle kleurprofielen die door de server worden gebruikt, moeten voldoen aan de ICC-specificatie. ICC-profielbestanden hebben doorgaans een [!DNL .icc] of [!DNL .icm] bestandsachtervoegsel en bevinden zich op dezelfde locatie als afbeeldingsgegevensbestanden.

Uitvoerprofielen kunnen worden opgegeven op bestandspad/-naam in het dialoogvenster `icc=` wordt aangeraden alle profielbestanden te registreren in de ICC-profielkaart van de standaardcatalogus of afbeeldingscatalogus en gebruik sneltoetsidentificatoren ( `icc::Name`) in plaats van bestandspaden.

Alle ICC-profielen waarnaar wordt verwezen in `catalog::IccProfile` en in `attribute::IccProfile*` moet zijn geregistreerd in de ICC-profielkaart van de afbeelding of standaardcatalogus.

## Beperkingen {#section-fb50ede40b124b89b30679da29782ab5}

Momenteel worden alleen CMYK-, RGB- en grijswaardenkleurruimten ondersteund.

## Opgenomen ICC-kleurprofielen {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

De meeste ICC-profielen voor Adobe van afbeeldingen worden opgenomen in de standaardafbeeldingscatalogus. Deze profielen zijn toegankelijk met de algemene namen (zoals in Photoshop) of met een iets kortere id. In de volgende tabel worden alle standaard-ICC-profielen weergegeven. Wanneer u naar een profiel in het dialoogvenster `icc=` gebruiken onder de algemene naam, moeten spaties als gecodeerd worden `%20`.

Er kunnen aanvullende profielen worden toegevoegd aan de standaardprofielen, hetzij aan de standaardcatalogus, hetzij aan een specifieke afbeeldingscatalogus. Zie de [ICC Profile Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) voor meer informatie.

>[!NOTE]
>
>De volgende tabel is van toepassing op *Dynamic Media Hybrid* alleen (wordt uitgevoerd in `dynamicmedia` uitvoeringsmodus).

| Id | Algemene naam | Bestandsnaam |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RGB | AppleRGB.icc |
| `CIERGB` | CIE RGB | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch RGB | ColorMatchRGB.icc |
| `NTSC` | NTSC (1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto` | ProPhoto RGB | ProPhoto.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | sRGB-kleurruimteprofiel.icm |
| `WideGamutRGB` | Brede kleuromvang RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | Coated FOGRA27 (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | Coated FOGRA39 (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `CoatedGraCol` | Coated GRACoL 2006 (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europe ISO Coated FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `EuroscaleCoated` | Euroscale Coated | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 Coated | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Japan Color 2002 Newspaper | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Uncoated | JapanColor2001Uncoated.icc |
| `JapanColorWebCoated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated (Ad) | JapanWebCoated.icc |
| `NewsprintSNAP2007` | US Newsprint (SNAP 2007) | USNewsprintSNAP2007.icc |
| `PS4Default` | Photoshop 4 standaard CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5 standaard CMYK | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | Uncoated FOGRA29 (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | Web Coated FOGRA28 (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `WebCoatedGrade3` | Web Coated SWOP 2006 Grade 3 Paper | WebCoatedSWOP2006Grade3.icc |
| `WebCoatedGrade5` | Web Coated SWOP 2006 Grade 5 Paper | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

De volgende tabel is van toepassing op *Dynamic Media Classic Image Serving* en *Dynamic Media* (wordt uitgevoerd in `dynamicmedia_scene7` uitvoeringsmodus).

| Id | Algemene naam | Bestandsnaam |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RGB | AppleRGB.icc |
| `CIERGB|CIE RGB` | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch RGB | ColorMatchRGB.icc |
| `NTSC` | NTSC (1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto RGB` | ProPhoto RGB | ProPhoto RGB.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | sRGB-kleurruimteprofiel.icm |
| `WideGamutRGB` | Brede kleuromvang RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | Coated FOGRA27 (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | Coated FOGRA39 (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `Coated GRACoL 2006 (ISO 12647-2:2004)` | Coated GRACoL 2006 (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europe ISO Coated FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `Euroscale Coated v2` | Euroscale Coated v2 | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 Coated | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Japan Color 2002 Newspaper | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Uncoated | JapanColor2001Uncoated.icc |
| `Japan Color 2003 Web Coated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated (Ad) | JapanWebCoated.icc |
| `PS4Default` | Photoshop 4 standaard CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5 standaard CMYK | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | Uncoated FOGRA29 (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `US Newsprint (SNAP 2007)` | US Newsprint (SNAP 2007) | USNewsprintSNAP2007.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | Web Coated FOGRA28 (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `Web Coated SWOP 2006 Grade 3 Paper` | Web Coated SWOP 2006 Grade 3 Paper | WebCoatedSWOP2006Grade3.icc |
| `Web Coated SWOP Grade 5 Paper` | Web Coated SWOP 2006 Grade 5 Paper | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

## Zie ook {#section-39159397e80b4efca5f631eab8b9aa06}

[Internationaal kleurconsortium](https://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [kenmerk::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)&#42;, [kenmerk::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)&#42;, [kenmerk:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [kenmerk::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [kenmerk::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [ICC Profile Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [*`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
