---
title: Hoofdviewergebied
description: Het hoofdweergavegebied is het gebied dat wordt ingenomen door de catalogusafbeelding. Deze wordt meestal ingesteld op het beschikbare apparaatscherm wanneer geen grootte is opgegeven.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 854f5fa7-f46d-4c4f-9a44-886fec93f606
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# Hoofdviewergebied{#main-viewer-area}

Het hoofdweergavegebied is het gebied dat wordt ingenomen door de catalogusafbeelding. Deze wordt meestal ingesteld op het beschikbare apparaatscherm wanneer geen grootte is opgegeven.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van het weergavegebied wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer
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

Voorbeeld - Een viewer instellen met een witte achtergrond ( `#FFFFFF`) en maakt het formaat 512 x 288 pixels.

```
.s7ecatalogsearchviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
