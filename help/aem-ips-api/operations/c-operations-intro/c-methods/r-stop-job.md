---
description: Stopt een actieve taak.
seo-description: Stopt een actieve taak.
seo-title: stopJob
solution: Experience Manager
title: stopJob
topic: Dynamic Media Image Production System API
uuid: 698c1652-5afa-4a2c-819a-1ba6ffc6aacf
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---


# stopJob{#stopjob}

Stopt een actieve taak.

Syntaxis

## Toegestane gebruikerstypen {#section-b222f561143747f6ad089aadc0b274d8}

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
