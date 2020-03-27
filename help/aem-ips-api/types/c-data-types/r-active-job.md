---
description: Een taak die op een server wordt uitgevoerd. Het is ook een instantie van een geplande taak.
seo-description: Een taak die op een server wordt uitgevoerd. Het is ook een instantie van een geplande taak.
seo-title: ActiveJob
solution: Experience Manager
title: ActiveJob
topic: Scene7 Image Production System API
uuid: d7120a88-6f3e-4844-aafa-83d419470fad
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ActiveJob{#activejob}

Een taak die op een server wordt uitgevoerd. Het is ook een instantie van een geplande taak.

Banen bestaan in drie staten:

* Gepland om te worden uitgevoerd.
* Wordt momenteel uitgevoerd.
* Voltooid (en heeft reeds informatie aan een baanlogboek geschreven).

Geef een waarde voor het taaktype op om het taaktype te retourneren. U kunt de volgende taken retourneren:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublish`
* `JobUploadDirectoryJob`
* `uploadUrlsJob`

## Parameters {#section-6590fe864a434000822b9ec384784512}

<table id="table_1C4DDAB4EB1341FDA92B6F14E0132F75"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Naam </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> bedrijfshandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Handgreep aan het bedrijf. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taakhandgreep</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Handgreep aan de baan. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> naam</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> De unieke naam voor de taak. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> originalName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3">Oorspronkelijke naam van het <span class="codeph"> ActiveJob</span> -type dat samen met de taak is verzonden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Keuze van taaktypen die door het systeem worden geretourneerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> status</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Keuze van actieve taakstaten die door het systeem worden geretourneerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> e-mailadres van de gebruiker die de taak heeft gepland. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> landinstelling</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3">De landinstelling voor de gegevens van het taaklogboek en de e-maillokalisatie. <p>Geef landinstellingen op als <span class="codeph"> &lt;language_code&gt;[-&lt;country_code&gt;]</span>, waarbij de taalcode een code van twee kleine letters is, zoals gespecificeerd in ISO-639, en de optionele landcode een code van twee letters in hoofdletters is, zoals gespecificeerd in ISO-3166. De landinstelling voor Engels (Verenigde Staten) zou bijvoorbeeld als volgt zijn: <span class="codeph"> en-US</span>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> beschrijving</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3">Functiebeschrijving die oorspronkelijk is opgegeven in <span class="codeph"> submitJob</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> servernaam</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Naam van de server waarop de taak wordt uitgevoerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> begindatum</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Datum, tijd en tijdzone voor de actieve taak. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> totale grootte</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Totale grootte van de actieve taak. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> voortgang</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Voortgang van de taak (d.w.z. hoe dicht de taak bij voltooiing is). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> A text message that describes job progress. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Datum, tijd en tijdzone van de laatste voortgangsupdate. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskProgressArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:TaskProgressArray</span> </td> 
   <td colname="col3"> Voortgangsgegevens asynchrone taak. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typen:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Taakdetails voor een afbeelding die publicatietaak aanbiedt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingRenderJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageServingRenderJob</span> </td> 
   <td colname="col3"> Taakdetails voor een publicatietaak voor afbeeldingen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typen:VideoPublishJob</span> </td> 
   <td colname="col3"> Taakdetails voor een video-publicatietaak. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typen:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Taakgegevens voor de publicatietaak van een servermap. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:UploadUrlsJob</span> </td> 
   <td colname="col3"> Taakgegevens voor een upload-URL's-taak. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:RipPDFSJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typen:OptimizeImagesJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:ReprocessAssetsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadPostJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typen:UploadPostJob</span> </td> 
   <td colname="col3"> Uploaden naar het bureaublad voor het bijhouden van taakdetails. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typen:ExportJob</span> </td> 
   <td colname="col3">Toestaan dat eerder geüploade bestanden zijn geëxporteerd. Zie Taak <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exportjob.html" format="http" scope="external"></a>exporteren. </td> 
  </tr> 
 </tbody> 
</table>

