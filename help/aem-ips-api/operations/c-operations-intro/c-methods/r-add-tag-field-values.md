---
description: Hiermee voegt u nieuwe tagwaarden toe aan het woordenboek van een bestaand tagveld.
solution: Experience Manager
title: addTagFieldValues
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---


# addTagFieldValues{#addtagfieldvalues}

Hiermee voegt u nieuwe tagwaarden toe aan het woordenboek van een bestaand tagveld.

Syntaxis

## Toegestane gebruikerstypen {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**Input (addTagFieldValuesParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De greep van het bedrijf dat het tagveld bevat. |
| `*`fieldHandle`*` | `xsd:string` | Ja | De handgreep van het tagveld dat moet worden gewijzigd. |
| `*`valueArray`*` | `xsd:string` | Ja | Een array met tagwaarden die worden toegevoegd aan het bestaande woordenboek van het veld. |

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
