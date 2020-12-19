---
description: Hiermee verwijdert u waarden van tagvelden uit het woordenboek van een tagveld.
seo-description: Hiermee verwijdert u waarden van tagvelden uit het woordenboek van een tagveld.
seo-title: deleteTagFieldValues
solution: Experience Manager
title: deleteTagFieldValues
topic: Scene7 Image Production System API
uuid: 71cdec4e-c1d6-4518-87ed-5c47a5112b15
translation-type: tm+mt
source-git-commit: b5eaefb375fbd0d0786619fa6d84b4f6fc17a77f
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---


# deleteTagFieldValues{#deletetagfieldvalues}

Hiermee verwijdert u waarden van tagvelden uit het woordenboek van een tagveld.

## Toegestane gebruikerstypen {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-5db64a6ae238426395bc760b83587260}

**Input (deleteTagFieldValuesParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | De greep van het bedrijf dat het tagveld bevat. |
| ` *`fieldHandle`*` | `xsd:string` | Ja | De handgreep van het tagveld dat moet worden gewijzigd. |
| ` *`valueArray`*` | `types:StringArray` | Ja | Een array met tagwaarden die uit het woordenboek van het veld moet worden verwijderd. |

**Output (deleteTagFieldValuesParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-92f9e575a6da491caa09e264b4d6ee55}

**Verzoek**

```java
deleteTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</deleteTagFieldValuesParam>
```

**Antwoord**

Geen.
