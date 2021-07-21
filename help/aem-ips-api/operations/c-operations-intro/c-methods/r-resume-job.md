---
description: Hiermee wordt een gepauzeerde taak opnieuw gestart.
solution: Experience Manager
title: resumeJob
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: ba8818ff-3040-463c-80d3-b7cfd1e01f77
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---

# resumeJob{#resumejob}

Hiermee wordt een gepauzeerde taak opnieuw gestart.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-eab49f4b6d1041179000326a10fee889}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-6b2f8aa65d4d4ae1af0c9cee468b0a51}

**Input (resumeJobParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep van het bedrijf met de baan u wilt opnieuw beginnen. |
| `*`jobHandle`*` | `xsd:string` | Ja | De greep naar de gepauzeerde taak. |

**Output (resumeJobReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-d0524e031f1f43d89430eade19526162}

In dit codevoorbeeld wordt een gepauzeerde taak opnieuw gestart.

**Verzoek**

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**Antwoord**

Geen.
