---
description: Hiermee worden opgegeven taaklogbestanden voor het geselecteerde bedrijf opgehaald. U kunt sorteren op tekens, richting, begin- en einddatum en op het aantal rijen.
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 6239c3c4-bdbc-4e69-82d4-48a76f080eff
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# getJobLogs{#getjoblogs}

Hiermee worden opgegeven taaklogbestanden voor het geselecteerde bedrijf opgehaald. U kunt sorteren op tekens, richting, begin- en einddatum en op het aantal rijen.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-9df82972265d44c9ad91504a17c3ffa6}

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
