---
description: JavaScript API-referentie voor Video Viewer.
solution: Experience Manager
title: VideoViewer
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 1%

---


# VideoViewer{#videoviewer}

JavaScript API-referentie voor Video Viewer.

`VideoViewer([config])`

Constructor; Hiermee wordt een nieuwe instantie Video Viewer gemaakt.

## Parameters {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}  </span> optioneel JSON-configuratieobject. Hiermee kunnen alle viewerinstellingen worden doorgegeven aan de constructor en wordt het aanroepen van afzonderlijke settermethoden vermeden. Bevat de volgende eigenschappen: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}- </span> id van de DOM-container (normaal gesproken een  <span class="codeph"> DIV  </span>) waarin de viewer wordt ingevoegd. Het is niet nodig om het containerelement te hebben dat tegen de tijd wordt gecreeerd deze methode wordt geroepen. De container moet echter bestaan wanneer <span class="codeph"> init() </span> wordt uitgevoerd. Vereist. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params  </span> -  <span class="codeph"> {Object}  </span> JSON-object met viewerconfiguratieparameters waarbij de eigenschapnaam een viewer-specifieke configuratieoptie of een SDK-optie is en de waarde van die eigenschap een overeenkomende instellingenwaarde is. Vereist. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> handlers  </span> -  <span class="codeph"> {Object}  </span> JSON-object met callbacks voor viewergebeurtenissen, waarbij de naam van de eigenschap de naam van de ondersteunde viewergebeurtenis is en de waarde van de eigenschap een JavaScript-functieverwijzing naar een geschikte callback is. Optioneel. <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local"> Gebeurteniscallbacks </a> voor meer informatie over viewergebeurtenissen. </p> </li> 
      <li id="li_D344288C9B584E569F7BF92D960F9DF8"> <p> <span class="codeph"> gelokaliseerdText  </span> - { <span class="codeph"> Object  </span>} JSON-object met lokalisatiegegevens. Optioneel. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local"> De naamruimte </a> van de SDK van de viewer voor meer informatie. </p> <p>Zie de <i>Gebruikershandleiding voor de SDK van de viewer</i> en het voorbeeld voor meer informatie over de inhoud van het object. Optioneel. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```

