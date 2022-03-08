---
description: Hiermee stelt u de afbeelding met hyperlinks in voor een element.
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---

# setImageMaps{#setimagemaps}

Hiermee stelt u de afbeelding met hyperlinks in voor een element.

U moet de afbeeldingen met hyperlinks al hebben gemaakt. Afbeeldingen met hyperlinks worden toegepast in volgorde van opvraging uit de array. Dit betekent dat de tweede afbeelding met hyperlinks het eerste bedekt, de derde de tweede, enzovoort.

## Geautoriseerde gebruikerstypen {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-2292ec1aead947ef8741dd0653a41f42}

**Input (setImageMapsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Bedrijfshandgreep. |
| assetHandle | `xsd:string` | Ja | Asset handle. |
| imageMapArray | `types:ImageMapDefinitionArray` | Ja | Array met vooraf gedefinieerde afbeeldingen met hyperlinks. |

**Output (setImageMapsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| imageMapHandleArray | `types:HandleArray` | Ja | Een array met grepen voor afbeeldingen met hyperlinks die op het element zijn toegepast. |

## Voorbeelden {#section-fe2e35662a6a4ee29cf250c9fd180371}

In dit codevoorbeeld worden twee afbeeldingen met hyperlinks ingesteld voor een afbeeldingselement. De code geeft het vormtype, het gebied en de actie op die worden uitgevoerd wanneer de afbeeldingen met hyperlinks worden aangeroepen. De reactie bevat een array met grepen naar de afbeeldingen met hyperlinks.

**Verzoek**

```java
<setImageMapsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <imageMapArray>
      <items>
         <name>ImageMap2</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>true</enabled>
      </items>
      <items>
         <name>ImageMap3</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>false</enabled>
      </items>
   </imageMapArray>
</setImageMapsParam>
```
