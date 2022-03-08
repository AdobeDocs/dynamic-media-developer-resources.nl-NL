---
description: Verwijdert een type eigenschapset en de bijbehorende eigenschapset en eigenschappen.
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 97ec0f41-794f-4340-b86d-ab07a742d447
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# deletePropertySetType{#deletepropertysettype}

Verwijdert een type eigenschapset en de bijbehorende eigenschapset en eigenschappen.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-1c8973f5d35f44b4a6a483a41609e455}

**Input (deletePropertySetTypeParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| typeHandle | `xsd:string` | Ja | De greep naar het type eigenschapset dat moet worden verwijderd. |

**Output (deletePropertySetTypeParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-85faa2e3411a4e23aa6489037f7ce078}

In dit codevoorbeeld wordt de greep van het type gebruikt als een veld in het dialoogvenster `deletePropertySetTypeParam` verzonden naar de IPS de dienstenserver van het Web om het bezit te schrappen plaatste type.

**Verzoek**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**Antwoord**

Geen.
