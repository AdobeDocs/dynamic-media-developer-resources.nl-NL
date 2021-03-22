---
description: Retourneert afbeeldingsindelingen, zoals PDF, EPS, SWF en andere.
seo-description: Retourneert afbeeldingsindelingen, zoals PDF, EPS, SWF en andere.
seo-title: getImageFormats
solution: Experience Manager
title: getImageFormats
uuid: 0adf989d-9c72-4337-99c0-de6931943e78
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---


# getImageFormats{#getimageformats}

Retourneert afbeeldingsindelingen, zoals PDF, EPS, SWF en andere.

Syntaxis

## Toegestane gebruikerstypen {#section-6a386ad8641b4aa1a281600fc94fd3f6}

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
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep naar het bedrijf met de afbeeldingsindelingen die u wilt verkrijgen. |

**Output (getImageFormatsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`imageFormatArray`*` | `types:ImageFormatArray` | Ja | De array met afbeeldingsindelingen. |

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

