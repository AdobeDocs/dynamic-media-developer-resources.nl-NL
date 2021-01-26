---
description: Retourneert mappen en submappen in een hiërarchische boomstructuur. De reactie getFolderTree is beperkt tot maximaal 100.000 mappen
seo-description: Retourneert mappen en submappen in een hiërarchische boomstructuur. De reactie getFolderTree is beperkt tot maximaal 100.000 mappen
seo-title: getFolderTree
solution: Experience Manager
title: getFolderTree
topic: Dynamic Media Image Production System API
uuid: 93fda0d6-c656-4254-b07b-7a448e164f28
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---


# getFolderTree{#getfoldertree}

Retourneert mappen en submappen in een hiërarchische boomstructuur. De reactie getFolderTree is beperkt tot maximaal 100.000 mappen

Syntaxis

## Toegestane gebruikerstypen {#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>De gebruiker moet lees toegang tot de omslag hebben om gegevens op het terug te keren.

## Parameters {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**Input (getFolderTreeParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf. |
| `*`accessUserHandle`*` | `xsd:string` | Nee | Wordt alleen door beheerders gebruikt om zich voor te doen als een specifieke gebruiker. |
| `*`accessGroupHandle`*` | `xsd:string` | Nee | Wordt gebruikt om te filteren op een specifieke groep, inclusief een groep waartoe het bedrijf behoort. |
| `*`folderPath`*` | `xsd:string` | Nee | De hoofdmap om mappen en alle submappen op te halen naar bladniveau. Indien uitgesloten, wordt de bedrijfwortel gebruikt. |
| `*`diepte`*` | `xsd:int` | Ja | Bij de waarde nul wordt de map op hoofdniveau opgehaald. Elke andere waarde geeft de diepte aan die in de boomstructuur moet afnemen. |
| `*`assetTypeArray`*` | `types:StringArray` | Nee | Retourneert mappen die alleen opgegeven elementtypen bevatten. |
| `*`responseFieldArray`*` | `types:StringArray` | Nee | Bevat een lijst met velden die u wilt opnemen in het antwoord. |
| `*`excludeFieldArray`*` | `types:StringArray` | Nee | Bevat een lijst met velden die u wilt uitsluiten in het antwoord. |

**Output (getFolderTreeReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`mappen`*` | `types:folders` | Nee | De hiërarchie van mappen in een boomstructuur. De reactie is beperkt tot maximaal 100.000 mappen. |
| `*`permissionSetArray`*` | `types:PermissionSetArray` |  |  |

## Voorbeelden {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

Deze codesteekproef gebruikt een bedrijfshandvat en een diepteparameter om het niveau van diepte te bepalen de reactie zou moeten terugkeren. Het antwoord bevat mappen en submappenarrays met verwante items. Stel de dieptewaarde in op een kleiner getal om dieper in de mapstructuur te zoeken.

**Verzoek**

```java
<ns1:getFolderTreeParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:depth>-1</ns1:depth>
</ns1:getFolderTreeParam>
```

**Antwoord**

```java
<getFolderTreeReturn xmlns="http://www.scene7.com/IpsApi/xsd/">
  <folders>
    <items>
      <folderHandle>f|sampleFolder/uploadTestDir/</folderHandle>
      <path>MyCompany/uploadTestDir/</path>
      <lastModified>2011-11-14T11:19:59.031-08:00</lastModified>
      <childLastModified>2011-11-14T11:19:59.031-08:00</childLastModified>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <hasSubfolders>true</hasSubfolders>
      <subfolderArray>
        <items>
          <folderHandle>f|MyCompany/uploadTestDir/SubFolder/</folderHandle>
          <path>DevanCo/uploadTestDir/SubFolder/</path>
          <lastModified>2011-11-14T11:19:59.032-08:00</lastModified>
          <childLastModified>2011-11-14T11:19:59.032-08:00</childLastModified>
          <permissionSetHandle>pm|2</permissionSetHandle>
          <hasSubfolders>true</hasSubfolders>
          <subfolderArray>
            <items>
              <folderHandle>f|MyCompany/uploadTestDir/SubFolder/10/</folderHandle>
              <path>DevanCo/uploadTestDir/SubFolder/10/</path>
              <lastModified>2011-11-14T11:19:59.033-08:00</lastModified>
              <childLastModified>2011-11-14T15:06:58.563-08:00</childLastModified>
              <permissionSetHandle>pm|2</permissionSetHandle>
              <hasSubfolders>false</hasSubfolders>
            </items>
          </subfolderArray>
        </items>
      </subfolderArray>
    </items>
  </folders>
  <permissionSetArray>
    <items>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <permissionArray>
        <items>
          <groupHandle>g|1</groupHandle>
          <groupName>Asset Download Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>false</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Write</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
      </permissionArray>
    </items>
  <permissionSetArray>
</getFolderTreeReturn>
```

