---
description: Hiermee worden opgegeven taaklogbestanden voor het geselecteerde bedrijf opgehaald. U kunt sorteren op tekens, richting, begin- en einddatum en op het aantal rijen.
seo-description: Hiermee worden opgegeven taaklogbestanden voor het geselecteerde bedrijf opgehaald. U kunt sorteren op tekens, richting, begin- en einddatum en op het aantal rijen.
seo-title: getJobLogs
solution: Experience Manager
title: getJobLogs
topic: Dynamic Media Image Production System API
uuid: 850ccfad-6cdb-4eda-a20a-762fadadf8b2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# getJobLogs{#getjoblogs}

Hiermee worden opgegeven taaklogbestanden voor het geselecteerde bedrijf opgehaald. U kunt sorteren op tekens, richting, begin- en einddatum en op het aantal rijen.

Syntaxis

## Toegestane gebruikerstypen {#section-9df82972265d44c9ad91504a17c3ffa6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-8cfdc7994da24678a45edcb37e9a2166}

**Input (getJobLogsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Nee | De handgreep van het bedrijf. |
| `*`userHandle`*` | `xsd:string` | Nee | Hiermee worden logs opgehaald voor taken die door een specifieke gebruiker zijn ingediend. |
| `*`sortBy`*` | `xsd:string` | Nee | Hiermee kunt u sorteervelden selecteren. |
| `*`sortDirection`*` | `xsd:string` | Nee | Sorteervolgorde (oplopend of aflopend). |
| `*`startDate`*` | `xsd:dateTime` | Nee | De datum en tijd van het begin van het taaklogboek. Geef de tijdzone het verzoek voor dit veld. |
| `*`endDate`*` | `xsd:dateTime` | Nee | De datum en tijd van het einde van het taaklogboek. Geef de tijdzone het verzoek voor dit veld. |
| `*`numRows`*` | `xsd:int` | Nee | Maximumaantal rijen dat moet worden geretourneerd. |

**Output (getJobLogsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`jobLogArray`*` | `types: JobLogArray` | Ja | Array met taaklogbestanden. |

## Voorbeelden {#section-35871c94b4a44559912577efddbc46a6}

Deze codesteekproef keert IPS baanlogboeken voor een specifiek bedrijf terug. U kunt het ook gebruiken om taaklogboeken voor een specifieke gebruiker of een bedrijf en een gebruiker terug te keren.

**Verzoek**

```java
<ns1:getJobLogsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getJobLogsParam>
```

**Antwoord**

```java
<getJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobLogArray>
      <items>
         <companyHandle>47</companyHandle>
         <jobHandle>47||Add_2007-09-14-15:04:34</jobHandle>
         <jobName>Add_2007-09-14-15:04:34</jobName>
         <submitUserEmail>kmagnusson@adobe.com</submitUserEmail>
         <logType>BeginUpload</logType>
         <startDate>2007-09-14T22:04:58.536-07:00</startDate>
         <fileSuccessCount>2</fileSuccessCount>
         <fileErrorCount>0</fileErrorCount>
         <fileWarningCount>205</fileWarningCount>
         <fileDuplicateCount>0</fileDuplicateCount>
         <fileUpdateCount>0</fileUpdateCount>
         <totalFileCount>0</totalFileCount>
         <fatalError>false</fatalError>
       </items>
   </jobLogArray>
</getJobLogsReturn>
```

