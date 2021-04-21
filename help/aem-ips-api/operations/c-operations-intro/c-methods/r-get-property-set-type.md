---
description: Haalt een type eigenschapset op met een greep naar een bedrijf en de naam van het type eigenschapset. Het krijgt een typestructuur met de handvatten aan het type evenals het bezitstype.
solution: Experience Manager
title: getPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---


# getPropertySetType{#getpropertysettype}

Haalt een type eigenschapset op met een greep naar een bedrijf en de naam van het type eigenschapset. Het krijgt een typestructuur met de handvatten aan het type evenals het bezitstype.

Syntaxis

## Toegestane gebruikerstypen {#section-2b291d32f95b4a3d854429124cbae24c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-c9a53400c44744668bd7915f72d2bf3d}

**Input (getPropertySetTypeParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Nee | De handgreep aan het bedrijf. Optioneel omdat een type eigenschapset tot meerdere bedrijven kan behoren. |
| `*`name`*` | `xsd:string` | Ja | Naam van type eigenschappenset. |

**Output (getPropertySetTypeReturn)**

<table id="table_F2724F6B706C4F658AED99290E29F3E6"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:PropertySetType</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4">De typestructuur die a bevat: 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">Handgreep. </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">Typ naam. </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">Type eigenschap. </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">Waarde die aangeeft of het type meerdere eigenschapstypen toestaat. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeelden {#section-1b57199415e34a8fa449f864f8895b14}

Deze codesteekproef keert een bezitsplaatstype door naam terug.

**Verzoek**

```java
<getPropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <name>Adobe.UserProperty</name>
</getPropertySetTypeParam>
```

**Antwoord**

```java
<getPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <type>
      <typeHandle>pt|10801</typeHandle>
      <name>Adobe.UserProperty</name>
      <propertyType>UserProperty</propertyType>
      <allowMultiple>false</allowMultiple></type>
</getPropertySetTypeReturn>
```

