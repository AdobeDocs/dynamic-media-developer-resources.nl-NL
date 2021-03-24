---
description: Verwijdert een eigenschapset en alle bijbehorende eigenschappen.
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---


# deletePropertySet{#deletepropertyset}

Verwijdert een eigenschapset en alle bijbehorende eigenschappen.

Syntaxis

## Toegestane gebruikerstypen {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-e5fc868f69494cf6858e03027db09101}

**Input (deletePropertySetParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | Ja | De greep naar de eigenschap die is ingesteld om te worden verwijderd. |

**Output (deletePropertySetParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-cf319fc8f86a40ab9cbd838b031973fe}

Deze codesteekproef gebruikt de greep van de reeks als gebied in `deletePropertySetParam` die naar de IPS de dienstenserver van het Web wordt verzonden om het bezitsreeks te schrappen.

**Verzoek**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**Antwoord**

Geen.
