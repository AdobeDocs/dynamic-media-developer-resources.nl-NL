---
description: Voegt een bedrijf aan het systeem toe.
seo-description: Voegt een bedrijf aan het systeem toe.
seo-title: addCompany
solution: Experience Manager
title: addCompany
topic: Scene7 Image Production System API
uuid: 2f00a06d-40d1-4ba3-a317-6ea91e25beb3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---


# addCompany{#addcompany}

Voegt een bedrijf aan het systeem toe.

Verzendt de naam van het bedrijf dat aan het systeem moet worden toegevoegd en naar keuze verzendt of het bedrijf verloopt.

Wanneer deze verrichting wordt aangehaald, krijgt het systeem een ` *`companyInfo`*` type dat een bedrijfshandvat en beschrijvende gebieden bevat. Als de aangevraagde bedrijfsnaam al in het systeem bestaat, wordt een `ipsApiFault` gegenereerd.

## Toegestane gebruikerstypen {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-c64a21b72585447880760db9e7a12ccb}

**Input (addCompanyParam)**

<table id="table_AA915BAD2E8E4A1B9719725994309CE8"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>De naam van het bedrijf dat moet worden toegevoegd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> verloopt</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:dateTime</span> </p> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>Vervaldatum van de onderneming. Geef de tijdzone het verzoek voor dit veld. Tijdzones worden aangepast aan de Central Time. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (addCompanyReturn)**

<table id="table_89EBAC0E0FB34793BD843837BB02B518"> 
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
   <td colname="col2"> <p><span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Handgreep aan en naam, wortelweg, vervaldatum, en tijd van het nieuwe bedrijf. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeelden {#section-4c8f1bb40d154c77a7b410468206e52b}

Dit voorbeeld toont een verzoek aan om een bedrijf aan het IPS systeem en de reactie toe te voegen detailend de informatie over het toegevoegde bedrijf dat nodig is om andere verrichtingen uit te voeren.

**Verzoek**

```java
<ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:addCompanyParam>
```

**Antwoord**

```java
<ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:addCompanyReturn>
```

