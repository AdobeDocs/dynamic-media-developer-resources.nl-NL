---
description: Retourneert twee verschillende typen informatie op basis van de doorgegeven parameters. originatorHandle retourneert informatie over elementen die zijn gegenereerd op basis van het opgegeven element. generateHandle geeft informatie over stappen die worden gebruikt om het opgegeven element of bestand te genereren.
seo-description: Retourneert twee verschillende typen informatie op basis van de doorgegeven parameters. originatorHandle retourneert informatie over elementen die zijn gegenereerd op basis van het opgegeven element. generateHandle geeft informatie over stappen die worden gebruikt om het opgegeven element of bestand te genereren.
seo-title: getGenerationInfo
solution: Experience Manager
title: getGenerationInfo
topic: Dynamic Media Image Production System API
uuid: 4310a702-c08b-4479-9f57-9f2bc1d6b032
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# getGenerationInfo{#getgenerationinfo}

Retourneert twee verschillende typen informatie op basis van de doorgegeven parameters. originatorHandle retourneert informatie over elementen die zijn gegenereerd op basis van het opgegeven element. generateHandle geeft informatie over stappen die worden gebruikt om het opgegeven element of bestand te genereren.

Syntaxis

## Toegestane gebruikerstypen {#section-9cc2216b32c74107be07aeacecc11401}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-b7fa94c82147455888e8469fa5f6922b}

**Input (getGenerationInfoParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`Codewoordgroep`*` | `xsd:string` | Ja | De handgreep aan het bedrijf. |
| `*`Codewoordgroep`*` | `xsd:string` | Nee | De motor die in de productie werd gebruikt. Zie Lettertypestijlen. |
| `*`Codewoordgroep`*` | `xsd:string` | Nee | De greep van het element waarnaar moet worden gezocht voor gegenereerde elementen. |
| `*`Codewoordgroep`*` | `xsd:string` | Nee | De greep van het element die moet worden gezocht naar elementen en engines die worden gebruikt bij het genereren van het element. |
| `*`Codewoordgroep`*` | `xsd:StringArray` | Nee | Eigenschappen die in de bewerking zijn opgenomen. |
| `*`Codewoordgroep`*` | `xsd:StringArray` | Nee | Eigenschappen die van de bewerking zijn uitgesloten. |

**Output (getGenerationInfoReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`generationArray`*` | `types:GenerationInfoArray` | Ja | Array met generatiegegevens. |

## Voorbeelden {#section-fdffe6ed82d94c7aa90e47f7ce889403}

Deze codesteekproef keert informatie over activa terug die van een specifiek element worden geproduceerd. Er wordt geen informatie opgehaald over de stappen die zijn gebruikt om het opgegeven element te genereren. De reactie is afgebroken voor de beknoptheid.

**Verzoek**

```java
<getGenerationInfoParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <originatorHandle>a|716|25|160</originatorHandle>
</getGenerationInfoParam>
```

**Antwoord**

```java
<getGenerationInfoReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <generationArray>
      <items>
         <engine>PostScriptRip</engine>
         <originator>
         ...
         </generated>
         <attributeArray/>
      </items>
   </generationArray>
</getGenerationInfoReturn>
```

