---
description: Indeling reactieafbeelding.
seo-description: Indeling reactieafbeelding.
seo-title: fmt
solution: Experience Manager
title: fmt
topic: Scene7 Image Serving - Image Rendering API
uuid: 29151740-3bbc-4c5e-bbc7-4afe9064ff5f
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 0%

---


# fmt{#fmt}

Indeling reactieafbeelding.

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* — jpeg | jpg | pjpeg | png | png8 | png-alpha | png8-alpha | tif | tif-alfa | SWF | swf-alpha | swf3 | swf3-alfa | eps | gif | gif-alpha | m3u8 | f4m | web | webp-alpha | jpeg2000 | jpeg2000-alfa | jpegxr | jpegxr-alpha

| *`format`* | Beschrijving |
|---|---| 
| `jpeg` | JPEG met gegevensverlies |
| `jpg` | JPG met gegevensverlies |
| `pjpeg` | Progressieve JPEG |
| `png` | 24-bits PNG zonder gegevensverlies |
| `png8` | 8-bits PNG zonder gegevensverlies |
| `png-alpha` | 24-bits PNG zonder gegevensverlies met alfakanaal |
| `png8-alpha` | 8-bits PNG zonder gegevensverlies met alfakanaal |
| `tif` | TIFF |
| `tif-alpha` | TIFF met alfakanaal |
| `pdf` | Afbeelding ingesloten in PDF |
| `eps` | Niet-gecomprimeerde binaire Encapsulated PostScript |
| `gif` | GIF met 2 tot 256 kleuren |
| `gif-alpha` | GIF met 2 tot 255 kleuren plus transparantie van hoofdkleuren |
| `swf` | JPEG met verlies ingesloten in een Adobe AS2 SWF-bestand |
| `swf-alpha` | JPEG met verlies en een gecomprimeerd masker zijn ingesloten in een SWF-bestand met Adobe AS2 |
| `swf3` | JPEG met verlies ingesloten in een Adobe AS3 SWF-bestand |
| `swf3-alpha` | JPEG met verlies en een gecomprimeerd masker zijn ingesloten in een SWF-bestand met Adobe AS3. **Opmerking**: SWF- en swf-alfa-indelingen kunnen het best worden gebruikt voor ActionScript 2-toepassingen (Flash Player 8 en eerder). swf3 en swf3-alpha wordt aanbevolen voor gebruik bij ActionScript 3-toepassingen (Flash Player 9 en hoger) |
| `m3u8` | Apple Streaming Server-manifestindeling |
| `f4m` | Flash Streaming Server-manifest-indeling |
| `webp` | WebP zonder gegevensverlies |
| `webp-alpha` | WebP zonder verlies en met alfakanaal |
| `jpeg2000` | JPEG 2000 met verlies en zonder verlies |
| `jpeg2000-alpha` | JPEG 2000 met alfakanaal zonder verlies en verlies |
| `jpegxr` | JPEG XR zonder gegevensverlies |
| `jpegxr-alpha` | JPEG XR zonder verlies en met alfakanaal |


| *`pixelType`* — rgb | grijs | cmyk |
| *`pixelType`* | Beschrijving |
|---|---|
| `rgb` | Retourneer RGB-afbeeldingsgegevens. |
| `gray` | Retourneer afbeeldingsgegevens met grijswaarden. |
| `cmyk` | Retourneer CMYK-afbeeldingsgegevens. |

| *`compression`* — geen | lzw | zip | jpeg | verlies | verliesloos |
| *`compression`* | Beschrijving |
|---|---|
| `none` | Niet gecomprimeerd |
| `lzw` | LZW-compressie (Lempel-Ziv-Welch) (zonder verlies) |
| `zip` | Compressie &#39;Deflate&#39; (zonder gegevensverlies) |
| `jpeg` | JPEG-compressie (met verlies) |
| `lossy` | WebP-, JPEG 2000- en JPEG XR-compressie (met verlies) |
| `lossless` | WebP-, JPEG 2000- en JPEG XR-compressie (zonder gegevensverlies) |

* *`format`* geeft de indeling voor afbeeldingscodering op voor afbeeldingsgegevens die naar de client worden verzonden en het bijbehorende MIME-type voor reactie op de HTTP-antwoordheader.
* *`pixelType`* kan worden gebruikt voor het uitvoeren van kleurruimteconversie van de uitvoer wanneer deze niet  `icc=` is opgegeven.

   Het standaardkleurprofiel dat overeenkomt met *`pixelType`* wordt toegepast. Als kleurbeheer is uitgeschakeld, wordt naïeve omzetting toegepast. *`pixelType`* wordt genegeerd wanneer  `icc=` wordt opgegeven, waardoor het pixeltype van de uitvoer wordt bepaald.

* *`compression`* is alleen toegestaan als  `tif`,  `tif-alpha`,  `pdf`,  `webp`,  `webp-alpha`,  `jpeg2000`,  `jpeg2000-alpha`,  `jpegxr`, of  `jpegxr-alpha` is opgegeven als de  *`format`*. Raadpleeg de onderstaande tabel voor de compressieopties die worden ondersteund voor deze afbeeldingsindelingen.

Met `qlt=` kunt u de JPEG-coderingsopties voor deze indelingen instellen: JPEG, TIFF met JPEG-compressie, PDF met JPEG-compressie en SWF. WebP, JPEG 2000, en JPEG XR gebruiken ook `qlt=` maar de waarden resulteren in verschillende kwaliteiten voor de verschillende formaten. Gebruik `quantize=` als `fmt=gif` of `fmt=gif-alpha`. Raadpleeg de opdrachtbeschrijvingen voor meer informatie. De andere indelingen hebben geen settable-opties.

8 bits per pixelcomponent worden geretourneerd voor alle *`formats`* en *`pixelTypes`* (8 bits per pixel voor GIF).

De volgende lijst maakt een lijst van de geldige combinaties van *`format`*en *`pixelType`*, de overeenkomstige MIME van de reactie van HTTP types, of ICC profielen kunnen worden ingebed (zie [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)), en welke formaat-specifieke opties u kunt toepassen.

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> format</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> Type Response MIME</b> </th> 
   <th class="entry"> <b>ICC-profiel insluiten</b> </th> 
   <th class="entry"> <b> Opties</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb, grijs, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span>,  <span class="codeph"> pscan=  </span>,  <span class="codeph"> qlt=  </span>,  <span class="codeph"> xmpEmbed=  </span> </p> <p>De parameter <span class="codeph"> pscan= </span> is alleen van toepassing op pjpeg-indeling. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grijs </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alfa </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grijs, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compressie  </span> </span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>alleen "tiff"; 'tiff-alpha' ondersteunt JPEG-compressie niet. </p> <p> <span class="codeph"> qlt=  </span> </p> <p> <span class="codeph"> qlt=  </span> wordt genegeerd, tenzij  <span class="varname"> compressie  </span> is ingesteld op  <span class="codeph"> jpeg  </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb, grijs </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nee </p> <p> <p>Opmerking:  De Adobe-Flash Player negeert ingesloten ICC-profielen. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt=  </span>,  <span class="codeph"> kenmerk::TrustedDomains  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb, grijs, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compressie  </span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt=  </span> wordt genegeerd, tenzij  <span class="codeph"> <span class="varname"> compressie  </span> </span> is ingesteld op  <span class="codeph"> jpeg  </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> reep </p> </td> 
   <td colname="col2"> <p>rgb, grijs, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grijs </p> <p>Gegevens worden na omzetting in grijs of RGB omgezet in palet. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nee </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> quantize=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>web, webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>Nee </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compressie  </span> </span> (  <span class="codeph"> met verlies  </span>,  <span class="codeph"> zonder verlies  </span>) </p> <p> <span class="codeph"> qlt=  </span> wordt genegeerd voor  <span class="codeph"> gegevensverlies  </span>. </p> <p>Omdat er geen concept van chrominantiedonsampling met formaat WebP is, als u een tweede waarde met <span class="codeph"> qlt </span> (bijvoorbeeld, <span class="codeph"> qlt=80,1 </span>) gebruikt wordt de tweede waarde ( <span class="codeph"> 1 </span>) genegeerd. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alpha </p> </td> 
   <td> <p>rgb, grijs </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>Nee </p> </td> 
   <td> <p>Hetzelfde als hierboven. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>Nee </p> </td> 
   <td> <p>Hetzelfde als hierboven. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

Request-kenmerk. Past ongeacht huidige laag toe die als `req=img` (gebrek) of `req=mask` plaatst; anders genegeerd.

*`type`* wordt genegeerd als  `iccProfile=` wordt opgegeven.

## Standaard {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`, waarbij de methode als volgt  *`defaultType`* wordt afgehandeld: Als deze  `icc=` is opgegeven,  *`defaultType`* komt dit overeen met het pixeltype van het opgegeven ICC-profiel. Als `icc=` niet wordt gespecificeerd, *`defaultType`* is `gray` als `req=mask`, anders is het `rgb`.

## Voorbeelden {#section-b93222e652df404a84c69025247f07df}

**Een kleine voorvertoning van lage kwaliteit in de JPEG-indeling aanvragen (standaard):**

` http:// *`server`*/myRootId/myImageId?qlt=60&wid=200`

**Dezelfde afbeelding converteren naar grijswaarden:**

` http:// *`server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**Dezelfde afbeelding aanvragen in een indeling zonder verlies met alfakanaal en met een hoge resolutie:**

` http:// *`server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**Vraag het alfakanaal aan voor dezelfde afbeelding als een grijswaardenTIFF-afbeelding:**

` http:// *`server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**Dezelfde afbeelding converteren naar CMYK met de standaard-ICC-profielen:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**Dezelfde afbeelding converteren naar CMYK met een ander ICC-profiel en het profiel insluiten in de TIFF-afbeelding:**

` http:// *`server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**Deze afbeelding leveren als een TIF-bestand met JPEG-compressie zonder conversie van pixeltypen:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**Zet de afbeelding om in een bitonale GIF met toetkleurtransparantie en forceer de kleuren naar zwart-wit:**

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**Verlies met een kwaliteitsinstelling van 80:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Zonder verlies met alfa:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**Verlies met een kwaliteitsinstelling van 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Zonder verlies met alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**Verlies met een kwaliteitsinstelling van 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Zonder verlies met alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## Zie ook {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38),  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135)pathEmbed=,pscan.
