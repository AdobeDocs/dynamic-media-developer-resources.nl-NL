---
description: Hiermee stelt u woordenboekwaarden in voor een bestaand tagveld.
seo-description: Hiermee stelt u woordenboekwaarden in voor een bestaand tagveld.
seo-title: setTagFieldValues
solution: Experience Manager
title: setTagFieldValues
topic: Scene7 Image Production System API
uuid: 56666c00-3694-4a43-a0ff-97af45c8df9f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '91'
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
| ` *`companyHandle`*` | `xsd:string` | Ja | Bedrijfshandgreep. |
| ` *`fieldHandle`*` | `xsd:string` | Ja | Handgreep van tagveld. |
| ` *`valueArray`*` | `types:StringArray` | Ja | Een array met tagwaarden die het bestaande woordenboek van het veld vervangen. Middelenkoppelingen blijven behouden wanneer een nieuwe waarde overeenkomt met een bestaande waarde. |

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
