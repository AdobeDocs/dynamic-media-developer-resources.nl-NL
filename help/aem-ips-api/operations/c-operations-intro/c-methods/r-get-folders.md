---
description: Retourneert alle mappen en submappen, te beginnen bij het mappad. De reactie getFolders retourneert maximaal 100.000 mappen.
solution: Experience Manager
title: getFolders
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 71fe3343-2560-4d74-8ec3-1229d83a62e1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# getFolders{#getfolders}

Retourneert alle mappen en submappen, te beginnen bij het mappad. De reactie getFolders retourneert maximaal 100.000 mappen.

## Doel van mappen {#section-66e344d5333f42f1b060a0cba25935c3}

Met een map kunt u submappen en elementen ordenen. Alle map- en elementnamen moeten uniek zijn. Mappen en elementen met dezelfde naam veroorzaken een naamruimteconflict, zelfs als ze zich in verschillende maphiërarchieën bevinden.
Syntaxis

## Geautoriseerde gebruikerstypen {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>De gebruiker moet lees toegang tot de omslag hebben om gegevens op het terug te keren.

## Parameters {#section-0c1976503eaa418a9226b51667901176}

**Input (getFoldersParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | De handgreep aan het bedrijf. |
| accessUserHandle | `xsd:string` | Nee | Wordt gebruikt door beheerders om zich voor te doen als een specifieke gebruiker. |
| accessGroupHandle | `xsd:string` | Nee | Filteren op een specifieke groep. |
| folderPath | `xsd:string` | Nee | De hoofdmap om mappen en alle submappen op te halen naar bladniveau. Indien uitgesloten, wordt de bedrijfwortel gebruikt. |
| assetTypeArray | `types:StringArray` | Nee | Retourneert mappen die alleen opgegeven elementtypen bevatten. |
| responseFieldArray | `types:StringArray` | Nee | Bevat een lijst met velden die u wilt opnemen in het antwoord. |
| excludeFieldArray | `types:StringArray` | Nee | Bevat een lijst met velden die u wilt uitsluiten van de reactie. |

**Output (getFoldersReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| folderArray | `types:FolderArray` | Nee | Een array met mappen die voldoen aan de filtercriteria. De reactie is beperkt tot maximaal 100.000 mappen. |
| permissionsSetArray | `types:PermissionSetArray` |  |  |

## Voorbeelden {#section-b5cb06e9fb9945ad898dbdc3692b754e}

Dit codevoorbeeld keert een serie terug die alle omslagen voor een bedrijf samen met specifieke informatie over elke omslag bevat.

**Verzoek**

```java
<ns1:getFoldersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getFoldersParam>
```

**Antwoord**

```java
<getFoldersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderArray>
      <items>
         <folderHandle>MyCompany/</folderHandle>
         <path>MyCompany/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/eCatalogs/</folderHandle>
         <path>MyCompany/eCatalogs/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/PDF/</folderHandle>
         <path>MyCompany/PDF/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
   </folderArray>
</getFoldersReturn>
```
