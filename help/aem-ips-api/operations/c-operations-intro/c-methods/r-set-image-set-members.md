---
description: Hiermee stelt u de lijst in met elementen die aan een afbeeldingsset zijn gekoppeld.
solution: Experience Manager
title: setImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: c30df5fe-e355-45d4-8c06-e396caca0d58
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# setImageSetMember{#setimagesetmembers}

Hiermee stelt u de lijst in met elementen die aan een afbeeldingsset zijn gekoppeld.

Deze bewerking negeert de `pageReset` parameter for `ImageSets` en `SpinSets` en wordt de waarde ingesteld op true.

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Bedrijfshandgreep. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Afbeeldingssethandgreep. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span> </span> </td> 
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
