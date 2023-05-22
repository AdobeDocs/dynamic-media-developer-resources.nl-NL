---
description: Uitvoerkleurprofiel.
solution: Experience Manager
title: icc
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8be7be8c-a23d-4a5b-93e4-44231155616b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# icc{#icc}

Uitvoerkleurprofiel.

`icc= *`object`*[, *`renderIntent`*[, *`blackpointComp`*[, *`dithering`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> object</span> </span> </p></td> 
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

*`object`* Hiermee geeft u het kleurruimteprofiel van de uitvoer op waarnaar de afbeelding moet worden geconverteerd als deze afwijkt van het werkprofiel. *`profile`* moet geldig zijn `icc::Name` gedefinieerd in de ICC-profielkaart van een afbeeldingscatalogus of standaardcatalogus, of een relatief pad naar een profielbestand (meestal met [!DNL .icc] of [!DNL .icm] achtervoegsel). Zie [ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)voor aanvullende informatie.

>[!NOTE]
>
>*`object`* mag geen &#39;,&#39;-tekens bevatten, zelfs niet als deze met HTTP zijn gecodeerd.

*`renderIntent`* Hiermee kunt u de standaard rendering intent overschrijven.

*`blackpointComp`* maakt compensatie van zwartpunten mogelijk als het uitvoerprofiel deze functie ondersteunt.

>[!NOTE]
>
>Niet alle kleurconversies ondersteunen alle kleuren *`renderIntent`* en *`blackpointComp`* keuzen. Doorgaans worden deze instellingen alleen ondersteund wanneer het ICC-uitvoerprofiel een uitvoerapparaat zoals een printer of monitor karakteriseert. Sommige ICC-uitvoerprofielen bieden ook geen ondersteuning voor alle profielen *`renderIntent`* keuzen.

Opmerking

*`dither`* maakt dithering mogelijk (werkelijke foutdiffusie), waardoor kleurstreepvorming-artefacten worden voorkomen of verminderd.

## Eigenschappen {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

Request-kenmerk. De server retourneert een fout als een afbeeldingstype is opgegeven met `fmt=` die niet overeenkomen *`profile`*.

*`renderIntent`* en *`blackpointComp`* worden genegeerd als dit niet compatibel is met het opgegeven ICC-profiel. CMYK-uitvoerapparaatprofielen bieden meestal ondersteuning voor verschillende render-intenties.

## Standaard {#section-0b9fe2eb428447df8ae9948f11ab5aae}

Als kleurbeheer is ingeschakeld en `icc=` niet is opgegeven, levert de server de afbeelding die naar het uitvoerprofiel is geconverteerd ( `attribute::IccProfile*`) die overeenkomen met het afbeeldingstype dat is opgegeven met `fmt=`.

Indien niet opgegeven, *`renderIntent`* wordt overgeërfd van `attribute::IccRenderIntent`, *`blackpointComp`* wordt overgeërfd van `attribute::IccBlackPointCompensation`, en *`dither`* wordt overgeërfd van `attribute::IccDither`.

## Zie ook {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[kenmerk::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) , [kenmerk:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [kenmerk::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [kenmerk::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Kleurbeheer](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7), [ICC Profile Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
