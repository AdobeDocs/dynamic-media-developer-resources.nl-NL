---
description: De centrifugeindicator wordt bedekt op het hoofdweergavegebied. De afbeelding wordt weergegeven wanneer de voorinstelling van de afbeelding is ingeschakeld en is ook afhankelijk van de parameter iconeffect.
seo-description: De centrifugeindicator wordt bedekt op het hoofdweergavegebied. De afbeelding wordt weergegeven wanneer de voorinstelling van de afbeelding is ingeschakeld en is ook afhankelijk van de parameter iconeffect.
seo-title: Pictogram, effect
solution: Experience Manager
title: Pictogram, effect
topic: Dynamic media
uuid: ce0524e4-fff4-45b0-8069-d5876802d66f
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---


# Pictogrameffect{#icon-effect}

De centrifugeindicator wordt bedekt op het hoofdweergavegebied. De afbeelding wordt weergegeven wanneer de voorinstelling van de afbeelding is ingeschakeld en is ook afhankelijk van de parameter iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van het weergavegebied wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7spinviewer .s7spinview .s7iconeffect
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
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p> Illustratie van de centrifuge-indicator. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#section-b671c70acf284cb0aea678c2d2e4babc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de centrifugeindicator. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de centrifuge. </p> </td> 
  </tr> 
 </tbody> 
</table>

De centrifugeindicator ondersteunt de `state`-kenmerkkiezer die is ingesteld op `spin_1D` in het geval van een eendimensionale centrifugeermodule en op `spin_2D` in het geval van een multidimensionale centrifugeerset.

Voorbeeld - voor het instellen van een zoomindicator van 100 x 100 pixels.

```
.s7spinviewer .s7spinview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7spinviewer .s7spinview .s7iconeffect[state="spin_1D"] { 
background-image: url(images/spinIcon_1D.png); 
} 
.s7spinviewer .s7spinview .s7iconeffect[state="spin_2D"] { 
background-image: url(images/spinIcon_2D.png); 
}
```

