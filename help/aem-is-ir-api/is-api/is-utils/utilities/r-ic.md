---
description: Hulpprogramma voor afbeeldingsomzetting.
seo-description: Hulpprogramma voor afbeeldingsomzetting.
seo-title: ic
solution: Experience Manager
title: ic
topic: Scene7 Image Serving - Image Rendering API
uuid: 08fabcc9-d0b5-4136-81fc-ac896c341e1d
translation-type: tm+mt
source-git-commit: e0f8153b038446180ddad313e591828223ed31e9

---


# ic {#ic}

Hulpprogramma voor afbeeldingsomzetting.

`ic` is een opdrachtregelprogramma waarmee afbeeldingsbestanden worden geconverteerd naar de geoptimaliseerde Piramid TIFF-indeling (PTIFF). Terwijl Image Serving afbeeldingen kan verwerken zonder conversie, raden we u aan alle afbeeldingen groter dan 512x512 pixels om te zetten in PTIFF. Deze conversie zorgt voor optimale serverprestaties en een optimaal gebruik van bronnen en minimaliseert de responstijden.

Het wordt aanbevolen PTIFF-bestanden die fotografische inhoud bevatten, JPEG-gecodeerd te laten zijn (specificeren `-jpegcompress`). Door de computer gegenereerde inhoud kan profiteren van compressie zonder verlies ( `-deflatecompress` of `-lzwcompress`). Tenzij een kleurconversie of conversie van pixeltypen vereist is, worden JPEG-bronafbeeldingsgegevens zonder decodering overgebracht naar PTIFF om kwaliteitsverlies te voorkomen. In dit geval zijn de opgegeven compressieopties alleen van toepassing op de piramide met lagere resolutie.

Als u grote afbeeldingen niet omzet, hoeft u de parameters die bepalen hoeveel geheugen u moet gebruiken, niet in te stellen. Als u dat wel doet, moet u `ic` meer geheugen vrijmaken door de `-maxmem` instelling hieronder te gebruiken. Een goede duim voor het berekenen van de vereiste hoeveelheid geheugen is het vermenigvuldigen van de breedte van de afbeelding en het vermenigvuldigen van de hoogte van de afbeelding en het aantal kanalen. Bijvoorbeeld vier voor een RGB-afbeelding met alpha-driemaal. Bovendien als de kanalen 16 beetjes per component in plaats van 8 tweemaal het definitieve resultaat zijn.

## Gebruik {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]` *`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]` *`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]` *`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>opties</i> </span></span> </p> </td> 
   <td colname="col2"> <p>Opdrachtopties (zie hieronder). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> sourceFile <i></i> </span></span> </p> </td> 
   <td colname="col2"> <p>Eén invoerafbeeldingsbestand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span></span> </p> </td> 
   <td colname="col2"> <p>Eén PTIFF-uitvoerbestand (niet geldig als het wordt gebruikt met SourceDirectory). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span></span> </p> </td> 
   <td colname="col2"> <p>Map met invoerafbeeldingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span></span> </p> </td> 
   <td colname="col2"> <p>Map waarnaar PTIFF-uitvoerbestanden worden geschreven. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-36a2dcfa39824d29b69547c432366219}

0 indien gelukt. Als een fout optreedt, wordt een waarde die niet gelijk is aan nul, geretourneerd en worden foutgegevens verzonden naar `stderr`.

## Opties {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -uncompressed </span> </p> </td> 
   <td colname="col2"> <p>Comprimeer de uitvoerafbeelding niet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress </span> </p> </td> 
   <td colname="col2"> <p>Gebruik compressie deflate (zip) (standaardwaarde). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>Gebruik Lempel-Ziv-Welch (LZW) compressie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>JPEG-codering gebruiken. Genegeerd als <span class="codeph"> sourceFile alpha-gegevens <span class="varname"></span> </span> bevat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname"> quality </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>JPEG-kwaliteit (0-100; de standaardwaarde is 95). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplechrominance </span> </p> </td> 
   <td colname="col2"> <p>Schakel JPEG-chroma-downsampling uit (kan de kwaliteit van tekst en afbeeldingen in kleur verbeteren). Dit heeft geen effect op uitvoerafbeeldingen die CMYK of grijswaarden zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname"> amount </span>&gt; &lt; <span class="varname"> radius </span>&gt; &lt; <span class="varname"> threshold </span>&gt; &lt; <span class="varname"> monochrome </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Pas onscherp maskeren toe op piramideniveaus in subsampling. Zie <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a> voor meer informatie. (Niet toegepast op de afbeelding met volledige resolutie.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath </span> </p> </td> 
   <td colname="col2"> <p>Gebruik het clippad in het bronbestand (indien aanwezig) om gekoppelde alfakanalen te maken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dpi </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Afdrukresolutie (dpi) voor <span class="codeph"> destFile <span class="varname"> </span> </span>; als niet opgegeven, wordt de afdrukresolutie van <span class="codeph"> srcFile </span> gekopieerd naar <span class="codeph"> <span class="varname"> destFile </span> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop &lt; <span class="varname"> corner </span>&gt; &lt; <span class="varname"> mode </span>&gt; &lt; <span class="varname"> tolerance </span>&gt; &lt; <span class="varname"> infoFile </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Bereken een snijrechthoek om een achtergrond met een effen kleur te minimaliseren. Er worden geen uitsnijdgegevens weergegeven als het algoritme voor automatisch uitsnijden zou resulteren in het uitsnijden van de gehele afbeelding. </p> <p>Als u de uitsnijdrechthoek wilt berekenen zonder de afbeelding om te zetten, geeft u <span class="codeph"> -automatisch uitsnijden </span> zonder - <span class="codeph"> omzetten </span> en zonder <span class="codeph"> <span class="varname"> destFile op.</span> </span></p>

<p><i><b>corner</b></i> - ul| EUR| Alle| lr </p>
   <p> Hiermee geeft u op welke hoek van de afbeelding een zaadpunt moet worden gebruikt. Genegeerd als de modus 1 is.</p>
   <p><i><b>modus</b></i> - 0| 1</p>
   <p>Stel de waarde in op 0 voor uitsnijden op basis van de kleur van de opgegeven hoekpixel; werkt aan vooraf vermenigvuldigde kleurengegevens als de alpha- gegevens met het bronbeeld worden geassocieerd.</p>
   <p>Instellen op 1 voor uitsnijden op basis van alpha-gegevens; hoek wordt genegeerd en 0 altijd de zaadwaarde is; er wordt geen uitsnijding toegepast als er geen alpha-gegevens aan de bronafbeelding zijn gekoppeld.</p> 
   <p><i><b>tolerantie</b></i> - Tolerantie afstemmen. Reële waarde 0,0 tot 1,0. Hiermee geeft u de tolerantie op voor overeenkomende pixelcomponentwaarden. Ingesteld op 0 voor exacte overeenkomsten.</p>
   <p><i><b>infoFile</b></i> - Pad en naam van het XML-uitvoerbestand waarnaar de gegevens over de uitsnijdgegevens worden geschreven.</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>Kopieer XMP-metagegevens, indien beschikbaar, van <span class="codeph"> sourceFile <span class="varname"> </span> naar </span> <span class="codeph"> destFile <span class="varname"> </span> </span> zonder wijzigingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> Sluit het ICC-kleurprofiel in het <span class="codeph"> destFile-bestand in <span class="varname"> </span> </span>als dit beschikbaar is (er is standaard geen profiel ingesloten). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Pad en naam van een ICC-profielbestand. Definieert de kleurruimte van het <span class="codeph"> bronbestand <span class="varname"> </span> </span> en moet overeenkomen met het pixeltype. Moet alleen worden opgegeven als er geen profiel is ingesloten in <span class="codeph"> bronbestand <span class="varname"> </span> </span>, aangezien dit het ingesloten profiel overschrijft. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> bestand </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Pad en naam van een ICC-profielbestand. Definieert het pixeltype en de kleurruimte van <span class="codeph"> destFile <span class="varname"> </span> </span>. IC wordt naar dit profiel geconverteerd als het <span class="codeph"> bronbestand <span class="varname"> een ingesloten profiel </span> heeft of als het </span> -imageprofiel <span class="codeph"> </span> ook is opgegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual </span> </p> </td> 
   <td colname="col2"> <p>Perceptuele render-intentie voor kleurruimteconversies. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric </span> </p> </td> 
   <td colname="col2"> <p> Relatieve colorimetrische render-intentie voor kleurruimteconversies (standaard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric </span> </p> </td> 
   <td colname="col2"> <p>Absolute colorimetrische render-intentie voor kleurruimteconversies. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation </span> </p> </td> 
   <td colname="col2"> <p>Render-intentie voor verzadiging voor conversies van kleurruimten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>Zwartpuntcompensatie uitschakelen voor bepaalde kleuromzettingen </p> <p>Standaard ingeschakeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>Dithering uitschakelen (foutdiffusie) bij het omzetten van kleuren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixelType </span> </p> </td> 
   <td colname="col2"> <p> Schakel automatische omzetting van CMYK in RGB uit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>Decodering en hercodering van JPEG-invoerafbeeldingen forceren. </p> <p> <b>Let op:</b> Als u deze optie toepast, kan de afbeeldingskwaliteit afnemen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2 </span> </p> </td> 
   <td colname="col2"> <p>Gebruik een standaardindelingsfilter voor kwaliteit (bi-lineair). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8 </span> </p> </td> 
   <td colname="col2"> <p>Gebruik filter voor het berekenen van nieuwe pixels van hogere kwaliteit (Lanczos-venster) (standaard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>Gebruik het filter Nieuwe pixels berekenen van hogere kwaliteit (FlashPix). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp </span> </p> </td> 
   <td colname="col2"> <p>Downsamplen met bicubisch, scherp filter in Photoshop-stijl 8 x 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage </span> </p> </td> 
   <td colname="col2"> <p> Wanneer opgegeven als de eerste optie, wordt de uitvoer van gebruiksinformatie onderdrukt wanneer er ongeldige opties worden aangetroffen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -overschrijven </span> </p> </td> 
   <td colname="col2"> <p>Overschrijven van een bestaand <span class="codeph"> destFile toestaan <span class="varname"> </span> </span>. Standaard wordt een numeriek achtervoegsel aan de bestandsnaam toegevoegd om te voorkomen dat het wordt overschreven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden </span> </p> </td> 
   <td colname="col2"> <p>Verborgen bronbestanden negeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueOnError </span> </p> </td> 
   <td colname="col2"> <p>Stop niet met verwerken wanneer een fout optreedt. Dit heeft alleen effect bij het verwerken van meerdere bestanden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logbestand &lt; <span class="varname"> bestand </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Pad en naam voor het logbestand (standaardinstellingen voor <span class="codeph"> stdout </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname"> level </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Logniveau. </p> 
   <p>&lt; 0 - Aanmelden uitgeschakeld.</p>
   <p>0 - Bestanden weergeven die moeten worden verwerkt.</p>
   <p>1 - Rapportage toevoegen voor overbodige bestanden.</p>
   <p>2 - Voeg voortgangsrapportage toe.</p>
   <p>3 - Voeg rapporten toe over elk aangetroffen bestand.</p>
   <p>4 - Voeg voortgangsrapporten toe op bestandsniveau.</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend </span> </p> </td> 
   <td colname="col2"> <p>Toevoegen aan logbestand (standaard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend </span> </p> </td> 
   <td colname="col2"> <p>Overschrijf het logbestand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec &lt; <span class="varname"> msec </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Het registreren interval in msec voor loglevel 2 en hoger (gebrek is 3000). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt; <span class="varname"> bytes </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Limiet geheugengebruik. Moet ten minste 10 MB zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname"> percent </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Limiet geheugengebruik. Standaard is 25% van het fysieke geheugen. Als noch <span class="codeph"> maxmem </span> noch <span class="codeph"> maxmempercent </span> uitdrukkelijk wordt geplaatst gebruik maxmempercent gebrek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -version </span> </p> </td> 
   <td colname="col2"> <p> Retourversie-info voor dit hulpprogramma. Opgeven zonder andere opties. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ondersteunde indelingen voor invoerafbeeldingen {#section-ab13d941d6724e65b9f84b62d949d31c}

In de volgende tabel worden de bestandsindelingen en indelingsopties voor afbeeldingen weergegeven die door de Inkoopordermap worden ondersteund.

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> Indeling</b> </p> </th> 
   <th class="entry"> <p> <b> Pixeltekstbits</b> / <b> kromtrekken</b> </p> </th> 
   <th class="entry"> <p> <b> Bits/chan</b> </p> </th> 
   <th class="entry"> <p> <b> Compressie</b> </p> </th> 
   <th class="entry"> <p> <b> Notities</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> (Windows Bitmap) </p> </td> 
   <td> <p> RGB| geïndexeerd </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> ongecomprimeerd| RLE </p> </td> 
   <td> <p> 5/6 bits/kanaal geeft ondersteuning aan voor 16-bits RGB (5-5-5 en 5-6-5 bits/kanaal). </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Encapsulated Postscript) </p> </td> 
   <td> <p> CMYK| RGB| grijs </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII| ASCII85| Binair| JPEG </p> </td> 
   <td> <p> Alleen EPS-bestanden die door Photoshop zijn gegenereerd, worden ondersteund. </p> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> <p> CompuServe </p> <b>GIF</b> </td> 
   <td> <p> geïndexeerd </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
   <td> <p> Indien aanwezig wordt de transparantiewaarde in het palet omgezet in alfa. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK| RGB| grijs </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK| CMYKA| RGB| RGBA| grijs| grijsA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> ongecomprimeerd| gecomprimeerd </p> </td> 
   <td> <p> Alleen samengevoegde afbeelding; lagen en extra kanalen worden genegeerd. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> alleen bitmapgegevens; vectorgegevens worden genegeerd. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB| RGBA| grijs| grijsA| geïndexeerd </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> gecomprimeerd </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK| CMYKA| RGB| RGBA| grijs| grijsA| geïndexeerd </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> ongecomprimeerd| ZIP| LZW| JPEG| CCITT RLE| CCITT G3| CCITT G4| Pakketten </p> </td> 
   <td> <p> Met uitzondering van het eerste gekoppelde alfakanaal worden extra kanalen genegeerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ingesloten ICC-profielen worden herkend in EPS-, JPG-, PSD-, PNG- en TIFF-bestanden.

Ingesloten paden en XMP-metagegevens worden herkend in EPS-, JPG-, PSD- en TIFF-bestanden.

## Voorbeelden {#section-3c1986b30315431989bd76b1ee5bef6d}

Converteer één afbeelding met de beste kwaliteit en zorg dat deze in dezelfde map blijft:

`ic -convert src/myFile.png src/myFile.tif`

Zet alle afbeeldingen om in *`srcFolder`* TIFF-bestanden met JPEG-codering en plaats ze in *`destFolder`*:

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

Alle afbeeldingen converteren in *`srcFolder`*. De gecodeerde afbeeldingsgegevens van JPG-bestanden worden gebruikt voor LZW-compressie met volledige resolutie en zonder verlies voor de rest van de afbeeldingspiramide van deze afbeeldingen en voor de volledige uitvoerafbeelding van alle niet-JPG-invoerbestanden. De pixeltypen, ingesloten kleurprofielen, XMP-metagegevens, enz. worden gehandhaafd.

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
