---
description: Haalt de types van bezitsreeks verbonden aan het gespecificeerde bedrijf, of globale bezitsvastgestelde types op als geen bedrijf wordt gespecificeerd.
seo-description: Haalt de types van bezitsreeks verbonden aan het gespecificeerde bedrijf, of globale bezitsvastgestelde types op als geen bedrijf wordt gespecificeerd.
seo-title: getPropertySetTypes
solution: Experience Manager
title: getPropertySetTypes
topic: Scene7 Image Production System API
uuid: b707344d-5571-45eb-9e37-cf0894ee81a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getPropertySetTypes{#getpropertysettypes}

Haalt de types van bezitsreeks verbonden aan het gespecificeerde bedrijf, of globale bezitsvastgestelde types op als geen bedrijf wordt gespecificeerd.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-9c7c0d2cd2c94dfca3f96774b3a9a2c6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-ac3ed9e036b54ea993f544046ff0e15d}

**Input (getPropertySetTypesParam)**

<table id="table_2590368FEEF04AD4B074412CBBA90F88"> 
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
   <td colname="col3"> Nee </td> 
   <td colname="col4">De handgreep aan het bedrijf waaraan de types van bezitsreeks worden geassocieerd. <p>Laat weg als u globale bezitsvastgestelde types wilt terugkeren. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (getPropertySetTypesReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`typeArray`*` | `types:PropertySetTypeArray` | Ja | Een serie van bezitsvastgestelde types verbonden aan het gespecificeerde bedrijf, of de globale types van bezitsreeks als geen bedrijf werd gespecificeerd. |

## Voorbeelden {#section-280c406a90864409856aee44d4069a52}

**Verzoek**

```java
<getPropertySetTypesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <companyHandle>c|1</companyHandle>
</getPropertySetTypesParam>
```

**Antwoord**

```java
<getPropertySetTypesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <typeArray>
    <items>
      <typeHandle>pt|1</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>SavedSearch</name>
      <propertyType>UserCompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
    <items>
      <typeHandle>pt|2</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>CompanyMetadata</name>
      <propertyType>CompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
  </typeArray>
</getPropertySetTypesReturn>
```

