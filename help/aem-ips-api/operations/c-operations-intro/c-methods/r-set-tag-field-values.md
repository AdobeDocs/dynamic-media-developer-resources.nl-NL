---
description: Hiermee stelt u woordenboekwaarden in voor een bestaand tagveld.
solution: Experience Manager
title: setTagFieldValues
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# setTagFieldValues{#settagfieldvalues}

Hiermee stelt u woordenboekwaarden in voor een bestaand tagveld.

Syntaxis

## Toegestane gebruikerstypen {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-a05cbee4cb4f44198c414a6b14e69156}

**Invoer**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Bedrijfshandgreep. |
| `*`fieldHandle`*` | `xsd:string` | Ja | Handgreep van tagveld. |
| `*`valueArray`*` | `types:StringArray` | Ja | Een array met tagwaarden die het bestaande woordenboek van het veld vervangen. Middelenkoppelingen blijven behouden wanneer een nieuwe waarde overeenkomt met een bestaande waarde. |

**Output (setTagFieldValuesReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-b11cafd9bed54ab5836c737cc075c918}

**Verzoek**

```java
<setTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Nurth</items>
      <items>Suth</items>
      <items>East</items>
      <items>West</items>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</setTagFieldValuesParam>
```

**Antwoord**

Geen.
