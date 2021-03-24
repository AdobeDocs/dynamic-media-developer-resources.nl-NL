---
description: Hiermee worden unieke veldwaarden voor metagegevens opgehaald.
solution: Experience Manager
title: getUniqueMetadataValues
feature: Dynamic Media Classic,SDK/API,metagegevens
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 1%

---


# getUniqueMetadataValues{#getuniquemetadatavalues}

Hiermee worden unieke veldwaarden voor metagegevens opgehaald.

Syntaxis

## Toegestane gebruikerstypen {#section-6a6b67e10a4c4e7bb18306115713380e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-b9d1413811c24566b6d095701f0f66db}

**Input (getUniqueMetadataValuesParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handgreep aan het bedrijf. |
| `*`fieldHandle`*` | `xsd:string` | Nee | Handgreep aan meta-gegevensgebied. |

**Output (getUniqueMetadataValuesReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`values`*` | `type:StringArray` |  |  |

## Voorbeelden {#section-440f3bc3e5be436cb6ec26117d05f476}

In dit codevoorbeeld wordt een veldgreep gebruikt om specifieke metagegevenswaarden te retourneren.

**Verzoek**

```java
<ns1:getUniqueMetadataValuesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
</ns1:getUniqueMetadataValuesParam>
```

**Antwoord**

```java
<getUniqueMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <values>
      <items>320</items>
   </values>
</getUniqueMetadataValuesReturn>
```

