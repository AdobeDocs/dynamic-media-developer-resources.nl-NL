---
description: Hiermee stelt u de afbeelding met hyperlinks in voor een element.
seo-description: Hiermee stelt u de afbeelding met hyperlinks in voor een element.
seo-title: setImageMaps
solution: Experience Manager
title: setImageMaps
topic: Dynamic Media Image Production System API
uuid: 1dd7e032-34b4-464d-8ec6-7ad282d12891
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---


# setImageMaps{#setimagemaps}

Hiermee stelt u de afbeelding met hyperlinks in voor een element.

U moet de afbeeldingen met hyperlinks al hebben gemaakt. Afbeeldingen met hyperlinks worden toegepast in volgorde van opvraging uit de array. Dit betekent dat de tweede afbeelding met hyperlinks het eerste bedekt, de derde de tweede, enzovoort.

## Toegestane gebruikerstypen {#section-adb21c5b679249939dd83816e4a0ee97}

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
| `*`companyHandle`*` | `xsd:string` | Ja | Bedrijfshandgreep. |
| `*`assetHandle`*` | `xsd:string` | Ja | Asset handle. |
| `*`imageMapArray`*` | `types:ImageMapDefinitionArray` | Ja | Array met vooraf gedefinieerde afbeeldingen met hyperlinks. |

**Output (setImageMapsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`imageMapHandleArray`*` | `types:HandleArray` | Ja | Een array met grepen voor afbeeldingen met hyperlinks die op het element zijn toegepast. |

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

