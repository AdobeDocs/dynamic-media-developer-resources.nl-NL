---
description: Groepeer bestanden in sets met behulp van een lijst met elementen.
seo-description: Groepeer bestanden in sets met behulp van een lijst met elementen.
seo-title: AutomatedSetGenerationJob
solution: Experience Manager
title: AutomatedSetGenerationJob
topic: Scene7 Image Production System API
uuid: 9c664bde-a731-4d6b-ae6b-c862bda02d4c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---


# AutomatedSetGenerationJob{#automatedsetgenerationjob}

Groepeer bestanden in sets met behulp van een lijst met elementen.

Syntaxis

## Parameters {#section-939b2e6946a64238be3709fec2cd0b84}

<table id="table_0E031B2014B646BDA2A94D7E0B55DD5B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Naam </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3">Een array met elementhandgrepen die wordt gebruikt om de set te maken. <p>Standaard is 1000 het maximale aantal elementen dat u in de array kunt opnemen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Pad naar de map waarin u de sets wilt opslaan. Hiermee wordt standaard naar de hoofdmap van het bedrijf opgeslagen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Hiermee stelt u een markering in die aangeeft of de elementen moeten worden gepubliceerd of niet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:AutoSetCreationOptions</span> </td> 
   <td colname="col3">Een array met ingestelde generatiescripts die u kunt uitvoeren op de geüploade bestanden. Zie <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> <p>Stel een geautomatiseerde e-mailmelding in voor de taak. </p> </td> 
  </tr> 
 </tbody> 
</table>

**e-mailinstellingsopties**

De parameter `emailSetting` bevat de volgende opties:

| Option | Retourneert |
|---|---|
| `All` | Alle taakmeldingen (fouten, waarschuwingen, voltooiing) aan de opgegeven ontvanger. |
| `Error` | Taakfouten naar de opgegeven ontvanger. |
| `ErrorAndWarning` | Taakfouten en -waarschuwingen voor de opgegeven ontvanger. |
| `JobCompletion` | Een bericht voor het voltooien van een taak aan de opgegeven ontvanger. |
| `None` | De taak verzendt geen taakmeldingen naar de opgegeven ontvanger. |

## Voorbeeld {#section-d01ee7671f274a1fa12737e8df91d2cf}

```
<complexType name="AutomatedSetGenerationJob">
  <sequence>
    <element name="assetHandleArray" type="types:HandleArray"/>
    <element name="destFolder" type="xsd:string" minOccurs="0"/>
    <element name="readyForPublish" type="xsd:boolean"/>
    <element name="autoSetCreationOptions" type="types:AutoSetCreationOptions"/>
    <element name="emailSetting" type="xsd:string"/>
  </sequence>
</complexType>
```

