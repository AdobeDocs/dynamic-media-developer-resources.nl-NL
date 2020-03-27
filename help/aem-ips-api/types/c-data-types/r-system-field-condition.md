---
description: Een zoekvoorwaarde voor het systeemveld voor de bewerking searchAssets.
seo-description: Een zoekvoorwaarde voor het systeemveld voor de bewerking searchAssets.
seo-title: SystemFieldCondition
solution: Experience Manager
title: SystemFieldCondition
topic: Scene7 Image Production System API
uuid: 811095df-732d-48a3-a6ff-55d6dc602b54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SystemFieldCondition{#systemfieldcondition}

Een zoekvoorwaarde voor het systeemveld voor de bewerking searchAssets.

Voor unary vergelijkt, ga precies één waarde ( `boolVal`, `longVal`, `doubleVal`, of `dateVal`) door afhankelijk van het type van systeemgebied. Geef voor zoekbereiken `min<Type>` en `max<Type>` parameters door en geef een `op` waarde van `Between` of `NotBetween`door.

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| ` *`field`*` | `xsd:string` | Keuze van velden voor het zoeken naar middelen. |
| ` *`op`*` | `xsd:string` | Keuze van tekenreeksvergelijkingsoperatoren. |
| ` *`value`*` | `xsd:string` | Waarde waartegen moet worden getest. |
| ` *`boolVal`*` | `xsd:boolean` | Booleaanse vergelijkingswaarde. |
| ` *`longVal`*` | `xsd:long` | Lange vergelijkingswaarde. |
| ` *`minLong`*` | `xsd:long` | Ondergrens van lange reeks. |
| ` *`maxLong`*` | `xsd:long` | Bovengrens van lange afstand. |
| ` *`doubleVal`*` | `xsd:double` | Dubbele vergelijkingswaarde. |
| ` *`minDouble`*` | `xsd:double` | Ondergrens van dubbel bereik. |
| ` *`maxDouble`*` | `xsd:double` | Bovengrens van dubbel bereik. |
| ` *`dateVal`*` | `xsd:dateTime` | Vergelijkingswaarde datum. |
| ` *`minDate`*` | `xsd:dateTime` | Datumbereik minimaal. |
| ` *`maxDate`*` | `xsd:dateTime` | Maximaal datumbereik. |

## Voorbeeld {#section-347d4aabfff44530adba03d1dc0b9968}

```
<systemFieldConditionArray>
   <items>
      <field>LastModified</field>
      <op>Between</op>
      <minDate>2007-08-01T00:00:00</minDate>
      <maxDate>2007-12-01T00:00:00</maxDate>
   </items>
</systemFieldConditionArray>
```

