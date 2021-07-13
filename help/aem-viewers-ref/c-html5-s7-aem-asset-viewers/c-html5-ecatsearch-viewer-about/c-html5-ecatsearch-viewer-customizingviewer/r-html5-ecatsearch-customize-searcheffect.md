---
description: In de viewer worden gebieden met zoekresultaten in de hoofdweergave weergegeven om woorden of woordgroepen in de catalogus te markeren.
solution: Experience Manager
title: Zoeken, effect
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 3591edb0-4b0a-4761-af87-c372132c5138
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# Zoeken, effect{#search-effect}

In de viewer worden gebieden met zoekresultaten in de hoofdweergave weergegeven om woorden of woordgroepen in de catalogus te markeren.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van gebieden met zoekresultaten wordt bepaald door de volgende CSS-klassenkiezer:

`.s7ecatalogsearchviewer .s7searcheffect .s7region`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background  </span> </p> </td> 
   <td colname="col2"> <p>Achtergrond van gebied met zoekresultaten. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - voor het instellen van gebieden met zoekresultaten met een halftransparante, gele vulling:

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```
