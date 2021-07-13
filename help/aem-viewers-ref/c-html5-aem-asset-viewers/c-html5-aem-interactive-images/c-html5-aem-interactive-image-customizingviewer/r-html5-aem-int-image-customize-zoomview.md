---
description: De hoofdweergave bestaat uit de statische afbeelding.
solution: Experience Manager
title: Zoomweergave
feature: Dynamic Media Classic,Viewers,SDK/API,Interactieve afbeeldingen
role: Developer,User
exl-id: e83d53a1-bee9-4e4d-8295-a3a350f3ff9c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---

# Zoomweergave{#zoom-view}

De hoofdweergave bestaat uit de statische afbeelding.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van het weergavegebied wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7interactiveimage .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Achtergrondkleur in hexadecimale notatie van de hoofdweergave. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - om de hoofdweergave transparant te maken.

```
.s7interactiveimage .s7zoomview { 
 background-color: transparent; 
}
```
