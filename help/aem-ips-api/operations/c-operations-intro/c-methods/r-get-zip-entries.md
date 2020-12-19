---
description: Retourneert Zip-bestandsgegevens.
seo-description: Retourneert Zip-bestandsgegevens.
seo-title: getZipEntry
solution: Experience Manager
title: getZipEntry
topic: Scene7 Image Production System API
uuid: cfc45f83-1cf9-4c50-9aac-5a731e62a839
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---


# getZipEnapters{#getzipentries}

Retourneert Zip-bestandsgegevens.

Syntaxis

## Toegestane gebruikerstypen {#section-33a3f03ba8a14086922397619ce12ab8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-aa3f498fe76d4a5f99c42d64520fadce}

**Input (getZipEntificationsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep naar het bedrijf dat het ZIP-bestand bevat. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Verwerk het ZIP-bestand. |

**Output (getZipEnaptersReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`zipArray`*` | `types:ZipEntryArray` | Ja | Array met items in een ZIP-bestand. |

## Voorbeelden {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

Dit codevoorbeeld retourneert ZIP-bestandsinformatie, inclusief gecomprimeerde en niet-gecomprimeerde grootte.

**Verzoek**

```java
<getZipEntriesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|94223|27|30602</assetHandle>
</getZipEntriesParam>
```

**Antwoord**

```java
<getZipEntriesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zipArray
      <items>
         <name>Checklist_Images/.DS_Store</name>
         <isDirectory>false</isDirectory>
         <lastModified>2007-05-09T15:41:52.000-07:00</lastModified>
         <compressedSize>503</compressedSize>
         <uncompressedSize>6148</uncompressedSize>
      </items>
   ...
   </zipArray>
</getZipEntriesReturn>
```

