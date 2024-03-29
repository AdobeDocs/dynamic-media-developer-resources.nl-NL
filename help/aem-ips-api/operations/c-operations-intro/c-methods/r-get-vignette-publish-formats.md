---
description: getVignetPublishFormats
solution: Experience Manager
title: getVignetPublishFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6e56d68e-b5cf-4044-9c58-f8221fa4490f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 0%

---

# getVignetPublishFormats{#getvignettepublishformats}

Syntaxis

## Geautoriseerde gebruikerstypen {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**Input (getVignetPublishFormatsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | De handgreep aan het bedrijf. |

**Output (getVignetPublishFormatsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| vignetteFormatArray | `types:VignettePublishFormatArray` | Ja | Array met publicatie-indelingen voor vignet. |

## Voorbeelden {#section-2cc32b27cc6243b7b3e273cc05996226}

Deze codesteekproef keert twee vignet terug publiceert formaten verbonden aan een specifiek bedrijf. Informatie wordt geretourneerd in een array die wordt afgekapt voor bondigheid.

**Verzoek**

```java
<getVignettePublishFormatsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
</getVignettePublishFormatsParam>
```

**Antwoord**

```java
<getVignettePublishFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatArray>
      <items>
         <companyHandle>c|21</companyHandle>
         <vignetteFormatHandle>v|21|281</vignetteFormatHandle>
         <name>APIcreateVignettePublishFormat</name>
         ...
      </items>
   </vignetteFormatArray>
</getVignettePublishFormatsReturn>
```
