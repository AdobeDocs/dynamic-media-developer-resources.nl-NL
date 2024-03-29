---
description: Binnen dit type is het pageReset-veld relevant voor renderSet- en Catalog-afbeeldingselementtypen
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# [!DNL ImageSetMemberUpdate]{#imagesetmemberupdate}

Binnen dit type is het pageReset-veld relevant voor de renderset- en catalogusafbeeldingselementtypen:

* Voor `RenderSet`, `pageReset` Hiermee wordt het begin van een nieuwe renderweergave/staalgroep aangegeven.

* Voor Catalog: `pageReset` Hiermee wordt het begin van een nieuwe paginaweergave aangegeven. Doorgaans zijn er afbeeldingen van 2 pagina&#39;s per paginaweergave, maar u kunt er meer of minder van hebben.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Asset handle in de image set member array. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3">Hiermee wordt de pagina opnieuw ingesteld. <p>Instelling wordt genegeerd en waarde wordt geforceerd op true voor <span class="codeph"> ImageSet</span> en <span class="codeph"> SpinSet</span>. </p></td> 
  </tr> 
 </tbody> 
</table>
