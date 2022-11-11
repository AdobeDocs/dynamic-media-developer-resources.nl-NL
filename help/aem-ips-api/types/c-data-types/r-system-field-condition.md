---
description: Een zoekvoorwaarde voor het systeemveld voor de bewerking searchAssets.
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# [!DNL SystemFieldCondition]{#systemfieldcondition}

Een zoekvoorwaarde voor het systeemveld voor de bewerking searchAssets.

Geef voor unaire vergelijkingen exact één waarde door ( `boolVal`, `longVal`, `doubleVal`, of `dateVal`), afhankelijk van het type systeemveld. Voor zoekbereiken geeft u door `min<Type>` en `max<Type>` parameters en een `op` waarde van `Between` of `NotBetween`.

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| field | `xsd:string` | Keuze van velden voor het zoeken naar middelen. |
| op | `xsd:string` | Keuze van tekenreeksvergelijkingsoperatoren. |
| value | `xsd:string` | Waarde waartegen moet worden getest. |
| boolVal | `xsd:boolean` | Booleaanse vergelijkingswaarde. |
| longVal | `xsd:long` | Lange vergelijkingswaarde. |
| minLong | `xsd:long` | Ondergrens van lange reeks. |
| maxLong | `xsd:long` | Bovengrens van lange afstand. |
| doubleVal | `xsd:double` | Dubbele vergelijkingswaarde. |
| minDouble | `xsd:double` | Ondergrens van dubbel bereik. |
| maxDouble | `xsd:double` | Bovengrens van dubbel bereik. |
| dateVal | `xsd:dateTime` | Vergelijkingswaarde datum. |
| minDate | `xsd:dateTime` | Datumbereik minimaal. |
| maxDate | `xsd:dateTime` | Maximaal datumbereik. |

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
