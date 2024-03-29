---
description: Stelt de opdrachten in van het protocol voor het renderen van afbeeldingen of de service voor het opgegeven element. Met deze opdrachten wijzigt u de weergave van het element zonder dat dit wordt vernietigd.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---

# setUrlModifier{#seturlmodifier}

Stelt de opdrachten in van het protocol voor het renderen van afbeeldingen of de service voor het opgegeven element. Met deze opdrachten wijzigt u de weergave van het element zonder dat dit wordt vernietigd.

Voor Beeldverwerking, opdrachten in het dialoogvenster `urlModifier` worden gepubliceerd in het veld Modifier-catalogus en toegepast vóór de opdrachten die op de aanvraag-URL zijn opgegeven. Opdrachten in `urlPostApplyModifier` worden gepubliceerd `PostModifier` catalogusveld en overschrijf alle opdrachten in de aanvraag-URL of in `urlModifier`. Voor het renderen van afbeeldingen worden de opdrachten in `urlModifier` en `urlPostApplyModifier` worden samengevoegd en gepubliceerd in het veld Modifier-catalogus.

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
| companyHandle | `xsd:string` | Ja | Bedrijfshandgreep. |
| assetHandle | `xsd:string` | Ja | Asset handle. |
| urlModifier | `xsd:string` | Nee | Opdrachten in het protocol voor het renderen van afbeeldingen die moeten worden toegepast voordat een aanvraag wordt ingediend of `urlPostApplyModifier` opdrachten. |
| urlPostApplyModifier | `xsd:string` | Nee | Opdrachten in het protocol voor het renderen van afbeeldingen die na `urlModifier` en verzoek opdrachten. |

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
