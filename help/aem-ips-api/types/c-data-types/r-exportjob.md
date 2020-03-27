---
description: Taaktype om geoorloofde export van eerder geüploade bestanden toe te staan.
seo-description: Taaktype om geoorloofde export van eerder geüploade bestanden toe te staan.
seo-title: ExportJob
solution: Experience Manager
title: ExportJob
topic: Scene7 Image Production System API
uuid: 439e3dd8-85b8-4f5b-abf8-8cc5a3f59fe6
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ExportJob{#exportjob}

Taaktype om geoorloofde export van eerder geüploade bestanden toe te staan.

De volgende elementtypen worden niet door ExportJob ondersteund:

* Afbeeldingsets
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
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>Lijst met <span class="codeph"> elementen die</span> moeten worden geëxporteerd. Zie <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> HandleArray</a>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fmt</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:tekenreeks </span> </p> </td> 
   <td colname="col3"> <p>Hiermee geeft u het type <span class="codeph"> export op. Mogelijke waarden</span>: [orig, converteren] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">Als <span class="codeph"> fmt=orig</span>, worden de activa uitgevoerd als origineel </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">Als <span class="codeph"> fmt=convert</span>, worden de activa omgezet in het formaat dat in de parameters van de <span class="codeph"> is_modifer</span> of van de <span class="codeph"> macro</span> input wordt gespecificeerd </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> is_modifier</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:tekenreeks </span> </p> </td> 
   <td colname="col3"> <p>Geeft de URL-tekenreeks op voor het renderen van <span class="codeph"> ImageServer</span> , die wordt toegevoegd aan de aanvraag voor <span class="codeph"> conversie</span> van ExportJob. </p> <p>Verwijs naar de documentatie <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/" scope="external" format="html"> van</a> IS voor details over het verzenden van de opties van IS. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> macro</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:tekenreeks </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> E- <span class="varname"> mailinstelling</span></span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> clientId</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:tekenreeks </span> </p> </td> 
   <td colname="col3"> <p>Specificeert het IP adres van de cliënt of de klant die het uitvoerverzoek in werking stelde. </p> <p> <p>Opmerking:  deze parameter is momenteel niet actief ingevuld en is uitsluitend gereserveerd voor toekomstig gebruik. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

Voor verzoeken ExportJob waar `fmt=convert` en zowel `is_modifier` als `macro` worden verstrekt, eerbiedigt het bestemmingsdossier het formaat dat door wordt verstrekt `macro`. Bijvoorbeeld:

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```

