---
description: Informatie over taakvoortgang.
seo-description: Informatie over taakvoortgang.
seo-title: TaskProgress
solution: Experience Manager
title: TaskProgress
topic: Scene7 Image Production System API
uuid: b3b67803-147a-48a3-acc3-d608e01e0800
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---


# TaskProgress{#taskprogress}

Informatie over taakvoortgang.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Beschrijving van taaktype. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numVerwerkt</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Aantal reeds verwerkte taakpunten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessing</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Aantal taakitems dat momenteel wordt uitgevoerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numPending</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Aantal hangende taakonderdelen (nog niet verwerkt). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> vordering</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dubbel</span> </td> 
   <td colname="col3"> % voortgang (bereik 0,0 - 1,0). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Voortgangsbericht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Tijd waarop de laatste voortgangsinformatie voor het laatst is bijgewerkt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskItemProgressArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:TaskItemProgressArray</span> </td> 
   <td colname="col3"> Array met taakitems. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3">Waarden zijn: 
    <ul id="ul_BD00DC855B1D42748204E8BCA81FD4BF">
     <li id="li_01FE691763B3465DBF3402E7CDEA50C3"><span class="codeph"> Onbekend</span>: Wanneer de taakmonitor overgaat tussen staten. </li>
     <li id="li_AA2D1F9ADDE84B54A85C7E7830D3A0C9"><span class="codeph"> Nieuw</span>: De taakmonitor is gemaakt, maar heeft nog geen taken geaccepteerd. </li>
     <li id="li_76D667D21BDF4FADA6A266A7EB4DC6EE"><span class="codeph"> Verwerking</span>: De controle van de taak verwerkt actieve taken. </li>
     <li id="li_3813B2178D7143DEB91804A6C5FF3902"><span class="codeph"> Stoppen</span>: De monitor van de taak stopt een baan wegens een verzoek van de eindetaak. </li>
     <li id="li_41C2E774FC504B58BD6736119AE9C0AE"><span class="codeph"> Gereed</span>: De taken die aan de taken van de taakmonitor zijn toegewezen zijn voltooid. </li>
     <li id="li_EB2322BB11314B97998D467F4620ED2E"><span class="codeph"> Mislukt</span>: Geeft een fatale fout aan. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

