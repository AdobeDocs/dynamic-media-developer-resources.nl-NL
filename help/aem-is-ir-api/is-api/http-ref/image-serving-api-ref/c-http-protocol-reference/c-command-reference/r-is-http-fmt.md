---
title: fmt
description: Indeling reactieafbeelding.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 0%

---

# fmt{#fmt}

Indeling reactieafbeelding.

`fmt=format[,` `[`*`pixelType`*`]` ,`[`*`compression`*`]]`

*`format`* - avif-alpha | avif | reep | f4m | gif-alpha | gif | heek | jpeg | jpeg2000-alpha | jpeg2000 | jpegxr-alpha | jpegxr | jpg | m3u8 | pdf | pjpeg | png-alpha | png | png8-alpha | png8 | swf-alpha | swf | swf3-alpha | swf3 | tif-alpha | tif | web-alpha | webben

| *`format`* | Beschrijving |
|---|---|
| `avif-alpha` | AVIF zonder verlies en met alfakanaal. |
| `avif` | AVIF zonder verlies en met verlies. |
| `eps` | Niet-gecomprimeerde binaire ingekapselde PostScript. |
| `f4m` | Flash Streaming Server-manifestindeling. |
| `gif-alpha` | GIF met 2 tot 255 kleuren plus hoofdkleurtransparantie. |
| `gif` | GIF met 2 tot 256 kleuren. |
| `heic` | HEIC zonder verlies. Deze indeling wordt standaard vanuit de browser gedownload als deze niet wordt ondersteund. |
| `jpeg` | JPEG met verlies. |
| `jpeg2000-alpha` | JPEG 2000 zonder verlies met alfakanaal. |
| `jpeg2000` | JPEG 2000 zonder verlies. |
| `jpegxr-alpha` | JPEG XR zonder verlies en met alfakanaal. |
| `jpegxr` | JPEG XR zonder verlies en zonder verlies. |
| `jpg` | JPG met verlies. |
| `m3u8` | Apple Streaming Server-manifestindeling. |
| `pdf` | Afbeelding ingesloten in PDF. |
| `pjpeg` | Progressieve JPEG. |
| `png-alpha` | 24-bits PNG zonder gegevensverlies met alfakanaal. |
| `png` | 24-bits PNG zonder gegevensverlies. |
| `png8-alpha` | 8-bits PNG zonder gegevensverlies met alfakanaal. |
| `png8` | 8-bits PNG zonder gegevensverlies. |
| `swf-alpha` | JPEG met verlies en een gecomprimeerd masker zijn ingesloten in een Adobe AS2 SWF-bestand. |
| `swf` | JPEG met verlies is ingesloten in een Adobe AS2 SWF-bestand. |
| `swf3-alpha` | JPEG met verlies en een gecomprimeerd masker zijn ingesloten in een Adobe AS3 SWF-bestand. **Nota:** swf en swf-alpha formaten worden best gebruikt voor ActionScript 2 toepassingen (Flash Player 8 en vroeger). De indelingen swf3 en swf3-alpha worden aanbevolen voor gebruik in ActionScript3-toepassingen (Flash Player 9 en hoger). |
| `swf3` | JPEG met verlies ingesloten in een Adobe AS3 SWF-bestand. |
| `tif-alpha` | TIFF met alpha-kanaal. |
| `tif` | TIFF. |
| `webp-alpha` | WebP zonder verlies en met alfakanaal. |
| `webp` | WebP zonder verlies en verlies. |

*`pixelType`* - rgb | grijs | cmyk

| *`pixelType`* | Beschrijving |
|---|---|
| `cmyk` | Retourneer CMYK-afbeeldingsgegevens. |
| `gray` | Retourneer afbeeldingsgegevens met grijswaarden. |
| `rgb` | Retourneer RGB-afbeeldingsgegevens. |

*`compression`* - jpeg | verlies | verliesloos | lzw | none | zip

| *`compression`* | Beschrijving |
|---|---|
| `jpeg` | JPEG-compressie (met verlies). |
| `lossy` | JPEG 2000, en JPEG XR compressie (verlies), en WebP. |
| `lossless` | HEIC, JPEG 2000, en JPEG XR compressie (lossless), en WebP. |
| `lzw` | LZW-compressie (Lempel-Ziv-Welch) (zonder verlies). |
| `none` | Niet gecomprimeerd. |
| `zip` | Compressie &#39;Deflate&#39; (zonder verlies). |

* *`format`* geeft de indeling voor afbeeldingscodering op voor afbeeldingsgegevens die naar de client worden verzonden en het corresponderende MIME-type voor reactie op de HTTP-responsheader.
* *`pixelType`* kan worden gebruikt om de kleurruimteconversie van de uitvoer te beïnvloeden wanneer `icc=` niet is opgegeven.

  Het standaardkleurprofiel dat overeenkomt met *`pixelType`* wordt toegepast. Als kleurbeheer is uitgeschakeld, wordt naïeve omzetting toegepast. *`pixelType`* wordt genegeerd wanneer `icc=` wordt opgegeven, wat het type uitvoerpixel bepaalt.

* *`compression`* is alleen toegestaan als `tif` , `tif-alpha` , `pdf` , `webp` , `webp-alpha` , `jpeg2000` , `jpeg2000-alpha` , `jpegxr` of `jpegxr-alpha` is opgegeven als de *`format`* . Raadpleeg de onderstaande tabel voor de compressieopties die worden ondersteund voor deze afbeeldingsindelingen.

Met `qlt=` kunt u de coderingsopties voor JPEG instellen voor de volgende indelingen: JPEG, TIFF met JPEG-compressie, PDF met JPEG-compressie en SWF. WebP, JPEG 2000, en JPEG XR gebruiken ook `qlt=` maar de waarden resulteren in verschillende kwaliteiten voor de verschillende formaten. Gebruik `quantize=` if `fmt=gif` of `fmt=gif-alpha` . Raadpleeg de opdrachtbeschrijvingen voor meer informatie. De andere indelingen hebben geen settable-opties.

8 bits per pixelcomponent worden geretourneerd voor alle *`formats`* en *`pixelTypes`* (8 bits per GIF).

De volgende lijst maakt een lijst van de geldige combinaties van * `format`*and *`pixelType`*, de overeenkomstige MIME van de reactie van HTTP types, of ICC profielen kunnen worden ingebed (zie [ iccEmbed= ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)), en welke formaat-specifieke opties u kunt toepassen.

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> format </i> </b> </th> 
   <th class="entry"> <b> <i> pixelType </i> </b> </th> 
   <th class="entry"> <b> MIME-type reactie </b> </th> 
   <th class="entry"> <b> bed ICC profiel </b> in </th> 
   <th class="entry"> <b> Opties </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> avif, avif-alpha </p> </td> 
   <td> <p>rgb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image/avif&gt; </span> </p> </td> 
   <td> <p>Nee </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compression </span> </span> ( <span class="codeph"> lossy </span> , <span class="codeph"> lossless </span> ) </p> <p> <span class="codeph"> qlt= </span> wordt genegeerd voor <span class="codeph"> verliesloos </span> . </p> <p>Omdat er geen concept is van chrominantiedonsampling met de WebP-indeling, wordt de tweede waarde ( <span class="codeph"> 1 </span> ) genegeerd als u een tweede waarde met <span class="codeph"> qlt </span> gebruikt (bijvoorbeeld <span class="codeph"> qlt=80,1 </span> ). </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> reep </p> </td> 
   <td colname="col2"> <p>rgb, grijs, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grijs </p> <p>Gegevens worden na omzetting in grijs of rgb omgezet in palet. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nee </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> quantize= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> heek </p> </td> 
   <td colname="col2"> <p>rgb </p> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/heic&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nee </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alpha </p> </td> 
   <td> <p>rgb, grijs </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>Nee </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compression </span> </span> ( <span class="codeph"> lossy </span> , <span class="codeph"> lossless </span> ) </p> <p> <span class="codeph"> qlt= </span> wordt genegeerd voor <span class="codeph"> verliesloos </span> . </p> <p>Omdat er geen concept is van chrominantiedonsampling met de WebP-indeling, wordt de tweede waarde ( <span class="codeph"> 1 </span> ) genegeerd als u een tweede waarde met <span class="codeph"> qlt </span> gebruikt (bijvoorbeeld <span class="codeph"> qlt=80,1 </span> ). </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb, grijs, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>, <span class="codeph"> pscan= </span>, <span class="codeph"> qlt= </span>, <span class="codeph"> xmpEmbed= </span> </p> <p>De parameter <span class="codeph"> pscan= </span> is alleen van toepassing op de JPEG-indeling. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>Nee </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compression </span> </span> ( <span class="codeph"> lossy </span> , <span class="codeph"> lossless </span> ) </p> <p> <span class="codeph"> qlt= </span> wordt genegeerd voor <span class="codeph"> verliesloos </span> . </p> <p>Omdat er geen concept is van chrominantiedonsampling met de WebP-indeling, wordt de tweede waarde ( <span class="codeph"> 1 </span> ) genegeerd als u een tweede waarde met <span class="codeph"> qlt </span> gebruikt (bijvoorbeeld <span class="codeph"> qlt=80,1 </span> ). </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb, grijs, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compression </span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span> ), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> wordt genegeerd, tenzij <span class="codeph"> <span class="varname"> compression </span> </span> is ingesteld op <span class="codeph"> jpeg </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alfa </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grijs </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb, grijs </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nee </p> <p> <p>Opmerking: de Flash Player Adobe negeert ingesloten ICC-profielen. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span> , <span class="codeph"> kenmerk::TrustedDomains </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grijs, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compression </span> </span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>Alleen 'tiff'; 'tiff-alpha' ondersteunt JPEG-compressie niet. </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> wordt genegeerd, tenzij <span class="varname"> compression </span> is ingesteld op <span class="codeph"> jpeg </span> . </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp, webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>Nee </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compression </span> </span> ( <span class="codeph"> lossy </span> , <span class="codeph"> lossless </span> ) </p> <p> <span class="codeph"> qlt= </span> wordt genegeerd voor <span class="codeph"> verliesloos </span> . </p> <p>Omdat er geen concept is van chrominantiedonsampling met de WebP-indeling, wordt de tweede waarde ( <span class="codeph"> 1 </span> ) genegeerd als u een tweede waarde met <span class="codeph"> qlt </span> gebruikt (bijvoorbeeld <span class="codeph"> qlt=80,1 </span> ). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

Request-kenmerk. Is van toepassing ongeacht de huidige laaginstelling als `req=img` (standaardwaarde) of `req=mask` ; anders genegeerd.

*`type`* wordt genegeerd als `iccProfile=` wordt opgegeven.

## Standaard {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *` defaultType `*,none`, waar *`defaultType`* als volgt wordt behandeld: Als `icc=` wordt gespecificeerd, *`defaultType`* beantwoordt aan het pixeltype van het gespecificeerde ICC profiel. Wanneer `icc=` niet is opgegeven, is *`defaultType`* is `gray` if `req=mask` , anders is het `rgb` .

## Voorbeelden {#section-b93222e652df404a84c69025247f07df}

**verzoek een klein, laag-kwaliteit voorproefbeeld in het formaat van JPEG (gebrek):**

` http:// *` server `*/myRootId/myImageId?qlt=60&wid=200`

**Verzoek het zelfde beeld dat in grijs-schaal wordt omgezet:**

` http:// *` server `*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**Verzoek het zelfde beeld in een verliesloos formaat met alpha- kanaal en bij hoge resolutie:**

` http:// *` server `*/myRootId/myImageId?fmt=png-alpha&wid=300`

**verzoek het alpha- kanaal voor het zelfde beeld zoals een grijs-schaal TIFF beeld:**

` http:// *` server `*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**zet het zelfde beeld in cmyk om gebruikend de standaardICC profielen:**

` http:// *` server `*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**zet het zelfde beeld in cmyk om gebruikend een verschillend ICC profiel en bedt het profiel in het beeld van TIFF in:**

` http:// *` server `*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**lever dit beeld als TIF dossier met de compressie van JPEG zonder pixeltypeomzetting:**

` http:// *` server `*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**zet beeld in een bi-toon GIF met zeer belangrijke-kleurentransparantie om en forceer kleuren aan zwart-wit:**

` http:// *` server `*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**Verlies met een kwaliteit die van 80 plaatst:**

` http:// *` server `*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Zonder verlies met alpha:**

` http:// *` server `*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**Verlies met een kwaliteit die van 80 plaatst:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Zonder verlies met alpha:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**Verlies met een kwaliteit die van 80 plaatst:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Zonder verlies met alpha:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## Zie ook {#section-fce8d69c74234bf48cf814d799409541}

[ qlt= ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352), [ quantize= ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38), [ req= ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [ icc= ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [ iccEmbed= ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [ pathEmbed= ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301), [ pscan ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135).
