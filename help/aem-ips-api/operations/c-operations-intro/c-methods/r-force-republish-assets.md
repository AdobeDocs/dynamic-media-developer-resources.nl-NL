---
description: Hiermee herstelt u de publicatiestatus voor een of meer elementen zodat het element opnieuw moet worden gepubliceerd in de volgende publicatietaak.
seo-description: Hiermee herstelt u de publicatiestatus voor een of meer elementen zodat het element opnieuw moet worden gepubliceerd in de volgende publicatietaak.
seo-title: forceRepublishAssets
solution: Experience Manager
title: forceRepublishAssets
topic: Scene7 Image Production System API
uuid: fd1f4ece-075c-40e3-868a-f27b9a4c3374
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# forceRepublishAssets{#forcerepublishassets}

Hiermee herstelt u de publicatiestatus voor een of meer elementen zodat het element opnieuw moet worden gepubliceerd in de volgende publicatietaak.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-3d5a3e3afea748d69845de5c8c376448}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-fd3f4dde9e984240b6f3e6d7a8db4e78}

**Input (forceRepublishAssetsParam)**

<table id="table_742D67AD77554904976EC4A07A0CBC64"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> bedrijfshandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Handle aan het bedrijf dat activa bevat om terug te stellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> republishFiles</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>Hiermee geeft u aan dat de bestanden voor het element opnieuw worden gepubliceerd naar de leveringsservers. De standaardwaarde is <span class="codeph"> true</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> resyncCatalog</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>Hiermee geeft u aan dat de metagegevens van de catalogus die worden gebruikt om het element te leveren, worden gesynchroniseerd om te garanderen dat het element actueel is. Deze parameter wordt gebruikt om rasvoorwaarden op te lossen die op dichtbijgelegen gezamenlijke updates aan het zelfde verslag zouden kunnen voorkomen. De standaardwaarde is <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Array van handgrepen voor elementen waarvan de publicatiestatus moet worden hersteld. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (forceRepublishAssetsParam)**

<table id="table_78E74186669F477E9E2D837D58A789DC"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishStateUpdateArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:PublishStateUpdateArray</span> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Array met updates van publicatiestatus. </p> </td> 
  </tr> 
 </tbody> 
</table>

