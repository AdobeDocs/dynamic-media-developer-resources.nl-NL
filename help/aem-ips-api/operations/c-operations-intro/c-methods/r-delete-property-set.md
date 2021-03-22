---
description: Verwijdert een eigenschapset en alle bijbehorende eigenschappen.
seo-description: Verwijdert een eigenschapset en alle bijbehorende eigenschappen.
seo-title: deletePropertySet
solution: Experience Manager
title: deletePropertySet
uuid: b4fdf51f-89ec-4a69-9179-078ee8e1937f
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '99'
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
