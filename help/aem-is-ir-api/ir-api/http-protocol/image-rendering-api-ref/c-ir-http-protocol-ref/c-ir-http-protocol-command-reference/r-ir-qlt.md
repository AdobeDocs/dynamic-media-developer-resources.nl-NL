---
description: JPEG-kwaliteit. Hiermee geeft u JPEG-coderingskenmerken op om het compressieniveau te bepalen.
seo-description: JPEG-kwaliteit. Hiermee geeft u JPEG-coderingskenmerken op om het compressieniveau te bepalen.
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Scene7 Image Serving - Image Rendering API
uuid: 46f5b0da-7fe7-4daf-947b-bb5f5f5f5e6d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# qlt{#qlt}

JPEG-kwaliteit. Hiermee geeft u JPEG-coderingskenmerken op om het compressieniveau te bepalen.

` qlt= *``*[. *`kwalitatief chroma`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> kwaliteit </span> </p> </td> 
  <td class="stentry"> <p>JPEG-coderingskwaliteit (1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> chroma </span> </p> </td> 
  <td class="stentry"> <p>downsampling van JPEG-chromaticiteit (0=normaal, 1=uitgeschakeld); optioneel, standaard is 0. </p> </td> 
 </tr> 
</table>

Hiermee geeft u JPEG-coderingskenmerken op om het compressieniveau te bepalen. Dit varieert op zijn beurt de bestandsgrootte (de hoeveelheid antwoordgegevens) en indirect de visuele kwaliteit van de resulterende afbeelding.

Bij hogere *`quality`* waarden neemt de bestandsgrootte en kwaliteit toe, bij lagere waarden neemt de bestandsgrootte af en neemt de waargenomen afbeeldingskwaliteit af. Met waarden boven 90 worden vaak afbeeldingen gegenereerd die niet van de ongecomprimeerde afbeelding zijn te onderscheiden.

Stel de *`chroma`* markering zo in dat de kleurverkleining van typische JPEG-codeermodules wordt uitgeschakeld. Hierdoor kan de waargenomen scherpte van de randen in een afbeelding toenemen wanneer de rand wordt gedefinieerd door een wijziging in kleurtoon in plaats van helderheid. Als u deze markering instelt, kan de bestandsgrootte enigszins toenemen. Experimenteer met deze instelling als de tekst iets vaag lijkt.

## Eigenschappen {#section-897b61c786dd4230a2c5807f2f40e722}

Kan overal in het verzoek voorkomen.

Genegeerd als de indeling van de uitvoerafbeelding JPEG-compressie niet ondersteunt. Zie de beschrijving van `fmt=` voor een lijst met uitvoerafbeeldingsindelingen die JPEG-compressie ondersteunen.

## Standaard {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## Zie ook {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [kenmerk::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
