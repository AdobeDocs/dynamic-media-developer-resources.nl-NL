---
description: Hiermee definieert u zoekvoorwaarden voor tagvelden.
solution: Experience Manager
title: TagCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---


# TagCondition{#tagcondition}

Hiermee definieert u zoekvoorwaarden voor tagvelden.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Naam </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Handgreep van tagveld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3">Afhankelijk van het veldtype van de tag en of het veld valueArray wordt gebruikt. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">Wanneer <span class="codeph"> value</span> wordt doorgegeven, moet <span class="codeph"> op</span> de tekenreeksconstante Matches zijn. De voorwaarde komt overeen met elk element dat aan de tagwaarde is gekoppeld. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">Wanneer <span class="codeph"> valueArray</span> wordt doorgegeven, kan het op-veld de constante <span class="codeph"> MatchesAny</span> zijn voor enkelvoudige of multigetaxeerde tagvelden. Een <span class="codeph"> voorwaarde MatchesAny</span> komt overeen met elk element dat is gekoppeld aan ten minste een van de tagwaarden in <span class="codeph"> valueArray</span>. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">Voor velden met meerdere tags kan het veld op worden ingesteld op de constante <span class="codeph"> MatchesAll</span> met het veld <span class="codeph"> valueArray</span>. In dit geval komt de voorwaarde alleen overeen met elementen die zijn gekoppeld aan alle tagwaarden in <span class="codeph"> valueArray</span> (mogelijk naast andere tagwaarden). </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Een overeenkomende waarde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Meerdere overeenkomende waarden. </td> 
  </tr> 
 </tbody> 
</table>

