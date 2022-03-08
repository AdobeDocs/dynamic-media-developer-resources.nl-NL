---
description: Hiermee verwijdert u een vignetpublicatie-indeling.
solution: Experience Manager
title: deleteVignetPublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a437cb47-c45c-41a0-8499-53e4c2ae3164
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# deleteVignetPublishFormat{#deletevignettepublishformat}

Hiermee verwijdert u een vignetpublicatie-indeling.

## Geautoriseerde gebruikerstypen {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-789625ba29df4b5f880914d4c64f77ce}

**Input (deleteVignetPublishFormatParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | De handgreep van het bedrijf waartoe het vignet behoort. |
| vignetteFormatHandle | `xsd:string` | Ja | De handgreep van de te verwijderen publicatie-indeling van het vignet. |

**Output (deleteVignetPublishFormatParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

In dit codevoorbeeld wordt een door de greep opgegeven vignetpublicatie-indeling verwijderd.

**Verzoek**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**Antwoord**

Geen.
