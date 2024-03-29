---
description: Taaktype om geoorloofde export van eerder geüploade bestanden toe te staan.
solution: Experience Manager
title: ExportJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f0266b9f-c6e0-4843-b002-0bc068d43424
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---

# [!DNL ExportJob]{#exportjob}

Taaktype om geoorloofde export van eerder geüploade bestanden toe te staan.

De volgende elementtypen worden niet door ExportJob ondersteund:

* Afbeeldingssets
* Rendersets
* Sets draaien
* Mediasets
* Sets met meerdere bitsnelheden
* Videosets
* eCatalogs
* Aanbiedingssets

<table id="table_D8F3FD30D15648BFA5B980D3DC0A5AB1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Naam </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL assetHandleArray]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>Lijst van <span class="codeph"> assetHandle</span> die moeten worden geëxporteerd. Zie <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> HandleArray</a>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL fmt]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:tekenreeks </span> </p> </td> 
   <td colname="col3"> <p>Geeft het type van <span class="codeph"> export.Mogelijke waarden</span>: [orig, converteren] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">Indien <span class="codeph"> fmt=orig</span>, worden de elementen geëxporteerd als origineel </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">Indien <span class="codeph"> fmt=convert</span>, worden de elementen geconverteerd naar de indeling die is opgegeven in de <span class="codeph"> is_modifer</span> of <span class="codeph"> macro</span> invoerparameters </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL is_modifier]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:tekenreeks </span> </p> </td> 
   <td colname="col3"> <p>Hiermee geeft u de <span class="codeph"> ImageServer</span> het teruggeven van koord URL, dat aan ExportJob wordt toegevoegd <span class="codeph"> omzetten</span> verzoek. </p> <p>Zie de <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/homeisir.html" scope="external" format="html"> IS-documentatie</a> voor details over het verzenden van de IS bepalingen. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL macro]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:tekenreeks </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL emailSetting]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:tekenreeks </span> </p> </td> 
   <td colname="col3"> <p>Keuze van e-mailinstelling. Mogelijke waarden: </p> <p> 
     <ul id="ul_0EEDAE11B7CD4C53A6E4B2B8CB2CF730"> 
      <li id="li_F235F93828594ED78C6D464440F953FF"> <span class="codeph"> Alles</span> </li> 
      <li id="li_59E14E7EBFA64432A5FAC15DA21A0521"> <span class="codeph"> Fout</span> </li> 
      <li id="li_BFE0B52CADD14CC1BA1AF42AB0AA1CE1"> <span class="codeph"> ErrorAndWarning</span> </li> 
      <li id="li_BE3AA67E14FB487B8B9CD6EF3D58824C"> <span class="codeph"> JobCompletion</span> </li> 
      <li id="li_409C68AD0D244975BFB86B08609E0146"> <span class="codeph"> Geen</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL clientId]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:tekenreeks </span> </p> </td> 
   <td colname="col3"> <p>Specificeert het IP adres van de cliënt of de klant die het uitvoerverzoek in werking stelde. </p> <p> <p>Opmerking: deze parameter is momenteel niet actief ingevuld en is uitsluitend gereserveerd voor toekomstig gebruik. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

Voor ExportJob-aanvragen waarbij `fmt=convert` en beide `is_modifier` en `macro` het doelbestand voldoet aan de indeling van `macro`. Bijvoorbeeld:

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```
