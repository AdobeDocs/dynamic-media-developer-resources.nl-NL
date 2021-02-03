---
description: Taaktype waarmee eerder geüploade primaire bestanden opnieuw kunnen worden verwerkt, waaronder het terugzetten van PDF's en het opnieuw optimaliseren van afbeeldingen.
seo-description: Taaktype waarmee eerder geüploade primaire bestanden opnieuw kunnen worden verwerkt, waaronder het terugzetten van PDF's en het opnieuw optimaliseren van afbeeldingen.
seo-title: ReprocessAssetsJob
solution: Experience Manager
title: ReprocessAssetsJob
topic: Dynamic Media Image Production System API
uuid: 5b4aa838-0fb4-4ae8-be5a-8ce1e1487127
translation-type: tm+mt
source-git-commit: d38df1eb4713c034727ad0eb10834dc156122beb
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 0%

---


# ReprocessAssetsJob{#reprocessassetsjob}

Taaktype waarmee eerder geüploade primaire bestanden opnieuw kunnen worden verwerkt, waaronder het terugzetten van PDF&#39;s en het opnieuw optimaliseren van afbeeldingen.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Naam </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Asset handle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> readyForPublish</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:Boolean</span> </p> </td> 
   <td colname="col3"> <p>Hiermee wordt aangegeven of de bestanden klaar zijn voor publicatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:Boolean</span> </p> </td> 
   <td colname="col3"> <p>Bepaalt of de publicatiestatus van een bestaand element behouden blijft wanneer het wordt overschreven. Als deze niet is ingesteld, wordt de standaardinstelling van het bedrijf gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:Boolean</span> </p> </td> 
   <td colname="col3"> <p>Of een masker moet worden gemaakt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:Boolean</span> </p> </td> 
   <td colname="col3"> <p>Hiermee regelt u het behoud van bestaande uitsnijddefinities. De standaardwaarde is true.</p> <p>Als u de parameter manualCropOptions en de bijbehorende waarden opgeeft, worden de nieuwe waarden (behalve 0,0,0,0) toegepast op het element, ongeacht de waarde preserveCrop.</p><p>Als u <i>not</i> de parameter manualCropOptions verstrekt, wordt de waarde van preserveCrop gehandhaafd. En in het geval van true blijven de bestaande preserveCrop-waarden behouden. in het geval van false worden de waarden preserveCrop verwijderd.</p><p>Voorbeeld:</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />    &lt;left&gt;190&lt;/left&gt;<br />    &lt;right&gt;310&lt;/right&gt;<br />    &lt;top&gt;160&lt;/top&gt;<br />    &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Opties voor handmatig uitsnijden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Opties voor het automatisch uitsnijden van afbeeldingen op basis van kleur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Hiermee verwijdert u op basis van transparantie witruimte uit de randen van afbeeldingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> PhotoshopOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>Opties voor het uploaden van Photoshop-bestanden naar de afbeeldingsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>Opties voor het uploaden van PostScript-bestanden naar de afbeeldingsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>Opties voor het uploaden van PDF-bestanden naar de afbeeldingsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>Opties voor A/V-mediabestanden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>Opties voor het uploaden van Illustrator-bestanden naar de afbeeldingsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>Opties die u kunt opgeven tijdens het uploaden. De set bepaalt hoe de kleur wordt beheerd voor het uploaden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>Array met automatische ingestelde generatiescripts die moeten worden toegepast op geüploade bestanden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Een array met projecthandgrepen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>Opties voor e-mailinstellingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:Boolean</span> </p> </td> 
   <td colname="col3"> <p>Of alleen bestanden moeten worden geüpload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>URL naar uploadlocatie van bestand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Taakgegevens voor een publicatietaak die wordt uitgevoerd nadat het uploaden is voltooid. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Taakgegevens voor een publicatietaak voor het renderen van afbeeldingen die moet worden uitgevoerd nadat het uploaden is voltooid. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Taakgegevens voor een publicatietaak voor video die moet worden uitgevoerd nadat het uploaden is voltooid. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Opties voor het uploaden van InDesign-bestanden naar de afbeeldingsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Masker de achtergrond voor geselecteerde afbeeldingen. Hierdoor kunt u ze in andere lagen bedekken met transparantie buiten de afbeelding van het onderwerp. </p> <p>Optioneel. </p> <p>Zie<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:UnsharpMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>Opties waarmee u onscherpe maskerinstellingen kunt bepalen wanneer u een geoptimaliseerd TIF-bestand voor piramide maakt. Gebruik deze instellingen om de scherpte van de afbeelding te verbeteren. </p> <p>Zie <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Notities**

De opties voor `*CropOptions` omvatten:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

De opties voor `*PublishJob` omvatten:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`

