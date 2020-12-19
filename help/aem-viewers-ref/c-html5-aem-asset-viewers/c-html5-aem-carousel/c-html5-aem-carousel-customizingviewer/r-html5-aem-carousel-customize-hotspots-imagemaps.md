---
description: In de viewer worden hotspots weergegeven op de hoofdweergave op plaatsen waar hotspots oorspronkelijk in Dynamic Media of AEM Assets waren ontworpen, op aanvraag.
seo-description: In de viewer worden hotspots weergegeven op de hoofdweergave op plaatsen waar hotspots oorspronkelijk in Dynamic Media of AEM Assets waren ontworpen, op aanvraag.
seo-title: Hotspots en afbeeldingen met hyperlinks
solution: Experience Manager
title: Hotspots en afbeeldingen met hyperlinks
topic: Dynamic media
uuid: de7f4dc7-1a55-49d5-a712-7f178cc49068
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---


# Hotspots en afbeeldingen met hyperlinks{#hotspots-and-image-maps}

In de viewer worden hotspots weergegeven op de hoofdweergave op plaatsen waar hotspots oorspronkelijk in Dynamic Media of AEM Assets waren ontworpen, op aanvraag.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De weergave van het hotspot-pictogram wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7carouselviewer .s7imagemapeffect .s7icon
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

<!--<a id="section_26D0B8444D1F42D493793FF54968C0B9"></a>-->

**CSS-eigenschappen van het afbeeldingskaartgebied**

De vormgeving van het gebied met afbeeldingskaart wordt bepaald door de volgende CSS-klassenkiezer:

`.s7carouselviewer .s7imagemapeffect .s7region`

<table id="table_DAE7A78AA4A74DC78B2D94F29E8E236B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background  </span> </p> </td> 
   <td colname="col2"> <p>Vulkleur van gebied Afbeeldingskaart. </p> <p>Geef deze kleur op in <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> of <span class="codeph"> RGBA(R,G,B,A) </span>-indelingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Vulkleur van gebied Afbeeldingskaart. </p> <p>Geef deze kleur op in <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> of <span class="codeph"> RGBA(R,G,B,A) </span>-indelingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p> Randstijl van afbeeldingskaart. Moet worden opgegeven als " <span class="codeph"> width </span> <span class="codeph"> solid color </span>", waarbij <span class="codeph"> width </span> wordt uitgedrukt in pixels, en <span class="codeph"> color </span> wordt ingesteld als <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) &lt;a1 1/&gt;, of <span class="codeph"> RGBA(R,G,B,A) </span>.</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld: een transparant gebied voor een afbeelding met hyperlinks instellen met een zwarte rand van één pixel:

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

