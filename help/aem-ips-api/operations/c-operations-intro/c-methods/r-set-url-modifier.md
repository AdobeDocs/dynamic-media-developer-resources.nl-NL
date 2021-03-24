---
description: Stelt de opdrachten in van het protocol voor het renderen van afbeeldingen of de service voor het opgegeven element. Met deze opdrachten wijzigt u de weergave van het element zonder dat dit wordt vernietigd.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# setUrlModifier{#seturlmodifier}

Stelt de opdrachten in van het protocol voor het renderen van afbeeldingen of de service voor het opgegeven element. Met deze opdrachten wijzigt u de weergave van het element zonder dat dit wordt vernietigd.

Voor Beeldserver worden opdrachten in de parameter `urlModifier` gepubliceerd in het catalogusveld Modifier en toegepast voorafgaand aan de opdrachten die op de aanvraag-URL zijn opgegeven. Opdrachten in `urlPostApplyModifier` worden gepubliceerd naar het catalogusveld `PostModifier` en overschrijven alle opdrachten in de aanvraag-URL of in `urlModifier`. Voor Afbeelding renderen worden de opdrachten in `urlModifier` en `urlPostApplyModifier` samengevoegd en gepubliceerd naar het catalogusveld Modifier.

## Toegestane gebruikerstypen {#section-fefcd732ccf64c78956606538f96c73d}

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
| `*`companyHandle`*` | `xsd:string` | Ja | Bedrijfshandgreep. |
| `*`assetHandle`*` | `xsd:string` | Ja | Asset handle. |
| `*`urlModifier`*` | `xsd:string` | Nee | Opdrachten van het protocol voor het renderen van afbeeldingen die moeten worden toegepast vóór de aanvraag of `urlPostApplyModifier`-opdrachten. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Nee | Opdrachten van het protocol voor het renderen van afbeeldingen die moeten worden toegepast na `urlModifier` en opdrachten voor aanvragen. |

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
