---
description: Hiermee worden alle gedefinieerde tagwoordenboekwaarden opgehaald voor een of meer tagvelden.
solution: Experience Manager
title: getTagFieldValues
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 12836783-4f9d-41d3-9b42-6e25238d7ed5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# getTagFieldValues{#gettagfieldvalues}

Hiermee worden alle gedefinieerde tagwoordenboekwaarden opgehaald voor een of meer tagvelden.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-cc36a437394c491594e704a08a161c87}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-9ad806e7736e4d51ae42cad185050cf9}

**Input (getTagFieldValuesReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De greep van het bedrijf dat het tagveld bevat. |
| `*`fieldHandleArray`*` | `types:HandleArray` | Ja | Een array met veldgrepen om de waarden van tags die u wilt retourneren, te labelen. |

**Output (getTagFieldValuesReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`fieldArray`*` | `types:TagFieldValuesArray` | Ja | Een array van de tagwaarden in het woordenboek voor elk aangevraagd veld. |

## Voorbeelden {#section-4492742614e44bb191a7d397dc1a1407}

**Verzoek**

```java
<getTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandleArray>
      <items>m|3|ASSET|SingleOpenTag</items>
      <items>m|3|ASSET|SingleFixedTag</items>
   </fieldHandleArray>
</getTagFieldValuesParam>
```

**Antwoord**

```java
<getTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <fieldArray>
      <items>
         <fieldHandle>m|3|ASSET|SingleOpenTag</fieldHandle>
         <valueArray>
            <items>GroupB</items>
            <items>GroupA</items>
         </valueArray>
      </items>
      <items>
         <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
         <valueArray>
            <items>North</items>
            <items>South</items>
            <items>East</items><items>West</items>
         </valueArray>
      </items>
   </fieldArray>
</getTagFieldValuesReturn>
```
