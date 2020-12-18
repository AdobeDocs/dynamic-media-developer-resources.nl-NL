---
description: Hiermee stelt u het zoomdoel in dat aan een elementafbeelding is gekoppeld. De bestaande zoomdoelen worden overschreven.
seo-description: Hiermee stelt u het zoomdoel in dat aan een elementafbeelding is gekoppeld. De bestaande zoomdoelen worden overschreven.
seo-title: setZoomTargets
solution: Experience Manager
title: setZoomTargets
topic: Scene7 Image Production System API
uuid: 5d0aecec-ebd8-4c69-9514-c29fae347ee6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# setZoomTargets{#setzoomtargets}

Hiermee stelt u het zoomdoel in dat aan een elementafbeelding is gekoppeld. De bestaande zoomdoelen worden overschreven.

Syntaxis

## Toegestane gebruikerstypen {#section-c5e1863e9cb1426591bfea513620b6ab}

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
| ` *`companyHandle`*` | `xsd:string` | Ja | Bedrijfshandgreep. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Element met het zoomdoel dat u wilt instellen. |
| ` *`zoomTargetArray`*` | `types:ZoomTargetDefinitionArray` | Ja | Array met zoomdoeldefinities. |

**Output (setZoomTargetsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`zoomTargetHandleArray`*` | `types:HandleArray` | Ja | De set handgrepen voor de zoomdoelen die door deze bewerking worden gemaakt. |

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

