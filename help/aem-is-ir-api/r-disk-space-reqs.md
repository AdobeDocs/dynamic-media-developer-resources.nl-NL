---
description: 'Naast de ruimte die nodig is om de software te installeren, heeft Image Serving de volgende vereisten voor schijfruimte '
seo-description: 'Naast de ruimte die nodig is om de software te installeren, heeft Image Serving de volgende vereisten voor schijfruimte '
seo-title: Vereisten en aanbevelingen voor schijfruimte
solution: Experience Manager
title: Vereisten en aanbevelingen voor schijfruimte
topic: Scene7 Image Serving - Image Rendering API
uuid: a6a21886-94d6-45b3-af68-497e039bdbac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---


# Vereisten en aanbevelingen voor schijfruimte{#disk-space-requirements-and-recommendations}

Naast de ruimte die nodig is om de software te installeren, gelden voor Image Serving de volgende vereisten voor schijfruimte:

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Beschrijving/Standaardlocatie/ Instellen met</b> </th> 
   <th class="entry"> <b>Berekening/aanbeveling</b> </th> 
   <th class="entry"> <b>Opmerkingen</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Bronafbeeldingen, lettertypen, ICC-profielen</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/images  </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS:RootPaths  </span> </p> </td> 
   <td> <p>variëren; zie onderstaande opmerkingen. </p> </td> 
   <td> <p>Alleen toegankelijk moet zijn voor de imageserver. de servers wijzigen nooit gegevens. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP-responsgegevenscache</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/is-response  </span> </p> <p> <span class="codeph"> PS:ResponseCacheFolders  </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize  </span> x 2; minimaal 2 GB aanbevolen. </p> </td> 
   <td> <p>In deze cache worden ook geneste/ingesloten gegevens en externe bronafbeeldingen opgeslagen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Gegevenscache afbeeldingscatalogus</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/catalog  </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder  </span> </p> </td> 
   <td> <p>Laat de catalogusmap 1,5x de ruimte gebruiken. </p> </td> 
   <td> <p>Wordt gevuld wanneer catalogi in eerste instantie worden geladen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Loggegevens</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/logs  </span> </p> <p> <span class="codeph"> PS:LogFolder  </span> </p> <p> <span class="codeph"> IS:LogFile  </span> </p> <p> <span class="codeph"> SV::LogFile  </span> </p> </td> 
   <td> <p>100 Mbytes of meer. </p> </td> 
   <td> <p>Dit varieert afhankelijk van de logboekconfiguratie en het servergebruik. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Tijdelijke bestanden afbeeldingsserver</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/temp  </span> </p> <p> <span class="codeph"> IS:TempDirectory  </span> </p> <p> <span class="codeph"> SV:TempDirectory  </span> </p> </td> 
   <td> <p>100 MBytes is voldoende voor de meeste toepassingen. </p> </td> 
   <td> <p>kortstondige gegevens; kan nodig zijn voor andere bronafbeeldingen dan PTIFF's en bepaalde indelingen voor reactieafbeeldingen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Vereisten voor schijfruimte voor bronafbeeldingen {#section-317da75099ad480d9a461c7e706d4f1c}

Het wordt aanbevolen alle bronafbeeldingen om te zetten in de piramidebestandsindeling TIFF (PTIFF) met het opdrachtregelprogramma voor het omzetten van afbeeldingen (IC). Deze conversie zorgt voor optimale runtimeprestaties van Image Serving voor alle toepassingen. Hoewel de server van het Beeld alle brondossierformaten kan verwerken die door IC worden goedgekeurd, verleent Scene7 geen steun voor dergelijk gebruik.

Als u PTIFF-bestanden gebruikt, kunt u aan de hand van de volgende regels met duim bepalen welke ruimte vereist is.

*`total_space`* (bytes) =  *`number_of_images`* x(2000 +  *`avg_pixel_count`* x  *`avg_num_components`* x  *`p_factor`*)

* *`avg_pixel_count`* De gemiddelde pixelgrootte (breedte x hoogte) van alle oorspronkelijke bronafbeeldingen. Als de oorspronkelijke afbeeldingen bijvoorbeeld doorgaans ongeveer 200 x 200 pixels groot zijn, is dit 4 MB pixels.
* *`avg_num_components`* Afhankelijk van het type afbeelding. Voor de meeste RGB-afbeeldingen is dit 3, voor de meeste CMYK- of RGBA-afbeeldingen is het 4. Gebruik 3.5 als de helft van de afbeeldingen RGB is en de andere helft RGBA.
* *`p_factor`* Afhankelijk van het compressietype en de kwaliteit die zijn ingesteld wanneer de afbeeldingen worden omgezet met IC.

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>PTIFF-compressie</b> </th> 
   <th class="entry"> <b><i>p_factor</i></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Niet gecomprimeerd </p> </td> 
   <td> <p> 33 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Compressie vertragen </p> </td> 
   <td> <p> 25-0,75, afhankelijk van de afbeelding </p> </td> 
  </tr> 
  <tr> 
   <td> <p>JPEG-compressie </p> </td> 
   <td> <p> 1 (standaard voor JPEG-kwaliteit 95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Bij deze benadering wordt geen rekening gehouden met overhead van het bestandssysteem. De werkelijke ruimte op de schijf kan aanzienlijk groter zijn.

**Voorbeeld**

Een implementatie van Image Serving verwacht 30.000 oudere afbeeldingen met lage resolutie te gebruiken, met een gemiddelde grootte van 500x500 RGB pixels. Er worden nieuwe afbeeldingsgegevens van afdrukkwaliteit toegevoegd met een snelheid van 10.000 per jaar. De CMYK-afbeeldingsgrootte is standaard 4k x 6k bytes. Alle gegevens worden gecomprimeerd met JPEG van hoge kwaliteit. De totale hoeveelheid schijfruimte na 3 jaar gebruik wordt als volgt geschat:

*`total_space`* = 30.000 x (2k + 0,5k x 0,5k x 3 x 0,1) + 3 x 10.000 x (2k + 4k x 6k x 4 x 0,1) = 2,2 G + 268 GB = ongeveer 270 GB

Voor een gegarandeerde beste kwaliteit kan deflate-compressie (ZIP) worden gebruikt. Veronderstellend *`p_factor`* van 0.4, is de totale vereiste hoeveelheid schijfruimte ongeveer 4 keer groter. In dit geval iets meer dan 1 TB.
