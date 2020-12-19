---
description: Hiermee verwijdert u een vignetpublicatie-indeling.
seo-description: Hiermee verwijdert u een vignetpublicatie-indeling.
seo-title: deleteVignetPublishFormat
solution: Experience Manager
title: deleteVignetPublishFormat
topic: Scene7 Image Production System API
uuid: 3c8148d5-dec6-4ffa-8ab8-2cd70811ada6
translation-type: tm+mt
source-git-commit: d3766bba78cd1051538ff6a94f61ba61e989f1a5
workflow-type: tm+mt
source-wordcount: '81'
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
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep van het bedrijf waartoe het vignet behoort. |
| ` *`vignetteFormatHandle`*` | `xsd:string` | Ja | De handgreep van de te verwijderen publicatie-indeling van het vignet. |

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
