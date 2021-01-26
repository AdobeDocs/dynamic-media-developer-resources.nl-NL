---
description: Afbeelding opslaan naar bestand.
seo-description: Afbeelding opslaan naar bestand.
seo-title: saveToFile
solution: Experience Manager
title: saveToFile
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 32a56d77-89e2-4f78-9fab-1b528e9a024a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# saveToFile{#savetofile}

Afbeelding opslaan naar bestand.

`req=saveToFile&name= *``*[&timeout= *`fileval`*]`

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
   <td> <p> <span class="codeph"> </span> Doneif successfully. </p> </td> 
  </tr> 
 </tbody> 
</table>

Retourneert HTTP-antwoordstatus 200 als de bewerking succesvol was en 403 als de aanvraag mislukt of de tijd uit is. De reactie heeft MIME type `text/plain` en is niet cacheable.

Belangrijk het Opslaan aan dossiers moet worden toegelaten door de weg aan een bestaande schrijfbare omslag in `attribute::SavePath` te specificeren. `saveToFile=` mislukt als  `attribute::SavePath` het leeg is.

*`file`* is vereist en moet een relatief pad zijn dat wordt gecombineerd met  `attribute::SavePath`. Er worden geen mappen gemaakt met Beeldserver. De doelmap moet op de server aanwezig zijn en de juiste machtigingsinstellingen voor Image Serving hebben om bestanden te maken.

`timeout=` is optioneel. De standaardonderbreking is 60.000 msec, of welke waarde met `PS::SaveTimeout` wordt gevormd.
