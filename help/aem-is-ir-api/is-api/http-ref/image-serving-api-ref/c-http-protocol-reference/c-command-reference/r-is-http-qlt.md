---
title: qlt
description: JPEG-kwaliteit. Hiermee geeft u JPEG-coderingskenmerken op om het compressieniveau te bepalen. Dit varieert op zijn beurt de bestandsgrootte (de hoeveelheid antwoordgegevens) en indirect de visuele kwaliteit van de resulterende afbeelding.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# qlt{#qlt}

JPEG-kwaliteit. Hiermee geeft u JPEG-coderingskenmerken op om het compressieniveau te bepalen. Dit varieert op zijn beurt de bestandsgrootte (de hoeveelheid antwoordgegevens) en indirect de visuele kwaliteit van de resulterende afbeelding.

` qlt= *`kwaliteit`*[, *`chroma`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> kwaliteit </span> </p> </td> 
  <td class="stentry"> <p>Coderingskwaliteit JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> chroma </span> </p> </td> 
  <td class="stentry"> <p>JPEG-chromaticiteitsdownsampling (0=normaal, 1=uitgeschakeld); optioneel, standaard is 0. </p> </td> 
 </tr> 
</table>

Hoger *`quality`* Als u waarden opgeeft, neemt de bestandsgrootte en kwaliteit toe, nemen lagere waarden toe en nemen de waargenomen beeldkwaliteit af. Met waarden boven 90 worden vaak afbeeldingen gegenereerd die niet van de ongecomprimeerde afbeelding zijn te onderscheiden.

Stel de *`chroma`* markering voor het uitschakelen van de downsampling van de RGB-kleurafwijking door typische JPEG-encoders. Hierdoor kan de waargenomen scherpte van de randen in een afbeelding toenemen wanneer de rand wordt gedefinieerd door een wijziging in kleurtoon in plaats van helderheid. Als u deze markering instelt, kan de bestandsgrootte enigszins toenemen. Experimenteer met deze instelling als de tekst iets vaag lijkt.

## Eigenschappen {#section-925a44cbdc9042db8d4eb149cd073d21}

Request-kenmerk. Ongeacht de huidige laaginstelling. Genegeerd als de bestandsindeling van de uitvoerafbeelding geen JPEG-codering ondersteunt. Zie de beschrijving van `fmt=` voor informatie over de uitvoerafbeeldingsindelingen `qlt=`.

*`chroma`* wordt genegeerd als het uitvoerpixeltype CMYK of grijs is.

## Standaard {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## Voorbeeld {#section-d7d33871d401433aa51d028823eae7a9}

Verminder kwaliteit voor snellere transmissie over een lage bandbreedteverbinding:

`http://server/myRoodId/myImageId?qlt=60&wid=300`

De kwaliteit van de verhoging voor hoge bandbreedteverbindingen:

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## Zie ook {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [kenmerk:JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
