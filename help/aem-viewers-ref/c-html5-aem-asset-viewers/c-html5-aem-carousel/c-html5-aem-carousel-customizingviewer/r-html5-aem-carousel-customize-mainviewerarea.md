---
description: Het hoofdweergavegebied is het gebied dat wordt ingenomen door de afbeelding van de carrouselbanner. Deze wordt meestal ingesteld op weergave op het beschikbare apparaatscherm wanneer geen grootte is opgegeven.
seo-description: Het hoofdweergavegebied is het gebied dat wordt ingenomen door de afbeelding van de carrouselbanner. Deze wordt meestal ingesteld op weergave op het beschikbare apparaatscherm wanneer geen grootte is opgegeven.
seo-title: Hoofdviewergebied
solution: Experience Manager
title: Hoofdviewergebied
topic: Dynamic media
uuid: 0e796f75-36a6-4961-9980-b634ab50c7ff
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Hoofdviewergebied{#main-viewer-area}

Het hoofdweergavegebied is het gebied dat wordt ingenomen door de afbeelding van de carrouselbanner. Deze wordt meestal ingesteld op weergave op het beschikbare apparaatscherm wanneer geen grootte is opgegeven.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van het weergavegebied wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7carouselviewer
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>De breedte van de viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>De hoogte van de viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Achtergrondkleur in hexadecimale notatie. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - een viewer instellen met een witte achtergrond ( `#FFFFFF`) en de grootte instellen op 1174 x 500 pixels.

```
.s7carouselviewer { 
 background-color: #FFFFFF; 
 width: 1174px; 
 height: 500px;  
}
```

