---
description: Stelt metagegevenswaarden in voor een specifiek element dat wordt gebruikt met setAssetMetadata. Beschrijft de veranderingen u aan meta-gegevens wilt aanbrengen.
seo-description: Stelt metagegevenswaarden in voor een specifiek element dat wordt gebruikt met setAssetMetadata. Beschrijft de veranderingen u aan meta-gegevens wilt aanbrengen.
seo-title: MetadataUpdate
solution: Experience Manager
title: MetadataUpdate
topic: Dynamic Media Image Production System API
uuid: 09d3940b-117d-4d83-8b12-e86520c9da34
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---


# MetadataUpdate{#metadataupdate}

Stelt metagegevenswaarden in voor een specifiek element dat wordt gebruikt met setAssetMetadata. Beschrijft de veranderingen u aan meta-gegevens wilt aanbrengen.

>[!NOTE]
>
>Als het veld Eén waarde wordt doorgegeven, wordt de tagwaarde van het element weer ingesteld op de opgegeven tagwaarde.

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
   <td colname="col3"> Handgreep metagegevensveld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Update-waarde metagegevens. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Booleaanse metagegevenswaarde (alleen voor velden met een Booleaans type). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> longVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> Lange metagegevenswaarde (alleen voor velden van het type int). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dubbel</span> </td> 
   <td colname="col3"> Dubbele metagegevenswaarde (alleen voor velden met floattype). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dateVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Waarde metagegevens datum (alleen voor datumvelden). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> addTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> <p>Hiermee voegt u een waarde toe aan de bestaande lijst met tagwaarden voor het element. 
     <ul id="ul_08DE6C490B614560A6118E7AC59720E3"> 
      <li id="li_358A3BDC0EC94CCF8178CD789F09F804">In tagvelden met één waarde wordt alleen de laatste waarde opgeslagen. </li> 
      <li id="li_3F47D3A3C63A4752BF9A45F7B00A6E70">Een veld voor een tag van een vaste-woordenlijst retourneert een fout als de waarde niet in het woordenboek staat. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3">Hiermee vervangt u de bestaande lijst met tagwaarden voor het element. 
    <ul id="ul_941C915C69E84CF2AC5938378837EB92"> 
     <li id="li_6E85019335034B2EB1302696AE690ED5">In tagvelden met één waarde wordt alleen de laatste waarde opgeslagen. </li> 
     <li id="li_0DC56717EBB642D29FB7A3D043CEDED1">Een veld voor een tag van een vaste-woordenlijst retourneert een fout als de waarde niet in het woordenboek staat. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> deleteTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Hiermee verwijdert u de opgegeven waarden uit de lijst met tagwaarden van het element, indien aanwezig. </td> 
  </tr> 
 </tbody> 
</table>

