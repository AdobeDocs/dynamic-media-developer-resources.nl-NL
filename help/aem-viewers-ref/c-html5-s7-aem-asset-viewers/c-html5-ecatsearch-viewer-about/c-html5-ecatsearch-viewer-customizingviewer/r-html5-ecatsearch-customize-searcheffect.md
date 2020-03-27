---
description: In de viewer worden gebieden met zoekresultaten in de hoofdweergave weergegeven om woorden of woordgroepen in de catalogus te markeren.
seo-description: In de viewer worden gebieden met zoekresultaten in de hoofdweergave weergegeven om woorden of woordgroepen in de catalogus te markeren.
seo-title: Zoeken, effect
solution: Experience Manager
title: Zoeken, effect
topic: Dynamic media
uuid: 3a076ff8-2da5-4020-8a77-8f5a256afefe
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

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
   <td colname="col1"> <p> <span class="codeph"> background </span> </p> </td> 
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

