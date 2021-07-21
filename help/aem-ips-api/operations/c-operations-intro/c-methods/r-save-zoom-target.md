---
description: Maak of bewerk een zoomdoel.
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 595fd5c8-4e98-4c1a-b396-c8e170aaf454
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 1%

---

# saveZoomTarget{#savezoomtarget}

Maak of bewerk een zoomdoel.

Syntaxis

## Type geautoriseerde gebruiker {#section-823cd9f0557045bca51da66768b5ba74}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-4a23983cae4e49a098e9bbe736933996}

**Input (saveZoomTargetParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep naar het bedrijf met het zoomdoel dat u wilt opslaan. |
| `*`assetHandle`*` | `xsd:string` | Ja | De handgreep van het zoomdoel. |
| `*`zoomTargetHandle`*` | `xsd:string` | Nee | Hiermee bewerkt of maakt u een zoomdoel. |
| `*`name`*` | `xsd:string` | Ja | Naam van zoomdoel. |
| `*`xPosition`*` | `xsd:int` | Ja | Locatie van linkerpixel. |
| `*`yPosition`*` | `xsd:int` | Ja | Bovenste pixellocatie. |
| `*`width`*` | `xsd:int` | Ja | Breedte van zoomdoel. |
| `*`height`*` | `xsd:int` | Ja | Hoogte doel zoomen. |
| `*`userData`*` | `xsd:string` | Ja | Voor klantspecifieke informatie. Kan elk type gegevens bevatten. |

**Output (saveZoomTargetReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`zoomTargetHandle`*` | `xsd:string` | Ja | Verwerk het nieuwe zoomdoel. |

## Voorbeelden {#section-509c472c316549cdb228d7e1cfa8400a}

In dit codevoorbeeld wordt een zoomdoel opgeslagen. De reactie retourneert de zoomdoelgreep.

**Verzoek**

```java
<saveZoomTargetParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>24267|1|17063</assetHandle>
   <name>My Zoom Target</name>
   <xPosition>2</xPosition>
   <yPosition>2</yPosition>
   <width>10</width>
   <height>10</height>
   <userData>My User Data</userData>
</saveZoomTargetParam>
```

**Antwoord**

```java
<saveZoomTargetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <zoomTargetHandle>34194|9|301</zoomTargetHandle>
</saveZoomTargetReturn>
```
