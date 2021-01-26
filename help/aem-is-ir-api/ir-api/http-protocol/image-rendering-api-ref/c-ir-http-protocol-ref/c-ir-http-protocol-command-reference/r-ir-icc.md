---
description: Kleurprofiel uitvoeren.
seo-description: Kleurprofiel uitvoeren.
seo-title: icc
solution: Experience Manager
title: icc
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 95a05fe5-d6b3-4118-aab4-4664ccee2850
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---


# icc{#icc}

Kleurprofiel uitvoeren.

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> profiel</span></span> </p></td> 
  <td class="stentry"> <p>ICC-kleurprofiel. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent  </span> </span> </p></td> 
  <td class="stentry"> <p>perceptueel | relatief | verzadiging | absoluut </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1 om, 0 toe te laten om zwartpuntcompensatie onbruikbaar te maken. </p></td> 
 </tr> 
</table>

*`profile`* Hiermee geeft u het kleurruimteprofiel van de uitvoer op waarnaar de gerenderde afbeelding moet worden geconverteerd als deze afwijkt van het werkprofiel. *`profile`* moet een geldig  `icc::Name` gedefinieerd pad zijn in de ICC-profielkaart van een afbeeldingscatalogus of standaardcatalogus, of een relatief pad naar een profielbestand (meestal met  [!DNL .icc]of  [!DNL .icm] achtervoegsel).

>[!NOTE]
>
>*`profile`* mag geen &#39;,&#39;-tekens bevatten, zelfs niet als deze met HTTP zijn gecodeerd.

*`renderIntent`* Hiermee kunt u de standaard rendering intent overschrijven.

*`blackpointComp`* maakt compensatie van zwartpunten mogelijk als het uitvoerprofiel deze functie ondersteunt.

>[!NOTE]
>
>Niet alle kleurconversies ondersteunen alle *`renderIntent`*- en *`blackpointComp`*-keuzen. Doorgaans worden deze instellingen alleen ondersteund wanneer het ICC-uitvoerprofiel een uitvoerapparaat zoals een printer of monitor karakteriseert. Sommige ICC-uitvoerprofielen bieden ook geen ondersteuning voor alle *`renderIntent`*-keuzen.

## Eigenschappen {#section-b4042623a8ea40248c11b2153e5906b1}

Kan overal binnen het verzoek voorkomen. Er wordt een fout geretourneerd als het afbeeldingstype niet overeenkomt met `fmt=`.*`profile`*

*`renderIntent`* en  *`blackpointComp`* worden genegeerd als deze niet compatibel zijn met het opgegeven ICC-profiel.

CMYK-uitvoerapparaatprofielen bieden meestal ondersteuning voor verschillende render-intenties.

## Standaard {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

Als kleurbeheer is ingeschakeld en `icc=` niet is opgegeven, levert de server de afbeelding die is omgezet in het uitvoerprofiel ( `attribute::IccProfile*`) dat overeenkomt met het afbeeldingstype dat is opgegeven met `fmt=`.

Indien niet opgegeven, wordt *`renderIntent`* overgeërfd van `attribute::IccRenderIntent`, en *`blackpointComp`* wordt overgeërfd van `attribute::IccBlackPointCompensation`.

## Zie ook {#section-37ef83149fd74345956a98f633cc0294}

[Kleurbeheer](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d),  [kenmerk::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127),  [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f),  [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [kenmerk::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [kenmerk::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
