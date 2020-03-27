---
description: Afbeeldingsindeling beantwoorden. Hiermee geeft u de indeling voor afbeeldingscodering op voor afbeeldingsgegevens die naar de client worden verzonden en het corresponderende MIME-type voor reactie op de HTTP-antwoordheader.
seo-description: Afbeeldingsindeling beantwoorden. Hiermee geeft u de indeling voor afbeeldingscodering op voor afbeeldingsgegevens die naar de client worden verzonden en het corresponderende MIME-type voor reactie op de HTTP-antwoordheader.
seo-title: fmt
solution: Experience Manager
title: fmt
topic: Scene7 Image Serving - Image Rendering API
uuid: 7c589119-d1b3-460f-acbd-5e8d10d0d976
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# fmt{#fmt}

Afbeeldingsindeling beantwoorden. Hiermee geeft u de indeling voor afbeeldingscodering op voor afbeeldingsgegevens die naar de client worden verzonden en het corresponderende MIME-type voor reactie op de HTTP-antwoordheader.

` fmt= *``*[,[ *``*][, *`formatpixelTypetiffCompression`*`]]

<table id="simpletable_200779AA8D8D49A089A295AED5C98C8F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> format </span> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>JPEG met gegevensverlies. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpg </p> </td> 
  <td class="stentry"> <p>JPG met verlies. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png </p> </td> 
  <td class="stentry"> <p>PNG zonder verlies. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png-alpha </p> </td> 
  <td class="stentry"> <p>PNG zonder verlies met alfakanaal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif </p> </td> 
  <td class="stentry"> <p>TIFF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif-alpha </p> </td> 
  <td class="stentry"> <p>TIFF met alfakanaal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>JPEG met gegevensverlies is ingesloten in een SWF-bestand met macromedia. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alpha </p> </td> 
  <td class="stentry"> <p>JPEG met verlies en een gecomprimeerd masker zijn ingesloten in een SWF-bestand met macromedia. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>pdf </p> </td> 
  <td class="stentry"> <p>Afbeelding ingesloten in PDF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>reep </p> </td> 
  <td class="stentry"> <p>Niet-gecomprimeerde binaire Encapsulated PostScript. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif </p> </td> 
  <td class="stentry"> <p>GIF met 256 kleuren. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif-alpha </p> </td> 
  <td class="stentry"> <p>GIF met 255 kleuren plus transparantie van hoofdkleuren. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pixelType </span> </p> </td> 
  <td class="stentry"> <p>rgb </p> </td> 
  <td class="stentry"> <p>Retourneer RGB-afbeeldingsgegevens. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>grijs </p> </td> 
  <td class="stentry"> <p>Retourneer afbeeldingsgegevens met grijswaarden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>cmyk </p> </td> 
  <td class="stentry"> <p>Retourneer CMYK-afbeeldingsgegevens. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> tiffCompression </span> </td> 
  <td class="stentry"> <p>none </p> </td> 
  <td class="stentry"> <p>Niet gecomprimeerd. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>lzw </p> </td> 
  <td class="stentry"> <p>LZW-compressie (Lempel-Ziv-Welch) (zonder verlies). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>zip </p> </td> 
  <td class="stentry"> <p>Compressie 'Deflate' (zonder verlies). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>JPEG-compressie (met gegevensverlies). </p> </td> 
 </tr> 
</table>

*`pixelType`* effecten, kleurruimteconversie uitvoeren als `icc=` deze niet is opgegeven; het standaardkleurprofiel dat overeenkomt met *`pixelType`* wordt toegepast. Als kleurbeheer is uitgeschakeld, wordt naïeve omzetting toegepast. *`pixelType`* wordt genegeerd wanneer `icc=` wordt opgegeven, waardoor het pixeltype van de uitvoer wordt bepaald.

*`compression`* is alleen toegestaan als de waarde tif, tif-alpha of PDF is opgegeven als de waarde *`format`*. Raadpleeg de onderstaande tabel voor de compressieopties die worden ondersteund voor deze afbeeldingsindelingen.

`qlt-` Hiermee stelt u de JPEG-coderingsopties in voor deze indelingen: JPEG, TIFF met JPEG-compressie, PDF met JPEG-compressie en SWF-bestand. Gebruik `quantize=` als `fmt=gif` of `fmt=gif-alpha`. Raadpleeg de opdrachtbeschrijvingen voor meer informatie. De andere indelingen hebben geen settable-opties.

8 bits per pixelcomponent worden geretourneerd voor alle indelingen en pixeltypen.

De volgende tabel bevat een lijst met geldige combinaties van *`format`* en *`pixelType`*, de corresponderende MIME-typen voor HTTP-reacties, of ICC-profielen kunnen worden ingesloten (zie [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)) en welke indelingsspecifieke optieopdrachten kunnen worden toegepast.

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname"> format </span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> pixelType </span> </p> </th> 
   <th colname="col3" class="entry"> <p>Type MIME-antwoord </p> </th> 
   <th colname="col4" class="entry"> <p>ICC-profiel insluiten </p> </th> 
   <th colname="col5" class="entry"> <p>Opties </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg, jpg </p> </td> 
   <td colname="col2"> <p>rgb, grijs, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <span class="codeph"> qlt= </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grijs </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png8, png8-alfa </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grijs, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> (none|lzw|zip|jpeg), pathEmbed=, qlt </span> </p> <p>( <span class="codeph"> qlt= </span> wordt genegeerd, tenzij <span class="varname"> tiffCompression </span> is ingesteld op 'jpeg'.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>swf, swf-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grijs </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nee </p> <p>(In Flash Player worden ingesloten ICC-profielen genegeerd.) </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> kenmerk::TrustedDomains </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pdf </p> </td> 
   <td colname="col2"> <p>rgb, grijs, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> (none|zip|jpeg),qlt= </span> </p> <p> ( <span class="codeph"> qlt= </span> wordt genegeerd, tenzij <span class="varname"> tiffCompression </span> is ingesteld op 'jpeg'.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>reep </p> </td> 
   <td colname="col2"> <p>rgb, grijs, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grijs </p> <p>(Gegevens worden na omzetting naar grijs of RGB omgezet in palet.) </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nee </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

Hiermee geeft u de coderingsindeling op voor de gegevens van de antwoordafbeelding die naar de client worden verzonden en het corresponderende MIME-type voor de antwoordheader van HTTP.

`png-alpha` geeft niet-gekoppelde alfa (oftewel alpha vermenigvuldigt de pixelwaarden niet vooraf), terwijl `tif-alpha`en `swf-alpha` daaraan gekoppelde alpha retourneert (de alpha-waarden worden dus vooraf vermenigvuldigd met de alpha-waarden). Het alfakanaal komt overeen met het omgekeerde van het achtergrondmasker van het vignet voor `req=img`, en met de groep of het objectmasker in het geval van `req=object`. Om alpha toe te passen wanneer het gebruiken van een genest verzoek van AIR, voeg `fmt=` met het aangewezen alpha- dossierformaat aan het ingebedde verzoek van IRL en het belangrijkste verzoek toe. Er worden geen alpha-gegevens geretourneerd als er een ICC-profiel met CMYK of grijswaarden is opgegeven met `icc=`.

## Eigenschappen {#section-eb12a82c69d84622bcea153dd84d95b3}

Kan overal in het verzoek voorkomen.

## Standaard {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`* is standaard ingesteld op `attribute::Format`en is *`tiffCompression`* standaard ingesteld op `attribute::TiffEncoding`. *`pixelType`* Wordt standaard ingesteld `rgb` als `icc=` dit niet het geval is, anders komt dit overeen met het pixeltype van het opgegeven ICC-profiel.

## Zie ook {#section-c55efc881fc94c70bff91b870e026a7b}

[kenmerk::Format](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2) , [kenmerk::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50), [kenmerk::TiffEncoding](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e), [qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f)[](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)[pathEmbed=,Req=,Quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)
