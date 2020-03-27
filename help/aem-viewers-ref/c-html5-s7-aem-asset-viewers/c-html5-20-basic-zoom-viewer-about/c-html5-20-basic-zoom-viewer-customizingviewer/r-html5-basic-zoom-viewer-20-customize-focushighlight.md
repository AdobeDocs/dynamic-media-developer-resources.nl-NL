---
description: Focusmarkering voor invoer die wordt weergegeven rond het interface-element voor geconcentreerd viewergebruik wordt beheerd met de CSS-klassenkiezer.
seo-description: Focusmarkering voor invoer die wordt weergegeven rond het interface-element voor geconcentreerd viewergebruik wordt beheerd met de CSS-klassenkiezer.
seo-title: Focus markeren
solution: Experience Manager
title: Focus markeren
topic: Dynamic media
uuid: 1b552aec-837a-4df4-91dc-615ceead92b3
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Focus markeren{#focus-highlight}

Focusmarkering voor invoer die wordt weergegeven rond het interface-element voor geconcentreerd viewergebruik wordt beheerd met de CSS-klassenkiezer.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De vormgeving wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7basiczoomviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> overzicht </span> </p> </td> 
   <td colname="col2"> <p>Focus markeerstijl. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u de standaardfocusmarkering voor de browser wilt uitschakelen voor alle gebruikersinterface-elementen van de viewer, voegt u de volgende CSS-kiezer toe aan de stijlpagina van de viewer:

```
.s7basiczoomviewer *:focus { 
 outline: none; 
}
```

