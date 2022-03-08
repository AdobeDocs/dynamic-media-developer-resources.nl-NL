---
description: Retourneert afbeeldingsindelingen, zoals PDF, EPS, SWF en andere.
solution: Experience Manager
title: getImageFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c2fa4cdd-fb4f-4e6a-8197-8f64c986c3a0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---

# getImageFormats{#getimageformats}

Retourneert afbeeldingsindelingen, zoals PDF, EPS, SWF en andere.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-6a386ad8641b4aa1a281600fc94fd3f6}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-eefa36a70b74498f8727ef61d98cfb63}

**Input (getImageFormatsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | De handgreep naar het bedrijf met de afbeeldingsindelingen die u wilt verkrijgen. |

**Output (getImageFormatsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| imageFormatArray | `types:ImageFormatArray` | Ja | De array met afbeeldingsindelingen. |

## Voorbeelden {#section-73881e12839b4904bf3299b0920bdd0c}

Dit codevoorbeeld keert alle beeldformaten voor het gespecificeerde bedrijf terug.

**Verzoek**

```java
<ns1:getImageFormatsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getImageFormatsParam>
```

**Antwoord**

```java
<getImageFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <imageFormatArray></imageFormatArray>
</getImageFormatsReturn>
```
