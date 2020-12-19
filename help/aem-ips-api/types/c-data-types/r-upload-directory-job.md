---
description: Hiermee worden bestanden op terugkerende basis geüpload uit opgegeven servermappen.
seo-description: Hiermee worden bestanden op terugkerende basis geüpload uit opgegeven servermappen.
seo-title: UploadDirectoryJob
solution: Experience Manager
title: UploadDirectoryJob
topic: Scene7 Image Production System API
uuid: 6e6ae415-7c54-4bbb-aa98-ff9a77d956b0
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---


# UploadDirectoryJob{#uploaddirectoryjob}

Hiermee worden bestanden op terugkerende basis geüpload uit opgegeven servermappen.

Syntaxis

## Parameters {#section-69c07f4e7b2e4a0fba143ffaa9f4d48f}

<table id="table_6E40A78846F444BDB8E437413B90CFCE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Naam </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:AutoColorOptions</span> </td> 
   <td colname="col3"> <p>Opties voor automatisch uitsnijden van afbeeldingen (op basis van kleur). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>Array met automatische ingestelde generatiescripts die moeten worden toegepast op geüploade bestanden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>Hiermee verwijdert u op basis van transparantie witruimte uit de randen van afbeeldingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>Opties die u kunt opgeven tijdens het uploaden. De set bepaalt hoe de kleur wordt beheerd voor het uploaden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> <p>Bepaalt of een masker wordt gemaakt tijdens het uploaden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> <p>IPS-map voor de bestanden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> <p>Keuze van e-mailinstellingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:IllustratorOptions</span> </td> 
   <td colname="col3"> <p>Opties voor het uploaden van Illustrator-bestanden naar de afbeeldingsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> <p>Of submappen moeten worden opgenomen tijdens het uploaden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:InDesignOptions</span> </td> 
   <td colname="col3"> <p>Opties voor het uploaden van InDesign-bestanden naar de server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>Masker de achtergrond voor geselecteerde afbeeldingen. Hierdoor kunt u ze in andere lagen bedekken met transparantie buiten de afbeelding van het onderwerp. </p> <p>Optioneel. </p> <p>Zie <a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>Opties voor handmatig uitsnijden van afbeeldingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:MediaOptions</span> </td> 
   <td colname="col3"> <p>Opties waarmee u een miniatuurafbeelding van de video kunt instellen. </p> <p>Zie <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> overschrijven</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> <p>Opties voor het uploaden van bestanden overschrijven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:PDFOptions</span> </td> 
   <td colname="col3"> <p>Opties voor het uploaden van PDF-bestanden naar de afbeeldingsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> PhotoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>Opties voor het uploaden van Photoshop-bestanden naar de afbeeldingsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> <p>De URL van de bestemming voor het uploaden van het bestand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> </span> </span>postImageRenderingPublishJob </td> 
   <td colname="col2"> <span class="codeph"> typen:ImageRendingPublishJob</span> </td> 
   <td colname="col3"> <p>Details voor een publicatietaak voor het renderen van afbeeldingen die wordt uitgevoerd nadat het uploaden is voltooid. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:ImageServingPublishJob</span> </td> 
   <td colname="col3"> <p>Details voor een publicatietaak voor afbeeldingen die wordt uitgevoerd nadat het uploaden is voltooid. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> <p>Of alleen bestanden moeten worden geüpload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:PostScriptOptions</span> </td> 
   <td colname="col3"> <p>Opties voor het uploaden van PostScript-bestanden naar de afbeeldingsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:VideoPublishJob</span> </td> 
   <td colname="col3"> <p>Details voor een video-publicatietaak die wordt uitgevoerd nadat het uploaden is voltooid. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> <p>Hiermee regelt u het behoud van bestaande uitsnijddefinities. Heeft als standaardwaarde true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> <p>Bepaalt of de publicatiestatus van een bestaand element behouden blijft wanneer het wordt overschreven. Als deze niet is ingesteld, wordt de standaardinstelling van het bedrijf gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> processMetadataFiles</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> <p>Of er afzonderlijke XML-metagegevensbestanden voor deze taak moeten worden verwerkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3"> <p>Array met projecthandgrepen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> <p>Hiermee wordt bepaald of bestanden zijn gemarkeerd als klaar voor publicatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDir</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> <p>Bron uploadmap. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:UnCompressOptions</span> </td> 
   <td colname="col3"> <p>Pak de inhoud van geüploade TAR-/ZIP-bestanden op met deze optionele instellingen en verwerk deze. </p> <p>Zie <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>Opties waarmee u onscherpe maskerinstellingen kunt bepalen wanneer u een geoptimaliseerd TIF-bestand voor piramide maakt. Gebruik deze instellingen om de scherpte van de afbeelding te verbeteren. </p> <p>Zie <a href="https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> xmpKeywords</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>Een extra metagegevensoptie voor alles in de uploadtaak </p> </td> 
  </tr> 
 </tbody> 
</table>

## Notities {#section-637405ff7e0b4a71b83fd359b92fa0c2}

Voor `CropOptions` kunt u slechts een van de volgende opties kiezen:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Voor `PublishJob` kunt u slechts een van de volgende opties kiezen:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`

