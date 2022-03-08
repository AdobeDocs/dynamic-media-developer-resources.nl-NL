---
description: Hiermee stelt u woordenboekwaarden in voor een bestaand tagveld.
solution: Experience Manager
title: setTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 50f437d6-fec5-4961-884e-fdb75d201ab7
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# setTagFieldValues{#settagfieldvalues}

Hiermee stelt u woordenboekwaarden in voor een bestaand tagveld.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-a05cbee4cb4f44198c414a6b14e69156}

**Invoer**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Bedrijfshandgreep. |
| fieldHandle | `xsd:string` | Ja | Handgreep van tagveld. |
| valueArray | `types:StringArray` | Ja | Een array met tagwaarden die het bestaande woordenboek van het veld vervangen. Middelenkoppelingen blijven behouden wanneer een nieuwe waarde overeenkomt met een bestaande waarde. |

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
