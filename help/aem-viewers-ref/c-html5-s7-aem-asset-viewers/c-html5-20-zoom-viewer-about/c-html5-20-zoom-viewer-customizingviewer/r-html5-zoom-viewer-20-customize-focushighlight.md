---
description: Invoerfocusmarkering die wordt weergegeven rond het interface-element met focus, wordt beheerd met de CSS-klassenkiezer.
seo-description: Invoerfocusmarkering die wordt weergegeven rond het interface-element met focus, wordt beheerd met de CSS-klassenkiezer.
seo-title: Focus markeren
solution: Experience Manager
title: Focus markeren
uuid: 5ae9c445-4be2-467e-a268-9c56b7859d47
feature: Dynamic Media Classic,Viewers,SDK/API,Zoomen
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# Focus markeren{#focus-highlight}

Invoerfocusmarkering die wordt weergegeven rond het interface-element met focus, wordt beheerd met de CSS-klassenkiezer.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen**

De vormgeving wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7zoomviewer *:focus
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
.s7zoomviewer *:focus { 
 outline: none; 
}
```

