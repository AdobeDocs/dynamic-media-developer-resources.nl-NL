---
description: Hiermee verwijdert u het metagegevensveld van een bedrijf.
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1922fc1b-2abc-4d31-985a-65c788af4d46
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# deleteMetadataField{#deletemetadatafield}

Hiermee verwijdert u het metagegevensveld van een bedrijf.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-73f12a30cc4340b6b32dd11effd5195e}

**Input (deleteMetadataFieldParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | De greep naar het bedrijf dat het metagegevensveld bevat dat moet worden verwijderd. |
| fieldHandle | `xsd:string` | Ja | De greep naar het metagegevensveld dat moet worden verwijderd. |

**Output (deleteMetadataFieldParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-e1c474ea91a040609ecd7c2400f4fa3c}

In dit codevoorbeeld wordt het metagegevensveld van een bedrijf verwijderd. De handgreep van het bedrijf en de verwerking van metagegevens worden gebruikt als velden in het dialoogvenster `deleteMetadataFieldParam` overgegaan binnen tot de IPS de dienstenserver van het Web om deze actie uit te voeren.

**Verzoek**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**Antwoord**

Geen.0
