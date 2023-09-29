---
title: Vereisten en aanbevelingen voor schijfruimte
description: Naast de ruimte die nodig is om de software te installeren, gelden voor Image Serving de volgende vereisten voor schijfruimte.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Vereisten en aanbevelingen voor schijfruimte{#disk-space-requirements-and-recommendations}

Naast de ruimte die nodig is om de software te installeren, heeft Image Serving de volgende vereisten voor schijfruimte:

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
   <td> <p><b>Bronafbeeldingen, lettertypen, ICC-profielen</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/images </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS:RootPaths </span> </p> </td> 
   <td> <p>Varieert; zie onderstaande opmerkingen. </p> </td> 
   <td> <p>Alleen toegankelijk moeten zijn voor de imageserver; de servers wijzigen nooit gegevens. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP-responsgegevenscache</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/is-response </span> </p> <p> <span class="codeph"> PS:ResponseCacheFolders </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize </span> x 2; ten minste 2 GB aanbevolen. </p> </td> 
   <td> <p>In deze cache worden ook geneste/ingesloten gegevens en externe bronafbeeldingen opgeslagen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Gegevenscache afbeeldingscatalogus</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/catalogus </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder </span> </p> </td> 
   <td> <p>Laat de catalogusmap 1,5x de ruimte gebruiken. </p> </td> 
   <td> <p>Wordt gevuld wanneer catalogi aanvankelijk worden geladen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Loggegevens</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/logs </span> </p> <p> <span class="codeph"> PS:LogFolder </span> </p> <p> <span class="codeph"> IS:LogFile </span> </p> <p> <span class="codeph"> SV::LogFile </span> </p> </td> 
   <td> <p>100 MB of meer. </p> </td> 
   <td> <p>Het varieert afhankelijk van de registrerenconfiguratie en het servergebruik. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Tijdelijke bestanden afbeeldingsserver</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/temp </span> </p> <p> <span class="codeph"> IS:TempDirectory </span> </p> <p> <span class="codeph"> SV:TempDirectory </span> </p> </td> 
   <td> <p>100 MB is voldoende voor de meeste toepassingen. </p> </td> 
   <td> <p>Gegevens van korte duur; mogelijk vereist voor andere bronafbeeldingen dan PTIFF's en bepaalde indelingen voor reactieafbeeldingen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Vereisten voor schijfruimte voor bronafbeeldingen {#section-317da75099ad480d9a461c7e706d4f1c}

Adobe raadt u aan alle bronafbeeldingen om te zetten in de PTIFF-bestandsindeling (piramid TIFF file format) met behulp van het opdrachtregelprogramma voor het omzetten van afbeeldingen (IC). Deze conversie zorgt voor optimale runtimeprestaties van Image Serving voor alle toepassingen. Hoewel de server van het Beeld alle brondossierformaten kan verwerken die door IC worden goedgekeurd, steunt Dynamic Media niet voor dergelijk gebruik.

Als u PTIFF-bestanden gebruikt, kunt u aan de hand van de volgende regels met duim bepalen welke ruimte vereist is.

*`total_space`* (bytes) = *`number_of_images`*  × (2000 + *`avg_pixel_count`* x *`avg_num_components`*  ×  *`p_factor`*)

* *`avg_pixel_count`* De gemiddelde pixelgrootte (breedte x hoogte) van alle oorspronkelijke bronafbeeldingen. Als de oorspronkelijke afbeeldingen bijvoorbeeld doorgaans ongeveer 2k × 2k pixels zijn, is dit 4 megapixels.
* *`avg_num_components`* Afhankelijk van het type afbeelding. Voor de meeste RGB-afbeeldingen is dit 3; voor de meeste CMYK- of RGBA-afbeeldingen is het 4. Gebruik 3.5 als de helft van de afbeeldingen RGB is en de andere helft RGBA.
* *`p_factor`* Afhankelijk van het compressietype en de kwaliteit die zijn ingesteld wanneer de afbeeldingen worden geconverteerd met IC.

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
   <td> <p> 1 (standaard voor kwaliteit JPEG 95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze benadering houdt geen rekening met overhead van het bestandssysteem. De werkelijke ruimte op de schijf kan aanzienlijk groter zijn.

**Voorbeeld**

Een implementatie van Image Serving verwacht 30.000 oudere images met lage resolutie te gebruiken, met een gemiddelde grootte van 500 × 500 RGB pixels. Nieuwe afbeeldingsgegevens van afdrukkwaliteit worden met een snelheid van 10.000 per jaar toegevoegd. De CMYK-afbeeldingsgrootte is standaard 4k × 6k bytes. Alle gegevens worden met hoge kwaliteit JPEG gecomprimeerd. De totale hoeveelheid schijfruimte na drie jaar gebruik wordt als volgt geschat:

*`total_space`* = 30,000 × (2k + 0,5k × 0,5k × 3 × 0,1) + 3 × 10,000 × (2k + 4k × 6k × 4 × 0,1) = 2,2 G + 268 GB = ongeveer 270 GB

Om de beste kwaliteit te garanderen, kan een compressie zoals .zip worden gebruikt. Ervan uitgaande dat *`p_factor`* van 0,4 is de totale benodigde schijfruimte ongeveer vier keer groter. In dit geval iets meer dan 1 terabyte.
