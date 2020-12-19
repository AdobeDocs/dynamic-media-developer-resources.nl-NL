---
description: Indeling van responsimage.
seo-description: Indeling van responsimage.
seo-title: fmt
solution: Experience Manager
title: fmt
topic: Scene7 Image Serving - Image Rendering API
uuid: 78ee7545-5ad9-4240-bbfc-20efe3e42ed3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---


# fmt{#fmt}

Indeling van responsimage.

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> format</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alpha | tif | tif-alfa | SWF | pdf | gif | gif-alpha | fxg | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Hiermee geeft u de indeling voor afbeeldingscodering op voor afbeeldingsgegevens die naar de client worden verzonden en het corresponderende MIME-type voor reactie op de HTTP-antwoordheader. </p> <p> <span class="codeph">  jpeg  </span>: JPEG met verlies </p> <p> <span class="codeph"> png  </span>: PNG zonder verlies </p> <p> <span class="codeph"> png-alpha  </span>: PNG zonder verlies met alfakanaal </p> <p> <span class="codeph">  tif  </span>: TIFF </p> <p> <span class="codeph"> tif-alpha  </span>: TIFF met alfakanaal </p> <p> <span class="codeph">  SWF  </span>: JPEG met verlies ingesloten in een Adobe SWF-bestand </p> <p> <span class="codeph"> pdf  </span>: afbeelding ingesloten in PDF </p> <p> <span class="codeph"> gif  </span>: GIF met 2 tot 256 kleuren </p> <p> <span class="codeph"> gif-alpha  </span>: GIF met 2 tot 255 kleuren plus transparantie van hoofdkleuren </p> <p> <span class="codeph"> fxg  </span>: FXG met toegepaste variabelen en DOM-manipulatie </p> <p> <span class="codeph">  fxgraw  </span>: oorspronkelijke FXG opgeslagen op de server </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rgb | grijs | cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Kan worden gebruikt om de uitvoerkleurruimte te beïnvloeden. </p> <p> <span class="codeph">  rgb  </span>: RGB-afbeeldingsgegevens retourneren </p> <p> <span class="codeph"> grijs  </span>: grijswaardenafbeeldingsgegevens retourneren </p> <p> <span class="codeph"> cmyk  </span>: CMYK-afbeeldingsgegevens retourneren </p> </td> 
 </tr> 
</table>

`tiffCompression` is alleen toegestaan als tif, tif-alpha de indeling is. Raadpleeg de onderstaande tabel voor de compressieopties die worden ondersteund voor deze afbeeldingsindelingen.

`qlt=` U kunt de JPEG-coderingsopties instellen voor de volgende indelingen: JPEG, TIFF met JPEG-compressie. quantize= kan worden gebruikt als fmt=gif of fmt=gif-alpha. Raadpleeg de opdrachtbeschrijvingen voor meer informatie. De andere indelingen hebben geen settable-opties.

8 bits per pixelcomponent worden geretourneerd voor alle indelingen en `pixelTypes[7]`.

De volgende tabel bevat een lijst met geldige combinaties van opmaak en de corresponderende MIME-typen voor HTTP-respons.`pixelType`

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> format</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>Type Response MIME </p> </th> 
   <th colname="col4" class="entry"> <p>ICC-profiel insluiten </p> </th> 
   <th colname="col5" class="entry"> <p>Opties </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb, grijs, cmyk </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png, png-alpha </p> </td> 
   <td> <p>rgb, grijs </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif, tif-alpha </p> </td> 
   <td> <p>rgb, grijs, cmyk </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> ( geen | lzw | ZIP | jpeg), qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf, swf-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application&gt; </p> </td> 
   <td> <p>nee </p> </td> 
   <td> <p><span class="codeph"> qlt=  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>rgb, grijs, cmyk </p> </td> 
   <td> <p>&lt;application&gt; </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif, gif-alpha </p> </td> 
   <td> <p>rgb, grijs </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>nee </p> </td> 
   <td> <p><span class="codeph"> quantize=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
