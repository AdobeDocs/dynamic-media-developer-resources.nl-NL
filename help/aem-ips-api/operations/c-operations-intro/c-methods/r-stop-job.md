---
description: Stopt een actieve taak.
solution: Experience Manager
title: stopJob
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 90e61cf1-11f1-4504-8007-126ba4fe436a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 0%

---

# stopJob{#stopjob}

Stopt een actieve taak.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-b222f561143747f6ad089aadc0b274d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-2b64f074e37c4c38849994f3bc65342a}

**Input (stopJobParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Bedrijfshandgreep. |
| `*`jobHandle`*` | `xsd:string` | Ja | Handgreep aan de baan u wilt ophouden. |

**Output (stopJobReturn0**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-f7e07fa09ae24dc89685533f20ab3b81}

**Verzoek**

```java
<stopJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</stopJobParam>
```

**Antwoord**

Geen.
