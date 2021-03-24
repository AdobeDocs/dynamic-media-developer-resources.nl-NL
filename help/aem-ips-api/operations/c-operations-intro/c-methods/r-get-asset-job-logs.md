---
description: Hiermee worden de taaklogbestanden voor een element opgehaald. Items die in de array worden geretourneerd, bevatten gedetailleerde informatie over elke vermelding in het taaklogboek voor dat element. Het reactiegebied logMessage wordt gelokaliseerd gebaseerd op het authHeader gebied.
solution: Experience Manager
title: getAssetJobLogs
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# getAssetJobLogs{#getassetjoblogs}

Hiermee worden de taaklogbestanden voor een element opgehaald. Items die in de array worden geretourneerd, bevatten gedetailleerde informatie over elke vermelding in het taaklogboek voor dat element. Het reactiegebied logMessage wordt gelokaliseerd gebaseerd op het authHeader gebied.

Syntaxis

## Toegestane gebruikerstypen {#section-72b98cdb0f6f47f5aabdc183a45ea577}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-9586617e124b4da4acb6b66b2a9adad8}

**Input (getAssetJobLogsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep van de onderneming waartoe het actief behoort. |
| `*`assetHandle`*` | `xsd:string` | Ja | De greep naar element met de taaklogboeken die moeten worden opgehaald. |

**Output (getAssetJobLogsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`jobLogArray`*` | `types:AssetJobLogArray` | Ja | Taaklogarray. |

## Voorbeelden {#section-f03d7f3ec5d043d38227f926fb7609f6}

In dit codevoorbeeld worden de taaklogbestanden van een bepaald element opgehaald. De reactie retourneert een taaklogarray met gedetailleerde informatie over alle taken waarin het element is gebruikt.

**Verzoek**

```java
<getAssetJobLogsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetJobLogsParam>
```

**Antwoord**

```java
<getAssetJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <jobLogArray>
      <items>
         <jobHandle>j|6||Add_2007-10-24-16:11:07</jobHandle>
         <jobName>Add_2007-10-24-16:11:07</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS</logMessage>
         <logType>UploadSuccess</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2007-10-24T16:12:32.297-07:00</logDate>
      </items>
      <items>
         <jobHandle>j|6||submitServerUploadJob40_2008-06-11-11:38</jobHandle>
         <jobName>submitServerUploadJob40_2008-06-11-11:38</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS.</logMessage>
         <logType>FileUpdated</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2008-06-11T11:38:48.547-07:00</logDate>
      </items>
   </jobLogArray>
</getAssetJobLogsReturn>
```

