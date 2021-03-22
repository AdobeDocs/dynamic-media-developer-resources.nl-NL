---
description: De hoofdweergave bestaat uit de draaiafbeelding.
seo-description: De hoofdweergave bestaat uit de draaiafbeelding.
seo-title: Weergave draaien
solution: Experience Manager
title: Weergave draaien
uuid: 74f42373-b08c-43c8-8f08-e61a09655b61
feature: Dynamic Media Classic,Viewers,SDK/API,Draaiensets
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---


# Weergave draaien{#spin-view}

De hoofdweergave bestaat uit de draaiafbeelding.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van het weergavegebied wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7spinviewer .s7spinview
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
.s7spinviewer .s7spinview { 
 background-color: transparent; 
}
```

