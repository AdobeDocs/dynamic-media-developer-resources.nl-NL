---
description: Verwijdert een type eigenschapset en de bijbehorende eigenschapset en eigenschappen.
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---


# deletePropertySetType{#deletepropertysettype}

Verwijdert een type eigenschapset en de bijbehorende eigenschapset en eigenschappen.

Syntaxis

## Toegestane gebruikerstypen {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-1c8973f5d35f44b4a6a483a41609e455}

**Input (deletePropertySetTypeParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | Ja | De greep naar het type eigenschapset dat moet worden verwijderd. |

**Output (deletePropertySetTypeParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-85faa2e3411a4e23aa6489037f7ce078}

Deze codesteekproef gebruikt het handvat van het type als gebied in `deletePropertySetTypeParam` die naar de IPS de dienstenserver van het Web wordt verzonden om het type van bezitsreeks te schrappen.

**Verzoek**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**Antwoord**

Geen.
