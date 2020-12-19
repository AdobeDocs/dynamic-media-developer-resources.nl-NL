---
description: Het gereedschap Twitter delen bestaat uit een knop die is toegevoegd aan het deelvenster Sociaal delen. Wanneer op de knop wordt geklikt, wordt de gebruiker omgeleid naar een dialoogvenster voor delen dat door een sociale service wordt aangeboden. De positie van de knop wordt volledig beheerd met het gereedschap Sociaal delen.
seo-description: Het gereedschap Twitter delen bestaat uit een knop die is toegevoegd aan het deelvenster Sociaal delen. Wanneer op de knop wordt geklikt, wordt de gebruiker omgeleid naar een dialoogvenster voor delen dat door een sociale service wordt aangeboden. De positie van de knop wordt volledig beheerd met het gereedschap Sociaal delen.
seo-title: Twitter delen
solution: Experience Manager
title: Twitter delen
topic: Dynamic media
uuid: 15fed20e-89c4-4c4b-8f0d-1f0bac0c0af7
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---


# Twitter delen{#twitter-share}

Het gereedschap Twitter delen bestaat uit een knop die is toegevoegd aan het deelvenster Sociaal delen. Wanneer op de knop wordt geklikt, wordt de gebruiker omgeleid naar een dialoogvenster voor delen dat door een sociale service wordt aangeboden. De positie van de knop wordt volledig beheerd met het gereedschap Sociaal delen.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

De weergave van de knop Delen via Twitter wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7videoviewer .s7twittershare
```

**CSS-eigenschappen van het gereedschap Twitter delen**

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

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) voor meer informatie.

Voorbeeld - voor het instellen van een gedeelde Twitter-knop van 28 x 28 pixels en het weergeven van een andere afbeelding voor elk van de vier verschillende knopstatussen:

```
.s7videoviewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7videoviewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7videoviewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7videoviewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```

