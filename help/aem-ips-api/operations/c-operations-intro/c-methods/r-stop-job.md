---
description: Stopt een actieve taak.
solution: Experience Manager
title: stopJob
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '61'
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
