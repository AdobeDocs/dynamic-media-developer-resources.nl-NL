---
description: Hiermee voegt u nieuwe tagwaarden toe aan het woordenboek van een bestaand tagveld.
solution: Experience Manager
title: addTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 099263e4-8214-46eb-898e-7a28c4f25598
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

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
| companyHandle | `xsd:string` | Ja | De greep van het bedrijf dat het tagveld bevat. |
| fieldHandle | `xsd:string` | Ja | De handgreep van het tagveld dat moet worden gewijzigd. |
| valueArray | `xsd:string` | Ja | Een array met tagwaarden die worden toegevoegd aan het bestaande woordenboek van het veld. |

**Output (addTagFieldValuesParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-c4049392f1c548f883b8b1f8f167bada}

**Verzoek**

```java {.line-numbers}
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
