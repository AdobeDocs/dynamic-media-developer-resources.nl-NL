---
description: Hiermee stelt u het zoomdoel in dat aan een elementafbeelding is gekoppeld. De bestaande zoomdoelen worden overschreven.
solution: Experience Manager
title: setZoomTargets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1b4ac729-00cf-4ea2-9098-60b4af3c7e6d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# setZoomTargets{#setzoomtargets}

Hiermee stelt u het zoomdoel in dat aan een elementafbeelding is gekoppeld. De bestaande zoomdoelen worden overschreven.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-c5e1863e9cb1426591bfea513620b6ab}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-161f8c733cc4439f94a06e12119d4226}

**Input (setZoomTargetsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Bedrijfshandgreep. |
| assetHandle | `xsd:string` | Ja | Element met het zoomdoel dat u wilt instellen. |
| zoomTargetArray | `types:ZoomTargetDefinitionArray` | Ja | Array met zoomdoeldefinities. |

**Output (setZoomTargetsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| zoomTargetHandleArray | `types:HandleArray` | Ja | De set handgrepen voor de zoomdoelen die door deze bewerking worden gemaakt. |

## Voorbeelden {#section-a2f14c7a1499443e96d099ea8a76c182}

In dit codevoorbeeld wordt een array met zoomdoelen op naam, positie (x- en y-as), breedte en hoogte gedefinieerd en wordt de array aan een element toegewezen. De reactie bevat handgrepen voor de nieuwe zoomdoelen.

**Verzoek**

```java
<setZoomTargetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <zoomTargetArray>
      <items>
         <name>zoomTarget2</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
      <items>
         <name>zoomTarget3</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
   </zoomTargetArray>
</setZoomTargetsParam>
```

**Antwoord**

```java
<setZoomTargetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zoomTargetHandleArray>
      <items>a|947|9|41</items>
      <items>a|948|9|42</items>
   </zoomTargetHandleArray>
</setZoomTargetsReturn>
```
