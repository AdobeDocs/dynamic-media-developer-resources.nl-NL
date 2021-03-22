---
description: Hiermee wordt een actieve taak gepauzeerd.
seo-description: Hiermee wordt een actieve taak gepauzeerd.
seo-title: pauseJob
solution: Experience Manager
title: pauseJob
uuid: baad2ad6-46f5-4133-a6d9-8ffadf990a06
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---


# pauseJob{#pausejob}

Hiermee wordt een actieve taak gepauzeerd.

Syntaxis

## Toegestane gebruikerstypen {#section-f2bf306ab4574871bd21f9f7dd681033}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-7aedb924cf8b4e05a0dc927636d537a0}

**Input (pauseJobParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handgreep aan het bedrijf. |
| `*`jobHandle`*` | `xsd:string` | Ja | Handgreep aan de baan u wilt pauzeren. |

**Uitvoer (PauseJobReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-ee4914f9496f4bd88556728a48fb22c1}

In dit codevoorbeeld wordt een actieve taak gepauzeerd.

**Verzoek**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**Antwoord**

Geen.
