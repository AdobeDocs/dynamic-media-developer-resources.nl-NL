---
title: SmartCropVideoViewer
description: JavaScript API-referentie voor SmartCrop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 55885e57-4a21-43bb-86b0-9ac34bd29bd0
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# SmartCropVideoViewer{#smartcropvideoviewer}

JavaScript API-referentie voor SmartCrop Video Viewer.

`SmartCropVideoViewer([config])`

Constructor; Hiermee wordt een instantie van de SmartCrop Video-viewer gemaakt.

## Parameters {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> Met het optionele JSON-configuratieobject kunnen alle viewerinstellingen worden doorgegeven aan de constructor en wordt het aanroepen van afzonderlijke settermethoden vermeden. Bevat de volgende eigenschappen: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID van de DOM-container (gewoonlijk een <span class="codeph"> DIV </span>) waarin de viewer wordt ingevoegd. Het is niet nodig om het containerelement te hebben dat tegen de tijd wordt gecreeerd deze methode wordt geroepen. De container moet echter bestaan wanneer <span class="codeph"> init() </span> wordt uitgevoerd. Vereist. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> param </span> - <span class="codeph"> {Object} </span> JSON-object met configuratieparameters voor de viewer waarbij de naam van de eigenschap een viewer-specifieke configuratieoptie of een SDK-modifier is en de waarde van die eigenschap een corresponderende instellingswaarde is. Vereist. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> handlers </span> - <span class="codeph"> {Object} </span> JSON-object met callbacks voor viewergebeurtenissen, waarbij de naam van de eigenschap de naam van de ondersteunde viewergebeurtenis is en de waarde van de eigenschap een JavaScript-functieverwijzing naar een geschikte callback is. Optioneel. <p>Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local"> Gebeurteniscallbacks </a> voor meer informatie over viewergebeurtenissen. </p> </li> 
      <li id="li_D344288C9B584E569F7BF92D960F9DF8"> <p> <span class="codeph"> localizedText </span> - { <span class="codeph"> Object </span>} JSON-object met lokalisatiegegevens. Optioneel. </p> <p>Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local"> Viewer SDK-naamruimte </a> voor meer informatie . </p> <p>Zie de <i>Gebruikershandleiding van de viewer-SDK</i> en het voorbeeld voor meer informatie over de inhoud van het object. Optioneel. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
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
"SmartCropVideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"SmartCropVideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```
