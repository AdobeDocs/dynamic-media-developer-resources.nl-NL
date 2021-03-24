---
description: Hiermee worden alle momenteel actieve taken opgehaald.
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---


# getActiveJobs{#getactivejobs}

Hiermee worden alle momenteel actieve taken opgehaald.

Syntaxis

## Toegestane gebruikerstypen {#section-125557a6ea7b4fc894d4bb468cd02118}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-29018fba6bf34c1e80dcd479dd24f3b5}

**Input (getActiveJobsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Nee | De handgreep aan het bedrijf. |
| `*`jobHandle`*` | `xsd:string` | Nee | De handgreep van de taak. |
| `*`originalName`*` | `xsd:string` | Nee | Oorspronkelijke taaknaam. |

**Output (getActiveJobsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`jobArray`*` | `xsd:string` | Ja | Array van actieve taken. |

## Voorbeelden {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

Deze codesteekproef keert alle actieve banen van een bedrijf terug dat in IPS loopt. In dit geval, is de reactie ongebruikelijk omdat IPS die coördinator plannen gehandicapt is zonder actieve banen die lopen. Onder normale omstandigheden zou de reactie een aantal actieve banen opleveren.

**Verzoek**

```java
<ns1:getActiveJobsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getActiveJobsParam>
```

**Antwoord**

```java
<getActiveJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray></jobArray>
</getActiveJobsReturn>
```

