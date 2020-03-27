---
description: Hiermee wordt een specifieke taak uitgevoerd.
seo-description: Hiermee wordt een specifieke taak uitgevoerd.
seo-title: executeJob
solution: Experience Manager
title: executeJob
topic: Scene7 Image Production System API
uuid: e73223c1-9032-4745-92b6-a5840949a824
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# executeJob{#executejob}

Hiermee wordt een specifieke taak uitgevoerd.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-8199e8599ea64e7097a2acb633417b15}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-2c61b2bffcf9479a9391f2c13fdf7d53}

**Input (executeJobParam)**

<table id="table_FA410513908F4084A21A5F0A9431006C"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> bedrijfshandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>De handgreep van het bedrijf waartoe de baan behoort. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> taakhandgreep</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>De greep naar de taak die moet worden uitgevoerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (executeJobReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-96f71aa58a954293b9a98ff96d86f232}

Deze codesteekproef stelt een baan in werking die om in IPS gepland is te lopen.

**Verzoek**

```java
<executeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</executeJobParam>
```

**Antwoord**

Geen.
