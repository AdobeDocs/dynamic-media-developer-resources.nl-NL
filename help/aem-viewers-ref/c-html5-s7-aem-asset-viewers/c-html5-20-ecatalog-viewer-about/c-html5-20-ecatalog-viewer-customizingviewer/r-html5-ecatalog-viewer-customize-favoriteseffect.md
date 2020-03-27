---
description: In de viewer worden pictogrammen voor favorieten weergegeven in de hoofdweergave op plaatsen waar deze oorspronkelijk door de gebruiker zijn toegevoegd.
seo-description: In de viewer worden pictogrammen voor favorieten weergegeven in de hoofdweergave op plaatsen waar deze oorspronkelijk door de gebruiker zijn toegevoegd.
seo-title: Favorieten, effect
solution: Experience Manager
title: Favorieten, effect
topic: Dynamic media
uuid: b660b9fd-592b-4072-83c9-f70330ee19ab
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Favorieten, effect{#favorites-effect}

In de viewer worden pictogrammen voor favorieten weergegeven in de hoofdweergave op plaatsen waar deze oorspronkelijk door de gebruiker zijn toegevoegd.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De vormgeving van het pictogram Favoriet wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogviewer .s7favoriteseffect .s7icon
```

**CSS-eigenschappen van het pictogram Favoriet**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p> De afbeelding die voor het pictogram wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van het pictogram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van het pictogram. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - stel een pictogram Favorieten van 36 x 36 pixels in.

```
.s7ecatalogviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

Op desktopsystemen ondersteunt de component de `cursortype` kenmerkkiezer die u op de `.s7favoriteseffect` klasse kunt toepassen en het type cursor op basis van de geselecteerde gebruikersactie. De volgende `cursortype` waarden worden ondersteund:

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add </span> </p> </td> 
   <td colname="col2"> <p>Weergegeven gebruiker voegt een nieuw pictogram Favoriet toe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove </span> </p> </td> 
   <td colname="col2"> <p>Weergegeven gebruiker verwijdert een bestaand pictogram Favoriet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_view </span> </p> </td> 
   <td colname="col2"> <p>Wordt weergegeven in de normale bewerkingsmodus wanneer Favorieten bewerken niet actief is. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld: gebruik verschillende muiscursors voor elk type componentstatus.

```
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_add"] { 
cursor: crosshair; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_remove"] { 
cursor: not-allowed; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_view"] { 
cursor: auto; 
}
```

