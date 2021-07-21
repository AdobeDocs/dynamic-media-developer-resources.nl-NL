---
description: Haalt tekenreekswaarden op van systeemeigenschappen die gerelateerd zijn aan Image Portal.
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 2297b785-28c7-49c6-8891-00986f35ea88
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# getProperty{#getproperty}

Haalt tekenreekswaarden op van systeemeigenschappen die gerelateerd zijn aan Image Portal.

Tot de ondersteunde systeemeigenschappen behoren:

* `IpsVersion`: IPS versienummer.
* `IpsImageServerUrl`: Volledig, extern voorvoegsel URL voor de IPS Server van het Beeld.
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`: URL-voorvoegsel voor het renderen van SVG-elementen.
* `SvgRenderEnabled`: True if SVG assets can be rendered by  `SvgRenderRootUrl`.

* `UploadPostMaxFileSize`: Maximale grootte (in bytes) van bestandsgegevens die is toegestaan tijdens het uploaden  [!DNL POST]. Het systeem wijst bestanden af die groter zijn dan de maximale limiet.

## Geautoriseerde gebruikerstypen {#section-2cd36bbd46ed414b8753569d5895530e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-e3d389d183b244c2a5ef39c0ec331b5e}

**Input (getPropertyParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`name`*` | `xsd:string` | Ja | The name of the property to get. |

**Output (getPropertyReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`value`*` | `xsd:string` | Ja | De eigenschapswaarde. |

## Voorbeelden {#section-3f80a78dd60c404181b34d3a912d7a36}

Deze codesteekproef gebruikt een IPS het koordconstante van Eigenschappen om een specifieke waarde terug te keren. In dit voorbeeld, is het IPS bezit de versie van de IPS server.

**Verzoek**

```java
<ns1:getPropertyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:name>IpsVersion</ns1:name>
</ns1:getPropertyParam>
```

**Antwoord**

```java
<getPropertyReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <value>3.8.0</value>
</getPropertyReturn>
```
