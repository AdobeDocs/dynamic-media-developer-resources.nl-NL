---
description: De hoofdweergave bestaat uit de bannerafbeelding.
seo-description: De hoofdweergave bestaat uit de bannerafbeelding.
seo-title: Carousel-weergave
solution: Experience Manager
title: Carousel-weergave
uuid: bf2065cc-fef2-4d4e-ab2a-a533fa063a80
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---


# Carrouselweergave{#carousel-view}

De hoofdweergave bestaat uit de bannerafbeelding.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van het weergavegebied wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7carouselviewer .s7carouselview
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
.s7carouselviewer .s7carouselview { 
 background-color: transparent; 
}
```

