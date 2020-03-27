---
description: Het afspeelpictogram wordt bedekt door het weergavegebied van de video. Deze wordt weergegeven wanneer de video wordt gepauzeerd of wanneer het einde van de video is bereikt. Deze parameter is ook afhankelijk van de parameter iconeffect.
seo-description: Het afspeelpictogram wordt bedekt door het weergavegebied van de video. Deze wordt weergegeven wanneer de video wordt gepauzeerd of wanneer het einde van de video is bereikt. Deze parameter is ook afhankelijk van de parameter iconeffect.
seo-title: Pictogram van videospeler, effect
solution: Experience Manager
title: Pictogram van videospeler, effect
topic: Dynamic media
uuid: 5d59c4b2-a7a1-49e1-84c7-0e127a571c4f
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Pictogram van videospeler, effect{#video-player-icon-effect}

Het afspeelpictogram wordt bedekt door het weergavegebied van de video. Deze wordt weergegeven wanneer de video wordt gepauzeerd of wanneer het einde van de video is bereikt. Deze parameter is ook afhankelijk van de parameter iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De weergave van het afspeelpictogram wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

**CSS-eigenschappen van het afspeelpictogram**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p> De weergegeven afbeelding voor het afspeelpictogram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> De breedte van het afspeelpictogram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>De hoogte van het afspeelpictogram. </p> </td> 
  </tr> 
 </tbody> 
</table>

Het effect Icon ondersteunt de `state` kenmerkkiezer. `state="play"` wordt gebruikt wanneer de video wordt gepauzeerd in het midden van het afspelen en `state="replay"` wordt gebruikt wanneer de afspeelkop zich aan het einde van de stream bevindt.

## Voorbeeld {#section-e8caea0a303c425a8a637c2a47c06355}

Stel een afspeelpictogram van 100 x 100 pixels in.

```
.s7mixedmediaviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```

