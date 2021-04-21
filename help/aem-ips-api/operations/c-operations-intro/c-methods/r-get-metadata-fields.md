---
description: Hiermee worden de door de gebruiker gedefinieerde metagegevensvelden opgehaald die aan een element zijn gekoppeld.
solution: Experience Manager
title: getMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# getMetadataFields{#getmetadatafields}

Hiermee worden de door de gebruiker gedefinieerde metagegevensvelden opgehaald die aan een element zijn gekoppeld.

Syntaxis

## Toegestane gebruikerstypen {#section-e32e481a02674b729bfc5454a6c9ff65}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-bac949e59c0546429c5786fe422d750d}

**Input (getMetadataFieldsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep van het bedrijf. |
| `*`assetType`*` | `xsd:string` | Ja | Elementen waarvan metagegevens kunnen worden opgehaald. |

**Output (getMetadataFieldsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`Codewoordgroep`*` | `Code Phrase` |  |  |

## Voorbeelden {#section-dbfde1483d614b5aac2b491cb32115d7}

Deze codesteekproef keert meta-gegevensactiva voor het gespecificeerde type en bedrijf terug. De reactie bevat een array met metagegevensvelden in een veldarray. Niet alle elementen hebben dezelfde metagegevens. De IPS-gebruiker definieert het metagegevensveld van het element.

**Verzoek**

```java
<ns1:getMetadataFieldsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
</ns1:getMetadataFieldsParam>
```

**Antwoord**

```java
<getMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldArray>
      <items>
         <fieldHandle>47|ALL|Resolution</fieldHandle>
         <name>Resolution</name>
         <type>String</type>
         <defaultValue>120</defaultValue>
         <isRequired>false</isRequired>
         <isUserDefined>true</isUserDefined>
      </items>
   </fieldArray>
</getMetadataFieldsReturn>
```

