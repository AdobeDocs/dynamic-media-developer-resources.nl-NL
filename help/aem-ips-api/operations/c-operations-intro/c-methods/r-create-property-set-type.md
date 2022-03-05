---
description: Een type eigenschapset geeft verschillende instellingen op die worden gebruikt voor het beheren van eigenschapssets.
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# createPropertySetType{#createpropertysettype}

Een type eigenschapset geeft verschillende instellingen op die worden gebruikt voor het beheren van eigenschapssets.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-43dece72eb9f44df80f4a119dd2c008b}

**Input (createPropertySetTypeParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Nee | De handgreep naar het bedrijf dat eigenaar is van het type eigenschapsset. Indien `companyHandle` wordt niet overgegaan en de bezoeker is `IpsAdmin`, wordt een algemeen type eigenschapset gemaakt. |
| `*`name`*` | `xsd:string` | Ja | De naam van het type eigenschapset. |
| `*`propertyType`*` | `xsd:string` | Ja | Keuze van type eigenschapset. |
| `*`allowMultiple`*` | `xsd:boolean` | Ja | Hiermee wordt bepaald of uw programma meerdere eigenschapssets kan hebben. |

**Output (createPropertySetTypeReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | Ja | Een greep naar de tekst. |

## Voorbeelden {#section-13396c9639a6475190e622eae3cdb534}

In dit codevoorbeeld wordt een eigenschapset gemaakt met een naam en type die door de `PropertySet Types` constante. De handgreep naar het bedrijf dat eigenaar is van het type eigenschapsset. Als companyHandle niet wordt overgegaan en de bezoeker een IpsAdmin is, wordt een globaal bezitsplaatstype gecreeerd.

**Verzoek**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10803</typeHandle>
</createPropertySetTypeReturn>
```

**Antwoord**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</createPropertySetTypeReturn>
```
