---
description: 'Binnen dit type is het pageReset-veld relevant voor renderSet- en Catalog-afbeeldingselementtypen '
seo-description: 'Binnen dit type is het pageReset-veld relevant voor renderSet- en Catalog-afbeeldingselementtypen '
seo-title: ImageSetMemberUpdate
solution: Experience Manager
title: ImageSetMemberUpdate
topic: Scene7 Image Production System API
uuid: b0226d21-87ba-4e07-9819-79c9df3df13c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ImageSetMemberUpdate{#imagesetmemberupdate}

Binnen dit type is het pageReset-veld relevant voor de renderset- en catalogusafbeeldingselementtypen:

* Hiermee geeft u `RenderSet`bijvoorbeeld `pageReset` het begin van een nieuwe renderweergave/staalgroep aan.

* Voor Catalog, `pageReset` wijst op het begin van een nieuwe paginamening. Doorgaans zijn er afbeeldingen van 2 pagina&#39;s per paginaweergave, maar u kunt er meer of minder van hebben.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Asset handle in de image set member array. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pagina herstellen</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3">Hiermee wordt de pagina opnieuw ingesteld. <p>Instelling wordt genegeerd en waarde wordt geforceerd naar waar voor <span class="codeph"> Afbeeldingsset</span> en <span class="codeph"> SpinSet</span>. </p></td> 
  </tr> 
 </tbody> 
</table>

