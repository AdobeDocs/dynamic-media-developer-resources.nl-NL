---
description: Haalt de zoekreeksen, trefwoorden en andere informatie over een element op. De reactie bevat aanvullende informatie over het element.
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e94215b8-1121-4be6-a8a9-e9444c57495d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---

# getSearchStrings{#getsearchstrings}

Haalt de zoekreeksen, trefwoorden en andere informatie over een element op. De reactie bevat aanvullende informatie over het element.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-c1efda4bb15349a68b276bafee8c18fd}

**Input (getSearchStringsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handgreep aan het bedrijf. |
| assetHandle | `xsd:string` | Ja | Verwerk het element. |

**Output (getSearchStringsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| searchStringArray | `types:SearchStrings` | Ja | Een array met zoektekenreeksen voor elementen. |

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
