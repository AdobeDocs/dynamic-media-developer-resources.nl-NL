---
title: InteractiveVideoViewer
description: JavaScript API-referentie voor Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: efd0ffea-482c-4af4-ac77-ac1b7f326ce9
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# InteractiveVideoViewer{#interactivevideoviewer}

JavaScript API-referentie voor Interactive Video Viewer.

`InteractiveVideoViewer([config])`

Constructor: maakt een Interactive Video Viewer-instantie.

## Parameters {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> Met het optionele JSON-configuratieobject kunnen alle viewerinstellingen aan de constructor worden doorgegeven om te voorkomen dat afzonderlijke settermethoden worden aangeroepen. Bevat de volgende eigenschappen: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID van de DOM-container (gewoonlijk een <span class="codeph"> DIV </span>) waarin de viewer wordt ingevoegd. Tegen de tijd dat deze methode wordt geroepen, is het niet noodzakelijk om het containerelement te hebben gecreeerd. De container moet echter bestaan wanneer <span class="codeph"> init() </span> wordt uitgevoerd. </p> <p>Vereist. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> param </span> - <span class="codeph"> {Object} </span> JSON-object met parameters voor viewerconfiguratie waarbij de naam van de eigenschap viewer-specifieke configuratieoptie of SDK-modifier is en de waarde van die eigenschap een corresponderende instellingswaarde is. </p> <p>Vereist. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> handlers </span> - <span class="codeph"> {Object} </span> JSON-object met callbacks voor viewergebeurtenissen, waarbij de eigenschapsnaam de naam van de ondersteunde viewergebeurtenis is en de eigenschapswaarde een JavaScript-functieverwijzing naar de juiste callback is. </p> <p>Optioneel. </p> <p>Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Gebeurteniscallbacks </a> voor meer informatie over viewergebeurtenissen. </p> </li> 
      <li id="li_42A3F3BEF1004E069F0FB2AE0A30B093"> <p> <span class="codeph"> localizedText </span> - <span class="codeph"> {Object} </span> JSON-object met lokalisatiegegevens. Optioneel. </p> <p>Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Lokalisatie van gebruikersinterface-elementen </a> voor meer informatie . </p> <p>Zie ook de <i>Gebruikershandleiding van de viewer-SDK</i> en het voorbeeld voor meer informatie over de inhoud van het object. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
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
