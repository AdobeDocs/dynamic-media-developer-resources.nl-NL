---
description: Hiermee wordt informatie over het opgegeven bedrijf geretourneerd, inclusief de greep van het bedrijf, de naam van het bedrijf, het hoofdpad en de vervaldatum. U moet of companyHandle of companyName specificeren waarvan informatie u wilt terugwinnen.
seo-description: Hiermee wordt informatie over het opgegeven bedrijf geretourneerd, inclusief de greep van het bedrijf, de naam van het bedrijf, het hoofdpad en de vervaldatum. U moet of companyHandle of companyName specificeren waarvan informatie u wilt terugwinnen.
seo-title: getCompanyInfo
solution: Experience Manager
title: getCompanyInfo
topic: Dynamic Media Image Production System API
uuid: 9218cba8-2873-46b7-90e3-7ab9d5018690
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# getCompanyInfo{#getcompanyinfo}

Hiermee wordt informatie over het opgegeven bedrijf geretourneerd, inclusief de greep van het bedrijf, de naam van het bedrijf, het hoofdpad en de vervaldatum. U moet of companyHandle of companyName specificeren waarvan informatie u wilt terugwinnen.

Syntaxis

## Toegestane gebruikerstypen {#section-74f20fb8602e4f96810795bc4b6f7fdf}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-7dec8871c89a414c9f066adade1831d8}

**Input (getCompanyInfoParam)**

<table id="table_DD2688C9DA9F49C9ABCA24944829B3E5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Naam </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Vereist </p> </th> 
   <th colname="col4" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>Of <span class="codeph"> <span class="varname"> companyHandle</span> </span> of <span class="codeph"> <span class="varname"> companyName</span> </span> is vereist. </p> </td> 
   <td colname="col4"> <p>De handgreep van het bedrijf waarvan informatie u wilt verkrijgen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>Of <span class="codeph"> <span class="varname"> companyHandle</span> </span> of <span class="codeph"> <span class="varname"> companyName</span> </span> is vereist. </p> </td> 
   <td colname="col4"> <p>De naam van het bedrijf waarvan informatie u wilt verkrijgen. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (getCompanyInfoReturn)**

<table id="table_634D4E274BA7494C9C917FD244286F0D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Naam </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Vereist </p> </th> 
   <th colname="col4" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyInfo</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typen:Bedrijf</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Handle en andere beschrijvende informatie over het bedrijf. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeelden {#section-3d5342aa7cb34b1fa84d7dea6e16e4aa}

Deze codesteekproef keert alle informatie over een bedrijf door een bedrijfsnaam en handvat te gebruiken terug. Het keert gegevens terug gelijkend op de reactie die werd ontvangen toen het creëren van een bedrijf.

**Verzoek**

```java
<ns1:getCompanyInfoParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:getCompanyInfoParam>
```

**Antwoord**

```java
<ns1:getCompanyInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:getCompanyInfoReturn>
```

