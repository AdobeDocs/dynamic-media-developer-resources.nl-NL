---
title: Hoofdviewergebied
description: Het hoofdweergavegebied is het gebied dat wordt ingenomen door de zoomafbeelding. Deze wordt meestal ingesteld op het beschikbare apparaatscherm wanneer geen grootte is opgegeven.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f51de2d6-0de2-4a4d-bbf4-185547e6c550
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# Hoofdviewergebied{#main-viewer-area}

Het hoofdweergavegebied is het gebied dat wordt ingenomen door de zoomafbeelding. Deze wordt meestal ingesteld op het beschikbare apparaatscherm wanneer geen grootte is opgegeven.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van het weergavegebied wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7basiczoomviewer
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
.s7basiczoomviewer{ 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
