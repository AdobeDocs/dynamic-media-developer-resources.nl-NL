---
description: Hiermee wordt een taak naar het systeem verzonden.
seo-description: Hiermee wordt een taak naar het systeem verzonden.
seo-title: submitJob
solution: Experience Manager
title: submitJob
topic: Scene7 Image Production System API
uuid: d3a83b59-bcd7-4ae9-b1ee-e515fc3c9261
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---


# submitJob{#submitjob}

Hiermee wordt een taak naar het systeem verzonden.

Syntaxis

## Toegestane gebruikerstypen {#section-eb7024277bec43c79e03f396205be16f}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-31a07dbccf964850883e817384499459}

**Input (submitJobParam)**

<table id="table_9CB1F668E036422E8CE4E0BBA42EC44C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Naam </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Vereist </p> </th> 
   <th colname="col4" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>Bedrijfshandgreep. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p>Handgreep naar de gebruiker die de taak heeft verzonden. </p> <p> <p>Opmerking: Het systeem verzendt e-mail naar de gebruiker die door <span class="codeph"> userHandle</span> wordt gespecificeerd. Als <span class="codeph"> userHandle</span> niet wordt verstrekt, ontvangt de persoon die de baan indiende de e-mails. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>Taaknaam. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> landinstelling</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p>De landinstelling die wordt gebruikt voor loggegevens van taken en e-maillokalisatie. </p> <p>Landinstellingen worden opgegeven als <span class="codeph"> &lt;language_code&gt;</span> en <span class="codeph"> [&lt;country_code&gt;]</span>, waarbij de taalcode een code van twee letters in kleine letters is, zoals gespecificeerd door ISO-639, en de optionele landcode een code van twee letters in hoofdletters is, zoals gespecificeerd door ISO-3166. De landinstelling voor Engels (Verenigde Staten) zou bijvoorbeeld als volgt zijn: en-US. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p>Datum en tijd waarop de taak moet worden uitgevoerd. </p> <p>Opmerking:  Geef de tijdzone het verzoek. De streken van de tijd worden aangepast aan de tijdzone van de doelIPS server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p>Hiermee bepaalt u wanneer de taak moet worden uitgevoerd. </p> <p> Kan een <span class="codeph"> cron</span> koord zijn dat de baan op een terugkomende basis in werking stelt. </p> <p>Het programma is altijd relatief ten opzichte van de lokale tijdzone van de server. Zie de IPS documentatie voor het formaat van het douaneschema. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> beschrijving</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p>Taakbeschrijving. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:ExportJob</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p>Eerder geüploade bestanden exporteren. </p> <p>Zie <a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local"> ExportJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p>Details voor een afbeelding die publicatietaak aanbiedt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p>Details voor een publicatietaak voor het renderen van afbeeldingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:VideoPublishJob</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p>Details voor een video-publicatietaak. </p> <p>Zie <a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> VideoPublishJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p>Details voor de publicatietaak van een serverdirectory. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadDirectoryJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:UploadDirectoryJob</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p>Details voor een uploadmaptaak. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:UploadUrlsJob</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p>Details voor een URL-uploadtaak. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:OptimizeImagesJob</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:RipPDFSJob</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ReprocessAssetsJob</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> automatedSetGenerationJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p>Verwerk een elementenlijst in sets met behulp van Geautomatiseerde setscripts. </p> <p>Zie <a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> AutomatedSetGenerationJob</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Uitvoer (submitJobReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`jobHandle`*` | `xsd:string` | Ja | Taakgreep. |

## Voorbeelden {#section-40ac77d14adf4588ba2575be6879b2d2}

Dit codevoorbeeld legt een beeld serend publiceerbaan aan IPS voor en keert een baanhandvat terug. Kies slechts één type taak in de aanvraag. Omdat `userHandle` is weggelaten, worden e-mailmeldingen verzonden naar de gebruiker die de taak heeft verzonden. Deze voorbeeldtaak wordt onmiddellijk uitgevoerd omdat `execTime` en `execSchedule` zijn weggelaten.

**Verzoek**

```java
<submitJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobName>My Test Job</jobName>
   <imageServingPublishJob>
      <publishType>Full</publishType>
      <emailSetting>Error</emailSetting>
   </imageServingPublishJob>
</submitJobParam>
```

**Antwoord**

```java
<submitJobReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobHandle>47|My Test Job|</jobHandle>
</submitJobReturn>
```

## Notities {#section-0f3078e503a249aeb6f3d662a51f036a}

U kunt hoogstens één van `execTime` en `execSchedule` specificeren. Als geen van beide is geslaagd, wordt de taak onmiddellijk uitgevoerd. U kunt slechts één van het volgende gebruiken:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`

