---
description: Hiermee verwijdert u waarden van tagvelden uit het woordenboek van een tagveld.
solution: Experience Manager
title: deleteTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2694bd6d-b1ba-4146-a155-12829d9dfa47
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---

# deleteTagFieldValues{#deletetagfieldvalues}

Hiermee verwijdert u waarden van tagvelden uit het woordenboek van een tagveld.

## Geautoriseerde gebruikerstypen {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-5db64a6ae238426395bc760b83587260}

**Input (deleteTagFieldValuesParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | De greep van het bedrijf dat het tagveld bevat. |
| fieldHandle | `xsd:string` | Ja | De handgreep van het tagveld dat moet worden gewijzigd. |
| valueArray | `types:StringArray` | Ja | Een array met tagwaarden die uit het woordenboek van het veld moet worden verwijderd. |

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
