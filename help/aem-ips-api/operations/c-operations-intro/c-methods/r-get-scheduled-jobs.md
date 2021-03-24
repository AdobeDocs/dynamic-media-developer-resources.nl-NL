---
description: Hiermee worden taken opgehaald die zijn gepland voor uitvoering.
solution: Experience Manager
title: getScheduledJobs
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---


# getScheduledJobs{#getscheduledjobs}

Hiermee worden taken opgehaald die zijn gepland voor uitvoering.

Syntaxis

## Toegestane gebruikerstypen {#section-bd1835ab508a429f8143b3bdb811d6a4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-2af604ff8282460990b9237158187f8f}

**Input (getScheduledJobsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf. |
| `*`jobHandle`*` | `xsd:string` | Nee | Taakgreep. |
| `*`originalName`*` | `xsd:string` | Nee | De naam die wordt opgegeven door `submitJob`. |

**Output (getScheduledJobsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`jobArray`*` | `types:ScheduledJobArray` | Ja | Array met geplande taken. |

## Voorbeelden {#section-e79e7da86ba848fd9996aa36de462e6c}

Dit codevoorbeeld retourneert alle geplande taken in een taakarray. De array zelf bevat gedetailleerde informatie over de taken.

**Verzoek**

```java
<getScheduledJobsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>0</companyHandle>
</getScheduledJobsParam>
```

**Antwoord**

```java
<getScheduledJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray>
      <items>
         <companyHandle>0</companyHandle>
         <jobHandle>0|Cleanup|</jobHandle>
         <name>Cleanup</name>
         <originalName></originalName>
         <type>Cleanup</type>
         <submitUserEmail>default@scene7.com</submitUserEmail>
         <execSchedule>00 00 00 * * </execSchedule>
         <nextFireTime>2007-10-13T00:00:00.000-07:00</nextFireTime>
         <timeZone>PST</timeZone>
         <triggerState>Paused</triggerState>
      </items>
   </jobArray>
</getScheduledJobsReturn>
```

