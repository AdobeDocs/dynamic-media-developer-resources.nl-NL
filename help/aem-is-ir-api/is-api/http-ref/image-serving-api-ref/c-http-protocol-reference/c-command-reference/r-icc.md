---
description: Uitvoerkleurprofiel.
seo-description: Uitvoerkleurprofiel.
seo-title: icc
solution: Experience Manager
title: icc
topic: Scene7 Image Serving - Image Rendering API
uuid: cfbd18aa-cbba-4085-920d-1f54645d0f89
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# icc{#icc}

Uitvoerkleurprofiel.

`icc= *``*[, *``*[, *``*[, *`objectrenderIntentblackpointCompdither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> object</span></span> </p></td> 
  <td class="stentry"> <p>ICC-kleurprofiel. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> perceptueel|relatief|verzadiging|absoluut</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1 om, 0 toe te laten om zwartpuntcompensatie onbruikbaar te maken. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> dithering</span></span> </p></td> 
  <td class="stentry"> <p>1 om dithering in te schakelen, 0 om dithering uit te schakelen. </p></td> 
 </tr> 
</table>

*`object`* Hiermee geeft u het kleurruimteprofiel van de uitvoer op waarnaar de afbeelding moet worden geconverteerd als deze afwijkt van het werkprofiel. *`profile`* moet een geldig `icc::Name` gedefinieerd pad zijn in de ICC-profielkaart van een afbeeldingscatalogus of standaardcatalogus, of een relatief pad naar een profielbestand (meestal met [!DNL .icc] of [!DNL .icm] achtervoegsel). Zie [ voor meer informatie *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

>[!NOTE]
>
>*`object`* mag geen &#39;,&#39;-tekens bevatten, zelfs niet als deze met HTTP zijn gecodeerd.

*`renderIntent`* Hiermee kunt u de standaard rendering intent overschrijven.

*`blackpointComp`* maakt compensatie van zwartpunten mogelijk als het uitvoerprofiel deze functie ondersteunt.

>[!NOTE]
>
>Niet alle kleurconversies ondersteunen alle *`renderIntent`* en *`blackpointComp`* keuzen. Doorgaans worden deze instellingen alleen ondersteund wanneer het ICC-uitvoerprofiel een uitvoerapparaat zoals een printer of monitor karakteriseert. Sommige ICC-uitvoerprofielen bieden ook geen ondersteuning voor alle *`renderIntent`* opties.

Opmerking

*`dither`* maakt dithering mogelijk (werkelijke foutdiffusie), waardoor kleurstreepvorming-artefacten worden voorkomen of verminderd.

## Eigenschappen {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

Request-kenmerk. De server retourneert een fout als een afbeeldingstype is opgegeven `fmt=` dat niet overeenkomt *`profile`*.

*`renderIntent`* en *`blackpointComp`* worden genegeerd als deze niet compatibel zijn met het opgegeven ICC-profiel. CMYK-uitvoerapparaatprofielen bieden meestal ondersteuning voor verschillende render-intenties.

## Standaard {#section-0b9fe2eb428447df8ae9948f11ab5aae}

Als kleurbeheer is ingeschakeld en niet `icc=` is opgegeven, levert de server de afbeelding die is omgezet in het uitvoerprofiel ( `attribute::IccProfile*`) dat overeenkomt met het afbeeldingstype dat met `fmt=`.

Als gespecificeerd niet, *`renderIntent`* wordt geërft van `attribute::IccRenderIntent`, *`blackpointComp`* wordt geërft van `attribute::IccBlackPointCompensation`, en *`dither`* wordt geërft van `attribute::IccDither`.

## Zie ook {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[kenmerk::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) , [kenmerk::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [kenmerk::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)[object,Color Management, attribuutICC Profile Map ReferencePiccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
