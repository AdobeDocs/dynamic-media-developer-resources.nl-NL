---
description: Gebruikt getActiveJobs om bureaubladuploads bij te houden.
seo-description: Gebruikt getActiveJobs om bureaubladuploads bij te houden.
seo-title: UploadPostJob
solution: Experience Manager
title: UploadPostJob
topic: Scene7 Image Production System API
uuid: 172f47c7-685a-4014-9c30-dacd78733655
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UploadPostJob{#uploadpostjob}

Gebruikt getActiveJobs om bureaubladuploads bij te houden.

Zie ook Elementen [uploaden via HTTP POST&#39;s naar Upload...](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>Alle POST-aanvragen voor een uploadtaak moeten afkomstig zijn van hetzelfde IP-adres.

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Naam </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col03" class="entry"> <p>Vereist? </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typen:AutoColorCropOptions</span> </td> 
   <td colname="col03"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Opties voor het automatisch uitsnijden van afbeeldingen op basis van kleur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typen:AutoSetCreateOptions</span> </td> 
   <td colname="col03"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Array met automatische ingestelde generatiescripts die moeten worden toegepast op geüploade bestanden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typen:AutoTransparentCropOptions</span> </td> 
   <td colname="col03"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Hiermee verwijdert u op basis van transparantie witruimte uit de randen van afbeeldingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typen:ColorManagementOptions</span> </td> 
   <td colname="col03"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Opties die u kunt opgeven tijdens het uploaden. De set bepaalt hoe de kleur wordt beheerd voor het uploaden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col03"> <p><b>Ja</b> </p> </td> 
   <td colname="col3"> <p>Of een masker moet worden gemaakt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> E- <span class="varname"> mailinstelling</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col03"> <p><b>Ja</b> </p> </td> 
   <td colname="col3"> <p>Keuze van e-mailinstellingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typen:InDesignOptions</span> </td> 
   <td colname="col03"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Opties voor het uploaden van InDesign-bestanden naar de afbeeldingsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Illustrator-opties</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typen:IllustratorOptions</span> </td> 
   <td colname="col03"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Opties voor het uploaden van Illustrator-bestanden naar de afbeeldingsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:KnockoutBackgroundOptions</span> </td> 
   <td colname="col03"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Masker de achtergrond voor geselecteerde afbeeldingen. Hierdoor kunt u ze in andere lagen bedekken met transparantie buiten de afbeelding van het onderwerp. Optioneel. </p> <p>Zie<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:ManualCropOptions</span> </td> 
   <td colname="col03"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Opties voor het handmatig uitsnijden van afbeeldingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> MediaOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typen:MediaOptions</span> </td> 
   <td colname="col03"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Opties waarmee u een miniatuurafbeelding van de video kunt instellen. </p> <p>Zie <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> overschrijven</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col03"> <p><b>Ja</b> </p> </td> 
   <td colname="col3"> <p>Of bestanden tijdens het uploaden moeten worden overschreven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typen:PDFOptions</span> </td> 
   <td colname="col03"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Opties voor het uploaden van PDF-bestanden naar de afbeeldingsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Photoshop-opties</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typen:PhotoshopOptions</span> </td> 
   <td colname="col03"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Opties voor het uploaden van Photoshop-bestanden naar de afbeeldingsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col03"> <p>Nee </p> </td> 
   <td colname="col3"> <p>De URL waar de bestanden worden geüpload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typen:PostScriptOptions</span> </td> 
   <td colname="col03"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Opties voor het uploaden van PostScript-bestanden naar de afbeeldingsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> Uitsnijden <span class="varname"></span> behouden </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col03"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Hiermee regelt u het behoud van bestaande uitsnijddefinities. Standaardwaarden zijn waar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col03"> <p><b>Ja</b> </p> </td> 
   <td colname="col3"> <p>Bepaalt of de publicatiestatus van een bestaand element behouden blijft wanneer het wordt overschreven. Als deze niet is ingesteld, wordt de standaardinstelling van het bedrijf gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col03"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Array met projecthandgrepen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col03"> <p><b>Ja</b> </p> </td> 
   <td colname="col3"> <p>Hiermee wordt aangegeven of de bestanden klaar zijn voor publicatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:UnCompressOptions</span> </td> 
   <td colname="col03"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Pak de inhoud van geüploade TAR-/ZIP-bestanden op met deze optionele instellingen en verwerk deze. </p> <p>Zie <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:UnsharpMaskOptions</span> </td> 
   <td colname="col03"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Opties waarmee u onscherpe maskerinstellingen kunt bepalen wanneer u een geoptimaliseerd TIF-bestand voor piramide maakt. Gebruik deze instellingen om de scherpte van de afbeelding te verbeteren. </p> <p>Zie <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col03"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Een extra metagegevensoptie voor alles in de uploadtaak. </p> </td> 
  </tr> 
 </tbody> 
</table>

