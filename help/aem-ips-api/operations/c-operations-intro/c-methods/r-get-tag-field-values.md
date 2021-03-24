---
description: Hiermee worden alle gedefinieerde tagwoordenboekwaarden opgehaald voor een of meer tagvelden.
solution: Experience Manager
title: getTagFieldValues
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---


# getTagFieldValues{#gettagfieldvalues}

Hiermee worden alle gedefinieerde tagwoordenboekwaarden opgehaald voor een of meer tagvelden.

Syntaxis

## Toegestane gebruikerstypen {#section-cc36a437394c491594e704a08a161c87}

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

