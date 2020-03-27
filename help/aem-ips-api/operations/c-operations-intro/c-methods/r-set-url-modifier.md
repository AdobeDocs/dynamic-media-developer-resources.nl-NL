---
description: Stelt de opdrachten in van het protocol voor het renderen van afbeeldingen of de service voor het opgegeven element. Met deze opdrachten wijzigt u de weergave van het element zonder dat dit wordt vernietigd.
seo-description: Stelt de opdrachten in van het protocol voor het renderen van afbeeldingen of de service voor het opgegeven element. Met deze opdrachten wijzigt u de weergave van het element zonder dat dit wordt vernietigd.
seo-title: setUrlModifier
solution: Experience Manager
title: setUrlModifier
topic: Scene7 Image Production System API
uuid: ec423e57-338b-4a32-be5a-a73fa96712ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setUrlModifier{#seturlmodifier}

Stelt de opdrachten in van het protocol voor het renderen van afbeeldingen of de service voor het opgegeven element. Met deze opdrachten wijzigt u de weergave van het element zonder dat dit wordt vernietigd.

Voor Beeldserver worden de opdrachten in de `urlModifier` parameter gepubliceerd in het catalogusveld Modifier en toegepast voorafgaand aan de opdrachten die op de aanvraag-URL zijn opgegeven. Opdrachten in `urlPostApplyModifier` worden gepubliceerd naar het `PostModifier` catalogusveld en overschrijven alle opdrachten in de aanvraag-URL of in `urlModifier`. Bij Afbeelding renderen worden de opdrachten in `urlModifier` en `urlPostApplyModifier` samengevoegd en gepubliceerd naar het catalogusveld Modifier.

## Geautoriseerde gebruikerstypen {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**Input (setUrlModifierParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Bedrijfshandgreep. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Asset handle. |
| ` *`urlModifier`*` | `xsd:string` | Nee | Opdrachten van het protocol voor het renderen van afbeeldingen of het renderen van afbeeldingen die moeten worden toegepast voorafgaand aan een aanvraag of `urlPostApplyModifier` opdracht. |
| ` *`urlPostApplyModifier`*` | `xsd:string` | Nee | Opdrachten in het protocol voor het renderen van afbeeldingen die moeten worden toegepast na opdrachten `urlModifier` en aanvragen. |

**Output (setUrlModifierReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-801d4b9b986443f59a5783a3d6bf44aa}

**Verzoek**

```java
<setUrlModifierParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|942|1|579</assetHandle>
   <urlModifier>modify=that</urlModifier>
   <urlPostApplyModifier>action=awesomeToo</urlPostApplyModifier>
</setUrlModifierParam>
```

**Antwoord**

Geen.
