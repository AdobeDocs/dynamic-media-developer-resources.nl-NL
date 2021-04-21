---
description: Invoerfocusmarkering die wordt weergegeven rond het interface-element met focus, wordt beheerd met de CSS-klassenkiezer.
solution: Experience Manager
title: Focus markeren
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---


# Focus markeren{#focus-highlight}

Invoerfocusmarkering die wordt weergegeven rond het interface-element met focus, wordt beheerd met de CSS-klassenkiezer.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen**

De vormgeving wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7spinviewer *:focus
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
.s7spinviewer *:focus { 
 outline: none; 
}
```

