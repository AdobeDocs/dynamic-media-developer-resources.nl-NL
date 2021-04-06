---
description: Focusmarkering voor invoer die wordt weergegeven rond het interface-element van de viewer die focus heeft, wordt beheerd met de CSS-klassenkiezer.
solution: Experience Manager
title: Focus markeren
feature: Dynamic Media Classic,Viewers,SDK/API,Interactieve video's
role: Ontwikkelaar,zakelijke praktiserer
exl-id: cb5231ed-106a-444f-aac7-06dd1a84a665
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Focus markeren{#focus-highlight}

Focusmarkering voor invoer die wordt weergegeven rond het interface-element van de viewer die focus heeft, wordt beheerd met de CSS-klassenkiezer.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen**

De vormgeving wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7interactivevideoviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> overzicht  </span> </p> </td> 
   <td colname="col2"> <p>Focus markeerstijl. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u de standaardfocusmarkering voor de browser wilt uitschakelen voor alle gebruikersinterface-elementen van de viewer, voegt u de volgende CSS-kiezer toe aan de stijlpagina van de viewer:

```
.s7interactivevideoviewer *:focus { 
 outline: none; 
}
```
