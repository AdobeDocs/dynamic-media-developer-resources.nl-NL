---
description: Hiermee voegt u nieuwe tagwaarden toe aan het woordenboek van een bestaand tagveld.
seo-description: Hiermee voegt u nieuwe tagwaarden toe aan het woordenboek van een bestaand tagveld.
seo-title: addTagFieldValues
solution: Experience Manager
title: addTagFieldValues
topic: Scene7 Image Production System API
uuid: 9304f02c-a1df-4477-ab33-f2491c390c92
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# addTagFieldValues{#addtagfieldvalues}

Hiermee voegt u nieuwe tagwaarden toe aan het woordenboek van een bestaand tagveld.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**Input (addTagFieldValuesParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | De greep van het bedrijf dat het tagveld bevat. |
| ` *`fieldHandle`*` | `xsd:string` | Ja | De handgreep van het tagveld dat moet worden gewijzigd. |
| ` *`valueArray`*` | `xsd:string` | Ja | Een array met tagwaarden die worden toegevoegd aan het bestaande woordenboek van het veld. |

**Output (addTagFieldValuesParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-c4049392f1c548f883b8b1f8f167bada}

**Verzoek**

```java
<addTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</addTagFieldValuesParam>
```

**Antwoord**

Geen.
