---
description: Afbeelding opslaan naar bestand.
solution: Experience Manager
title: saveToFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 10a8ea5c-7e64-4d99-a263-779f08ea6e37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# saveToFile{#savetofile}

Afbeelding opslaan naar bestand.

`req=saveToFile&name= *`file`*[&timeout= *`val`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> file</span> </p> </td> 
  <td class="stentry"> <p>Relatief pad naar doelafbeeldingsbestand. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Time-outinterval (milliseconden). </p></td> 
 </tr> 
</table>

Hiermee slaat u de reactieafbeelding op in een bestand op de server in plaats van deze naar de client te retourneren.

Wanneer de opslagaanvraag met succes is voltooid, retourneert de aanvraag verschillende eigenschappen in Java-indeling, waaronder de volgende:

<table id="table_8BA8F75A0B7241BAB9B4359F97C21137"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Eigenschap</b> </th> 
   <th class="entry"> <b> Type</b> </th> 
   <th class="entry"> <b> Beschrijving</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> lastUpdated</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>Aanmaaktijd van het bestand (aantal milliseconden sinds middernacht, 1 januari 1970 UTC/GMT ). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelsTotal</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Aantal pixels in opgeslagen afbeelding. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> status</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> gedaan</span> indien succesvol. </p> </td> 
  </tr> 
 </tbody> 
</table>

Retourneert HTTP-antwoordstatus 200 als de bewerking succesvol was en 403 als de aanvraag mislukt of de tijd uit is. Het antwoord heeft het MIME-type `text/plain` en is niet in cache te plaatsen.

Belangrijk opslaan naar bestanden moet zijn ingeschakeld door het pad naar een bestaande schrijfbare map op te geven in `attribute::SavePath`. `saveToFile=` mislukt als `attribute::SavePath` is leeg.

*`file`* is vereist en moet een relatief pad zijn dat wordt gecombineerd met `attribute::SavePath`. Er worden geen mappen gemaakt met Beeldserver. De doelmap moet op de server aanwezig zijn en de juiste machtigingsinstellingen voor Image Serving hebben om bestanden te maken.

`timeout=` is optioneel. De standaardonderbreking is 60.000 msec, of welke waarde wordt gevormd met `PS::SaveTimeout`.
