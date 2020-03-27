---
description: Hiermee stelt u de lijst in met elementen die aan een afbeeldingsset zijn gekoppeld.
seo-description: Hiermee stelt u de lijst in met elementen die aan een afbeeldingsset zijn gekoppeld.
seo-title: setImageSetMember
solution: Experience Manager
title: setImageSetMember
topic: Scene7 Image Production System API
uuid: 84a73ff4-e93f-4764-80e8-e15f1fec1aeb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setImageSetMember{#setimagesetmembers}

Hiermee stelt u de lijst in met elementen die aan een afbeeldingsset zijn gekoppeld.

Deze bewerking negeert de `pageReset` parameter voor `ImageSets` en `SpinSets` en dwingt de waarde tot true.

## Geautoriseerde gebruikerstypen {#section-8968d6a39a344cfc8521020d92ae8916}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>De gebruiker moet lees- en schrijftoegang hebben tot het element met de afbeeldingsset en leestoegang tot elk element van het lid.

## Parameters {#section-2f46efcd24c648aeacba738509426e46}

**Input (setImageSetMemberParam)**

<table id="table_0CBBB65BCEFD4125A4069A080DFC873A"> 
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
   <td colname="col4"> <p>Bedrijfshandgreep. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Afbeeldingssethandgreep. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageSetMemberUpdateArray</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Array met elementleden die bij de afbeeldingsset horen. </td> 
  </tr> 
 </tbody> 
</table>

**Output (setImageSetMemberReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-7b87219034464aa98524178ccee27738}

In dit codevoorbeeld wordt een lidarray gebruikt om de leden van een afbeeldingsset in te stellen.

**Verzoek**

```java
<setImageSetMembersParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>34205|22|929</assetHandle>
   <memberArray>
      <items>
         <assetHandle>24266|1|17062</assetHandle>
         <pageReset>true</pageReset>
      </items>
   </memberArray>
</setImageSetMembersParam>
```

**Antwoord**

Geen.
