---
description: Hiermee vervangt u afbeeldingsgegevens voor een afbeeldingselement.
seo-description: Hiermee vervangt u afbeeldingsgegevens voor een afbeeldingselement.
seo-title: replaceImage
solution: Experience Manager
title: replaceImage
topic: Scene7 Image Production System API
uuid: 46824e33-265c-4425-9ab1-8ad6b7ac154d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---


# replaceImage{#replaceimage}

Hiermee vervangt u afbeeldingsgegevens voor een afbeeldingselement.

Syntaxis

## Toegestane gebruikerstypen {#section-e2aad71fb2a54612badc7b16f82ed544}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-0d0ab668fa6d4310a93fb7ef8d8dd1e0}

**Input (replaceImageParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyName`*` | `xsd:string` | Ja | De handgreep van het bedrijf met de afbeelding die u wilt vervangen. |
| ` *`assetHandle`*` | `xsd:string` | Ja | De handgreep van het element dat u wilt vervangen. |
| ` *`urlModifier`*` | `xsd:string` | Ja | De bevelen van de Server van het beeld die nieuwe beeldgegevens produceren. |

**Uitvoer (replaceImageReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Ja | Verwerk het nieuwe element. |

## Voorbeelden {#section-cebb93576bde4cb98cb27356ca66783b}

Dit codevoorbeeld vervangt een beeld en past `urlModifier` met een bevel toe dat specificeert dat de Server van het Beeld geen actie op vervanging zal nemen.

**Verzoek**

```java
<replaceImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|140626|1|102524</assetHandle>
   <urlModifier>action=none</urlModifier>
</replaceImageParam>
```

**Antwoord**

```java
<replaceImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|140626|1|102524</assetHandle>
</replaceImageReturn>
```

