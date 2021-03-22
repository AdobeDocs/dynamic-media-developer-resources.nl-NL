---
description: Hiermee verwijdert u het metagegevensveld van een bedrijf.
seo-description: Hiermee verwijdert u het metagegevensveld van een bedrijf.
seo-title: deleteMetadataField
solution: Experience Manager
title: deleteMetadataField
uuid: 06ec434a-2793-4227-ac93-ae3871c38ab9
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---


# deleteMetadataField{#deletemetadatafield}

Hiermee verwijdert u het metagegevensveld van een bedrijf.

Syntaxis

## Toegestane gebruikerstypen {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameters {#section-73f12a30cc4340b6b32dd11effd5195e}

**Input (deleteMetadataFieldParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De greep naar het bedrijf dat het metagegevensveld bevat dat moet worden verwijderd. |
| `*`fieldHandle`*` | `xsd:string` | Ja | De greep naar het metagegevensveld dat moet worden verwijderd. |

**Output (deleteMetadataFieldParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-e1c474ea91a040609ecd7c2400f4fa3c}

In dit codevoorbeeld wordt het metagegevensveld van een bedrijf verwijderd. Het gebruikt het bedrijfs handvat en meta-gegevenshandvat als gebieden in `deleteMetadataFieldParam` die binnen aan de IPS de dienstenserver van het Web worden overgegaan om deze actie uit te voeren.

**Verzoek**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**Antwoord**

Geen.0
