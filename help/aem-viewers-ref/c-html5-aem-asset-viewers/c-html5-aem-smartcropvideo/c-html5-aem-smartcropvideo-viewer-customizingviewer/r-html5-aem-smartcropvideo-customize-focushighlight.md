---
description: Invoerfocusmarkering die wordt weergegeven rond het interface-element met focus, wordt beheerd met de CSS-klassenkiezer.
solution: Experience Manager
title: Focus markeren
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 9968c67b-02cc-4ac0-8ab1-c7eda565912d
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# Focus markeren{#focus-highlight}

Invoerfocusmarkering die wordt weergegeven rond het interface-element met focus, wordt beheerd met de CSS-klassenkiezer.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen**

De vormgeving wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7smartcropvideoviewer *:focus
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
.s7smartcropvideoviewer *:focus { 
 outline: none; 
}
```
