---
description: Verwijdert een eigenschapset en alle bijbehorende eigenschappen.
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72429030-200d-4e13-a537-10a728998a26
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# deletePropertySet{#deletepropertyset}

Verwijdert een eigenschapset en alle bijbehorende eigenschappen.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-e5fc868f69494cf6858e03027db09101}

**Input (deletePropertySetParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| setHandle | `xsd:string` | Ja | De greep naar de eigenschap die is ingesteld om te worden verwijderd. |

**Output (deletePropertySetParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-cf319fc8f86a40ab9cbd838b031973fe}

In dit codevoorbeeld wordt de greep van de set gebruikt als een veld in het dialoogvenster `deletePropertySetParam` verzonden naar de IPS de dienstenserver van het Web om het bezit te schrappen plaatste.

**Verzoek**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**Antwoord**

Geen.
