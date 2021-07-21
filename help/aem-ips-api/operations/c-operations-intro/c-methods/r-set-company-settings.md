---
description: Hiermee stelt u verschillende bedrijfsspecifieke configuratiewaarden in.
solution: Experience Manager
title: setCompanySettings
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: c6b72ceb-3c86-4b13-89e9-5f1bb9846b2c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# setCompanySettings{#setcompanysettings}

Hiermee stelt u verschillende bedrijfsspecifieke configuratiewaarden in.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-a472da6c57c74a94a179dda081004888}

**Input (setCompanySettingsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Bedrijfshandgreep. |
| `*`overwriteMode`*` | `xsd:string` | Nee | De modus voor het overschrijven van elementen. |
| `*`preservePublishState`*` | `xsd:boolean` | Nee | Stel in op `true` om de publicatiestatus te behouden wanneer een element opnieuw wordt geüpload. |
| `*`defaultSourceProfileHandle`*` | `xsd:string` | Nee | IccProfile-element dat als standaardbronkleurprofiel moet worden gebruikt. |
| `*`defaultDisplayProfileHandle`*` | `xsd:string` | Nee | IccProfile-element om als standaardkleurprofiel voor de weergave te gebruiken. |
| `*`iptcExifMappingXsltHandle`*` | `xsd:string` | Nee | XSL-element dat wordt gebruikt voor het toewijzen van IPTC- en EXIF-metagegevens aan IPS-metagegevensvelden. |
| `*`xmpMappingXsltHandle`*` | `xsd:string` | Nee | XSL-element dat wordt gebruikt om XMP metagegevens toe te wijzen aan IPS-metagegevensvelden. |
| `*`diskSpaceWarningMin`*` | `xsd:int` | Nee | Minimale vrije schijfruimte (in kB) beschikbaar voordat een waarschuwingsbericht wordt verzonden. |
| `*`emailTrashCleanupWarning`*` | `xsd:boolean` | Nee | Stel in op `true` om bedrijfsbeheerders een melding te sturen wanneer middelen uit de prullenbak worden verwijderd. |

**Output (setCompanySettingsReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

Deze codesteekproef plaatst de configuratie van een bedrijf.

**Verzoek**

```java
<ns1:setCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
   <ns1:overwriteMode>OverwriteFullName</ns1:overwriteMode>
   <ns1:retainPublishState>true</ns1:retainPublishState>
   <ns1:diskSpaceWarningMin>100000</ns1:diskSpaceWarningMin>
   <ns1:emailTrashCleanupWarning>true</ns1:emailTrashCleanupWarning>
</ns1:setCompanySettingsParam>
```

**Antwoord**

Geen.
