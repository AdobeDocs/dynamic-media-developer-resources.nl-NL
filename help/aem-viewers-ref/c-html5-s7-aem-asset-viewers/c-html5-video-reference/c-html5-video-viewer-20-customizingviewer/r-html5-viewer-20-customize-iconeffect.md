---
description: Het afspeelpictogram wordt boven in het hoofdweergavegebied geplaatst. Deze wordt weergegeven wanneer de video wordt gepauzeerd of wanneer het einde van de video is bereikt. Deze parameter is ook afhankelijk van de parameter iconeffect.
solution: Experience Manager
title: Pictogram, effect
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: f4bf343a-4a78-470b-abe5-94e2d608f45d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# Pictogram, effect{#icon-effect}

Het afspeelpictogram wordt boven in het hoofdweergavegebied geplaatst. Deze wordt weergegeven wanneer de video wordt gepauzeerd of wanneer het einde van de video is bereikt. Deze parameter is ook afhankelijk van de parameter iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De weergave van het afspeelpictogram wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7videoviewer . s7videoplayer .s7iconeffect
```

**CSS-eigenschappen van het afspeelpictogram**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p> De weergegeven afbeelding voor het afspeelpictogram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> De breedte van het afspeelpictogram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>De hoogte van het afspeelpictogram. </p> </td> 
  </tr> 
 </tbody> 
</table>

Het effect van het pictogram steunt `state` attributenselecteur. `state="play"` wordt gebruikt wanneer de video wordt gepauzeerd in het midden van het afspelen en  `state="replay"` wordt gebruikt wanneer de afspeelkop zich aan het einde van de stream bevindt.

## Voorbeeld {#section-e8caea0a303c425a8a637c2a47c06355}

Stel een afspeelpictogram van 100 x 100 pixels in.

```
.s7videoviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7videoviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7videoviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
