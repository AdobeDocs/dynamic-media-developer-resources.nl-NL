---
description: Retourneert elementen die zijn gebaseerd op een array met namen van elementen.
seo-description: Retourneert elementen die zijn gebaseerd op een array met namen van elementen.
seo-title: getAssetsByName
solution: Experience Manager
title: getAssetsByName
topic: Scene7 Image Production System API
uuid: e86b3b16-ad93-4f70-9f59-b72395513c4c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getAssetsByName{#getassetsbyname}

Retourneert elementen die zijn gebaseerd op een array met namen van elementen.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-754790841ea242d5ae8bedd587d7730e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Hiermee worden alleen elementen geretourneerd waartoe de gebruiker leestoegang heeft.

## Parameters {#section-f64e93c127b84a29aa3bf2fdd916cca9}

**Input (getAssetsByNameParam)**

<table id="table_CE7B503B0E074719A523B458DF3A7286"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> bedrijfshandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> De handgreep aan het bedrijf. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Biedt toegang als een andere gebruiker. Alleen beschikbaar voor beheerders. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Wordt gebruikt om te filteren op een specifieke groep. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nameArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Array met elementnamen die moeten worden opgehaald. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Array met elementtypen die zijn toegestaan voor opgehaalde elementen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Array met elementtypen die zijn uitgesloten voor opgehaalde elementen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Array met elementsubtypen die zijn toegestaan voor opgehaalde elementen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> <p>Als <span class="codeph"> true</span> en <span class="codeph"> assetSubTypeArray</span> niet leeg is, worden alleen elementen geretourneerd waarvan de subtypen zich in <span class="codeph"> assetSubTypeArray</span> bevinden. </p> <p>Indien <span class="codeph"> false</span>, worden elementen zonder gedefinieerd subtype opgenomen. </p> <p>De standaardwaarde is <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Bevat een lijst met velden en subvelden die zijn opgenomen in het antwoord. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Bevat een lijst met velden en subvelden die zijn uitgesloten van de reactie. </td> 
  </tr> 
 </tbody> 
</table>

**Output (getAssetsByNameReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`assetArray`*` | `types:AssetArray` | Nee | Array met elementen die voldoen aan de filtercriteria. |

## Voorbeelden {#section-3b7447398e574c88aeaf8ca159cc78dd}

Dit codevoorbeeld retourneert twee elementen van het afbeeldingstype.

**Verzoek**

```java
<getAssetsByNameParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <nameArray>
      <items>B010</items>
      <items>IMG_0103</items>
   </nameArray>
   <assetTypeArray>
      <items>Image</items>
   </assetTypeArray>
</getAssetsByNameParam>
```

**Antwoord**

```java
<getAssetsByNameReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <assetArray>
      <items>
         <assetHandle>a|210</assetHandle>
         <type>Image</type>
         <name>B010</name>
         ...</items>
      <items>
         <assetHandle>a|189</assetHandle>
         <type>Image</type>
         <name>IMG_0103</name>
         ...
      </items>
   </assetArray>
</getAssetsByNameReturn>
```

