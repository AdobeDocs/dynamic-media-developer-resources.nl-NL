---
description: Hiermee verwijdert u een vignetpublicatie-indeling.
solution: Experience Manager
title: deleteVignetPublishFormat
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---


# deleteVignetPublishFormat{#deletevignettepublishformat}

Hiermee verwijdert u een vignetpublicatie-indeling.

## Toegestane gebruikerstypen {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-789625ba29df4b5f880914d4c64f77ce}

**Input (deleteVignetPublishFormatParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep van het bedrijf waartoe het vignet behoort. |
| `*`vignetteFormatHandle`*` | `xsd:string` | Ja | De handgreep van de te verwijderen publicatie-indeling van het vignet. |

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
