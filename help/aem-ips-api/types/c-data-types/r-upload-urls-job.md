---
description: Hiermee uploadt u URL's vanaf de locatie waar u bestanden wilt ophalen.
seo-description: Hiermee uploadt u URL's vanaf de locatie waar u bestanden wilt ophalen.
seo-title: UploadUrlsJob
solution: Experience Manager
title: UploadUrlsJob
topic: Scene7 Image Production System API
uuid: 6140e969-bf61-4b62-9a60-29609626b0b4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---


# UploadUrlsJob{#uploadurlsjob}

Hiermee uploadt u URL&#39;s vanaf de locatie waar u bestanden wilt ophalen.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Naam </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:AutoColorCropOptions</span> </td> 
   <td colname="col3"> Opties voor het automatisch uitsnijden van afbeeldingen op basis van kleur. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:AutoSetCreationOptions</span> </td> 
   <td colname="col3"> Array met automatische ingestelde generatiescripts die moeten worden toegepast op geüploade bestanden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> Hiermee verwijdert u op basis van transparantie witruimte uit de randen van afbeeldingen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Of een masker moet worden gemaakt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:ColorManagementOptions</span> </td> 
   <td colname="col3"> Opties die u kunt opgeven tijdens het uploaden. De set bepaalt hoe de kleur wordt beheerd voor het uploaden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Keuze van e-mailinstellingen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:IllustratorOptions</span> </td> 
   <td colname="col3"> Opties voor het uploaden van Illustrator-bestanden naar de afbeeldingsserver. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:InDesignOptions</span> </td> 
   <td colname="col3"> Opties voor het uploaden van InDesign-bestanden naar de server. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3">Masker de achtergrond voor geselecteerde afbeeldingen. Hierdoor kunt u ze in andere lagen bedekken met transparantie buiten de afbeelding van het onderwerp. Optioneel. Zie<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ManualCropOptions</span> </td> 
   <td colname="col3"> Opties voor het handmatig uitsnijden van afbeeldingen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:MediaOptions</span> </td> 
   <td colname="col3">Opties waarmee u een miniatuurafbeelding van de video kunt instellen. Zie <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numUrls</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3">Retourneert het aantal URL's dat in een taak is verzonden. Wordt gebruikt door <a href="../../operations/c-operations-intro/c-methods/r-get-active-jobs.md#reference-67483cbd71d04042b48434d886e8a7a0" format="dita" scope="local"> getActiveJobs</a> en <a href="../../operations/c-operations-intro/c-methods/r-get-scheduled-jobs.md#reference-2bab1861325f4bff84c879d1efa9146e" format="dita" scope="local"> getScheduledJobs</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> overschrijven</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Of bestanden tijdens het uploaden moeten worden overschreven. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:PDFOptions</span> </td> 
   <td colname="col3"> Opties voor het uploaden van PDF-bestanden naar de afbeeldingsserver. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> PhotoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:PhotoshopOptions</span> </td> 
   <td colname="col3"> Opties voor het uploaden van Photoshop-bestanden naar de afbeeldingsserver. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> De URL waar de bestanden worden geüpload. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:ImageRendingPublishJob</span> </td> 
   <td colname="col3"> Details voor een publicatietaak voor het renderen van afbeeldingen die wordt uitgevoerd nadat het uploaden is voltooid. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Alle mediaopties. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:PostScriptOptions</span> </td> 
   <td colname="col3"> Opties voor het uploaden van PostScript-bestanden naar de afbeeldingsserver. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:VideoPublishJob</span> </td> 
   <td colname="col3"> Details voor een video-publicatietaak die wordt uitgevoerd nadat het uploaden is voltooid. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Hiermee regelt u het behoud van bestaande uitsnijddefinities. Is standaard ingesteld op true </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Bepaalt of de publicatiestatus van een bestaand element behouden blijft wanneer het wordt overschreven. Als deze niet is ingesteld, wordt de standaardinstelling van het bedrijf gebruikt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3"> Array met projecthandgrepen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Hiermee wordt aangegeven of de bestanden klaar zijn voor publicatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:UnCompressOptions</span> </td> 
   <td colname="col3">Pak de inhoud van geüploade TAR-/ZIP-bestanden op met deze optionele instellingen en verwerk deze. Zie <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:UnsharpMaskOptions</span> </td> 
   <td colname="col3">Opties waarmee u onscherpe maskerinstellingen kunt bepalen wanneer u een geoptimaliseerd TIF-bestand voor piramide maakt. Gebruik deze instellingen om de scherpte van de afbeelding te verbeteren. Zie <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> urlArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:UrlArray</span> </td> 
   <td colname="col3"> Een array van URL's die u wilt uploaden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmpKeywords</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> <p>Een extra metagegevensoptie voor alles in de uploadtaak. </p> </td> 
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

