---
description: De zoomindicator wordt bedekt op het hoofdweergavegebied. De afbeelding wordt weergegeven wanneer de voorinstelling van de afbeelding is ingeschakeld en is ook afhankelijk van de parameter iconeffect.
seo-description: De zoomindicator wordt bedekt op het hoofdweergavegebied. De afbeelding wordt weergegeven wanneer de voorinstelling van de afbeelding is ingeschakeld en is ook afhankelijk van de parameter iconeffect.
seo-title: Pictogram, effect
solution: Experience Manager
title: Pictogram, effect
topic: Dynamic media
uuid: 4995ac11-f591-4d1d-a292-be5d55aebf98
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Pictogram, effect{#icon-effect}

De zoomindicator wordt bedekt op het hoofdweergavegebied. De afbeelding wordt weergegeven wanneer de voorinstelling van de afbeelding is ingeschakeld en is ook afhankelijk van de parameter iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van het weergavegebied wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7pageview .s7iconeffect
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
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p> Illustraties van zoomindicatoren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van zoomindicator in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van zoomindicator in pixels. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Het effect Icon ondersteunt de `media-type` kenmerkenkiezer, die u kunt gebruiken om verschillende pictogrameffecten toe te passen op verschillende apparaten. Dit komt met name `media-type='standard'` overeen met desktopsystemen waarbij de muisinvoer normaal wordt gebruikt en `media-type='multitouch'` overeenkomt met apparaten met aanraakinvoer.

Voorbeeld: een zoomindicator van 100 x 100 pixels instellen met verschillende illustraties voor desktopsystemen en aanraakapparaten.

```
.s7ecatalogsearchviewer .s7pageview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7ecatalogsearchviewer .s7pageview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7ecatalogsearchviewer .s7pageview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```

