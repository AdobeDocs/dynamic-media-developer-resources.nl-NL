---
description: Keert IPS montages voor een specifiek bedrijf terug.
solution: Experience Manager
title: getCompanySettings
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: b9f41405-8a45-416c-acec-ef22c2ee119e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 0%

---

# getCompanySettings{#getcompanysettings}

Keert IPS montages voor een specifiek bedrijf terug.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-3378c9c67029473a87d5f5d8c616b1f3}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-e146f479c2744baa8f68be8c8848c97f}

**Input (getCompanySettingsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep naar het bedrijf waarvan u de instellingen wilt ophalen. |

**Output (getCompanySettingsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`instellingen`*` | `types:CompanySettings` | Ja | Bedrijfsinstellingen. |

## Voorbeelden {#section-191f78995ecf473a95eadf7296204fd7}

Deze codesteekproef keert alle IPS montages voor een specifiek bedrijf terug.

**Verzoek**

```java
<ns1:getCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
</ns1:getCompanySettingsParam>
```

**Antwoord**

```java
<getCompanySettingsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <settings>
      <metadataArray>
         <items>
            <name>Profile Class</name>
            <value>1</value>
            <longVal>1</longVal>
         </items>
         <items>
             <name>Default Color Profile</name>
             <value>1</value>
         </items>
      </metadataArray>
      <iccProfileInfo>
         <originalPath>Scene7SharedAssets/ICCColorProfiles/Adobe ICC Profiles/RGB Profiles/</originalPath>
         <originalFile>sRGB Color Space Profile.icm</originalFile>
         <fileSize>0</fileSize>
      </iccProfileInfo>
      </defaultDisplayProfile>
      <diskSpaceWarningMin>100000</diskSpaceWarningMin>
      <emailTrashCleanupWarning>true</emailTrashCleanupWarning>
   </settings>
</getCompanySettingsReturn>
```
