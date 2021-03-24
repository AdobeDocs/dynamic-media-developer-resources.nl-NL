---
description: Geeft als resultaat een array met Photoshop-padnamen voor de opgegeven afbeelding.
solution: Experience Manager
title: getPhotoshopPathNames
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---


# getPhotoshopPathNames{#getphotoshoppathnames}

Geeft als resultaat een array met Photoshop-padnamen voor de opgegeven afbeelding.

Syntaxis

## Toegestane gebruikerstypen {#section-baa0fd4b92bc4ad89809efd659b3a629}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-605a4aab23104489a21f7f7f5849801b}

**Input (getPhotoshopPathNamesParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Verwerk het bedrijf dat de afbeelding bevat waarmee u wilt werken. |
| `*`assetHandle`*` | `xsd:string` | Ja | Verwerk het afbeeldingselement. |

**Output (getPhotoshopPathNamesReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`pathNameArray`*` | `types:StringArray` | Ja | Een array met Photoshop-padnamen in een afbeelding. |

## Voorbeelden {#section-6d316f14b4184d42af4ca3f717b042dd}

**Verzoek**

```java
<getPhotoshopPathNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
</getPhotoshopPathNamesParam>
```

**Antwoord**

```java
<getPhotoshopPathNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <pathNameArray>
    <items>Background Path</items>
    <items>Face Path</items>
  </pathNameArray>
</getPhotoshopPathNamesReturn>
```

