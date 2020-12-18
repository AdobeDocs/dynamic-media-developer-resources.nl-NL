---
description: Controleert op IPS ID-conflicten door elementnamen te vergelijken met alle namen van de naamruimte van de catalogus Afbeelding weergeven/Afbeelding renderen van een bedrijf.
seo-description: Controleert op IPS ID-conflicten door elementnamen te vergelijken met alle namen van de naamruimte van de catalogus Afbeelding weergeven/Afbeelding renderen van een bedrijf.
seo-title: checkAssetNames
solution: Experience Manager
title: checkAssetNames
topic: Scene7 Image Production System API
uuid: 91d073a8-7648-429b-aa5c-c7d595550299
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# checkAssetNames{#checkassetnames}

Controleert op IPS ID-conflicten door elementnamen te vergelijken met alle namen van de naamruimte van de catalogus Afbeelding weergeven/Afbeelding renderen van een bedrijf.

Syntaxis

## Toegestane gebruikerstypen {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## Parameters {#section-9c75b00f2072453abea0bdefc6ad7c99}

**Input (checkAssetNamesParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Nee | De handgreep aan het bedrijf dat de gebruiker bevat. |
| ` *`assetNamesArray`*` | `types:StringArray` | Ja | Een array met namen van elementen die moeten worden gecontroleerd. |

**Uitvoer (checkAssetNamesReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`inUseNameArray`*` | `types:StringArray` | Ja | Een array met namen van elementen in gebruik. |

## Voorbeelden {#section-bc5d120d74614a63a425ca3acc337219}

In deze voorbeeldcode worden de namen van elementen opgevraagd die voor een opgegeven bedrijf worden gebruikt. De reactie retourneert een array met namen van elementen die in gebruik zijn.

**Verzoek**

```java
<checkAssetNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <companyHandle>c|1</companyHandle>
   <assetNameArray>
      <items>ABC123</items>
      <items>DEF456</items>
   </assetNameArray>
</checkAssetNamesParam>
```

**Antwoord**

```java
<checkAssetNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <inUseNameArray>
      <items>DEF456</items>
   </inUseNameArray>
</checkAssetNamesReturn>
```

