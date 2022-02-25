---
title: Focus markeren
description: Focusmarkering voor invoer die wordt weergegeven rond het interface-element voor geconcentreerd viewergebruik wordt beheerd met de CSS-klassenkiezer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 74ff9669-d56b-4731-9d4a-dda7c831e162
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

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
