---
description: In de viewer worden hotspots weergegeven op de hoofdweergave op plaatsen waar hotspots oorspronkelijk in Dynamic Media of AEM Assets waren ontworpen, op aanvraag.
seo-description: In de viewer worden hotspots weergegeven op de hoofdweergave op plaatsen waar hotspots oorspronkelijk in Dynamic Media of AEM Assets waren ontworpen, op aanvraag.
seo-title: Hotspots
solution: Experience Manager
title: Hotspots
topic: Dynamic media
uuid: 79c4d128-e24a-43b0-8e18-13b588eb396e
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Hotspots{#hotspots}

In de viewer worden hotspots weergegeven op de hoofdweergave op plaatsen waar hotspots oorspronkelijk in Dynamic Media of AEM Assets waren ontworpen, op aanvraag.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De weergave van het hotspot-pictogram wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7interactiveimage .s7imagemapeffect .s7icon
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
   <td colname="col2"> <p>Hotspot-pictogramafbeeldingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p>Plaats binnen de illustratie-sprite als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van hotspot-pictogram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van hotspot-pictogram. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - stel een hotspot-pictogram in van 56 x 56 pixels waarmee een andere afbeelding wordt weergegeven voor elk van de twee verschillende pictogramstatussen:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
 width: 56px; 
 height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

