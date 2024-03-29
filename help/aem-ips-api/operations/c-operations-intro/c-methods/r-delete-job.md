---
description: Hiermee wordt een huidige of geplande taak verwijderd.
solution: Experience Manager
title: deleteJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d38dd1e2-668e-4956-b854-54bf466d6d45
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# deleteJob{#deletejob}

Hiermee wordt een huidige of geplande taak verwijderd.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-1b959679dc8147c291126ddf7e061742}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-000c42bc93744b1a8e777f3ec3c272b0}

**Input (deleteJobParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | De handgreep van het bedrijf waartoe de baan behoort. |
| jobHandle | `xsd:string` | Ja | De handgreep van de taak die moet worden verwijderd. |

**Uitvoer**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-732d21d4dad04337b7a5ae1a0cc00eba}

Dit codevoorbeeld schrapt een baan die loopt of gepland om in IPS in werking te stellen. Er is een taakgreep voor nodig, die u moet verkrijgen van een andere bewerking.

**Verzoek**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**Antwoord**

Geen.
