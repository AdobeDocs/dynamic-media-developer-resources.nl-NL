---
description: Haalt de zoekreeksen, trefwoorden en andere informatie over een element op. De reactie bevat aanvullende informatie over het element.
seo-description: Haalt de zoekreeksen, trefwoorden en andere informatie over een element op. De reactie bevat aanvullende informatie over het element.
seo-title: getSearchStrings
solution: Experience Manager
title: getSearchStrings
topic: Dynamic Media Image Production System API
uuid: 9d588d6b-c79c-4531-a2e8-8467254a7985
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---


# getSearchStrings{#getsearchstrings}

Haalt de zoekreeksen, trefwoorden en andere informatie over een element op. De reactie bevat aanvullende informatie over het element.

Syntaxis

## Toegestane gebruikerstypen {#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-c1efda4bb15349a68b276bafee8c18fd}

**Input (getSearchStringsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handgreep aan het bedrijf. |
| `*`assetHandle`*` | `xsd:string` | Ja | Verwerk het element. |

**Output (getSearchStringsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`searchStringArray`*` | `types:SearchStrings` | Ja | Een array met zoektekenreeksen voor elementen. |

## Voorbeelden {#section-e1f73bff6e4440c489d59cb9aa5384d8}

Dit codevoorbeeld retourneert asset-specifieke zoekreeksen. De reactie retourneert een lege array.

**Verzoek**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**Antwoord**

Geen.
