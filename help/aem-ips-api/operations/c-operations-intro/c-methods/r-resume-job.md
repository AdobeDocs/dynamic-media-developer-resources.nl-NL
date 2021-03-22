---
description: Hiermee wordt een gepauzeerde taak opnieuw gestart.
seo-description: Hiermee wordt een gepauzeerde taak opnieuw gestart.
seo-title: resumeJob
solution: Experience Manager
title: resumeJob
uuid: 0ca5db75-cce0-4afc-9a58-c47c6229931e
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---


# resumeJob{#resumejob}

Hiermee wordt een gepauzeerde taak opnieuw gestart.

Syntaxis

## Toegestane gebruikerstypen {#section-eab49f4b6d1041179000326a10fee889}

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
