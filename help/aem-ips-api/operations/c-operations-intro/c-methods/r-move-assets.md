---
description: Hiermee verplaatst u meerdere elementen onafhankelijk van elkaar. Hiervoor wordt het type AssetMove gebruikt dat zich in de assetMoveArray bevindt. Elk veld AssetMove bevat een doelmap.
seo-description: Hiermee verplaatst u meerdere elementen onafhankelijk van elkaar. Hiervoor wordt het type AssetMove gebruikt dat zich in de assetMoveArray bevindt. Elk veld AssetMove bevat een doelmap.
seo-title: moveAssets
solution: Experience Manager
title: moveAssets
topic: Scene7 Image Production System API
uuid: 178f9979-fff5-45ce-a001-1263d1770ea8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# moveAssets{#moveassets}

Hiermee verplaatst u meerdere elementen onafhankelijk van elkaar. Hiervoor wordt het type AssetMove gebruikt dat zich in de assetMoveArray bevindt. Elk veld AssetMove bevat een doelmap.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-4166515fd9d8487b8af37465ce61802b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-7d47f663474b41cc83439288ac133cc5}

**Input (moveAssetsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf met activa om worden bewogen. |
| ` *`assetMoveArray`*` | `types:AssetMoveArray` | Ja | Een array met elementen verplaatsen. Het bevat een middel en een omslag van de middelenbestemming. |

**Output (moveAssetsReturn)**

<table id="table_FD902FAB4F98413C8A051270ADD7D9C7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Naam </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Vereist </th> 
   <th colname="col4" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> successCount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Telling van elementen verplaatst. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningCount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Aantal elementen dat waarschuwingen heeft gegenereerd toen de bewerking deze probeerde te verplaatsen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorCount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Aantal elementen dat fouten genereerde toen de bewerking deze probeerde te verplaatsen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningDetailArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <span class="codeph"></span>AssetOperationFaultsthat contain the: 
    <ul id="ul_689F4A87A68140F18DFB43868226A409"> 
     <li id="li_274C8BF5932F4AF584AA92F25E0F33C6">Middelen die de waarschuwingen gaven. </li> 
     <li id="li_5CC4A9120CA94F968CAF0D0135C49E0A">Waarschuwingscodes. </li> 
     <li id="li_AEC91FA68B2E43BC8BAA108C743F5667">Reden voor de waarschuwing. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorDetailArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <span class="codeph"></span>AssetOperationFaultsthat contain the: 
    <ul id="ul_C397BC384A134F429D01ADA28DF2E097"> 
     <li id="li_EAEBB5F539164480BA9EAA7C8FFBF69A">Middelen die de fouten hebben veroorzaakt. </li> 
     <li id="li_F96D5FBB2F7A402AA36D8DFA3971391D">Foutcodes. </li> 
     <li id="li_F610415E416F43DDA4B1DBF1897E2F61">Reden voor de fouten. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeelden {#section-c31ed4c004ab4b3fa42c96d26ceb5ce7}

In dit codevoorbeeld worden elementen verplaatst naar een specifieke locatie die door het `assetMoveArray`voorbeeld wordt opgegeven. De array bevat de elementgreep en de bijbehorende maphandgreep. De reactie geeft aan dat de elementen zijn verplaatst.

**Verzoek**

```java
<moveAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetMoveArray>
      <items>
          <assetHandle>a|942|1|579</assetHandle>
          <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
      <items>
         <assetHandle>a|943|1|580</assetHandle>
         <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
   </assetMoveArray>
</moveAssetsParam>
```

**Antwoord**

```java
<moveAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</moveAssetsReturn>
```

