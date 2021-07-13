---
description: In de viewer worden pictogrammen voor favorieten weergegeven in de hoofdweergave op plaatsen waar deze oorspronkelijk door de gebruiker zijn toegevoegd.
solution: Experience Manager
title: Favorieten, effect
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 7603c873-a2d1-4a24-85a6-8e56a1f207de
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Favorieten, effect{#favorites-effect}

In de viewer worden pictogrammen voor favorieten weergegeven in de hoofdweergave op plaatsen waar deze oorspronkelijk door de gebruiker zijn toegevoegd.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De vormgeving van het pictogram Favoriet wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon
```

**CSS-eigenschappen van het pictogram Favoriet**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p> De afbeelding die voor het pictogram wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van het pictogram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van het pictogram. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - stel een pictogram Favorieten van 36 x 36 pixels in.

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

Op desktopsystemen ondersteunt de component de `cursortype`-kenmerkkiezer die u kunt toepassen op de klasse `.s7favoriteseffect` en bepaalt het type cursor op basis van de geselecteerde gebruikershandeling. De volgende `cursortype` waarden worden ondersteund:

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add  </span> </p> </td> 
   <td colname="col2"> <p>Weergegeven gebruiker voegt een nieuw pictogram Favoriet toe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove  </span> </p> </td> 
   <td colname="col2"> <p>Weergegeven gebruiker verwijdert een bestaand pictogram Favoriet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_view  </span> </p> </td> 
   <td colname="col2"> <p>Wordt weergegeven in de normale bewerkingsmodus wanneer Favorieten bewerken niet actief is. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld: gebruik verschillende muiscursors voor elk type componentstatus.

```
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_add"] { 
cursor: crosshair; 
} 
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_remove"] { 
cursor: not-allowed; 
} 
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_view"] { 
cursor: auto; 
}
```
