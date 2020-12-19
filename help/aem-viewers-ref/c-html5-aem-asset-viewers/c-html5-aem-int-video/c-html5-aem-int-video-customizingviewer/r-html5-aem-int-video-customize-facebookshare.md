---
description: Het Facebook-gereedschap Delen bestaat uit een knop die is toegevoegd aan het deelvenster Delen via sociale media. Wanneer op de knop wordt geklikt, wordt de gebruiker omgeleid naar een dialoogvenster voor delen dat door een sociale service wordt aangeboden. De positie van de knop wordt volledig beheerd met het gereedschap Sociaal delen.
seo-description: Het Facebook-gereedschap Delen bestaat uit een knop die is toegevoegd aan het deelvenster Delen via sociale media. Wanneer op de knop wordt geklikt, wordt de gebruiker omgeleid naar een dialoogvenster voor delen dat door een sociale service wordt aangeboden. De positie van de knop wordt volledig beheerd met het gereedschap Sociaal delen.
seo-title: Facebook-share
solution: Experience Manager
title: Facebook-share
topic: Dynamic media
uuid: 6f7e9700-19c2-441d-a0d0-5bc30a50b0e3
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---


# Facebook share{#facebook-share}

Het Facebook-gereedschap Delen bestaat uit een knop die is toegevoegd aan het deelvenster Delen via sociale media. Wanneer op de knop wordt geklikt, wordt de gebruiker omgeleid naar een dialoogvenster voor delen dat door een sociale service wordt aangeboden. De positie van de knop wordt volledig beheerd met het gereedschap Sociaal delen.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

De weergave van de Facebook-deelknop wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7interactivevideoviewer .s7facebookshare
```

**CSS-eigenschappen van het gereedschap Delen via Facebook**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Knopbreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p> De afbeelding die voor een bepaalde knopstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoop steunt `state` attributenselecteur, die kan worden gebruikt om verschillende huiden op verschillende knoopstaten toe te passen.

Het is mogelijk om de knop uit het deelvenster Sociaal delen te verwijderen door de CSS-eigenschap `display:none` in te stellen op de CSS-klasse.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Voorbeeld {#section-01cbe0096b1443e0a7d91956bd264465}

Als u een Facebook-deelknop van 28 x 28 pixels wilt instellen, wordt een andere afbeelding weergegeven voor elk van de vier verschillende knopstatussen:

```
.s7interactivevideoviewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7interactivevideoviewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7interactivevideoviewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7interactivevideoviewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7interactivevideoviewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```

