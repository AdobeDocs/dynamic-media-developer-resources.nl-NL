---
description: JavaScript API-referentie voor Flyout Viewer.
seo-description: JavaScript API-referentie voor Flyout Viewer.
seo-title: FlyoutViewer
solution: Experience Manager
title: FlyoutViewer
topic: Dynamic media
uuid: 070ae248-34fd-40fb-9d40-2c7fff388592
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutViewer{#flyoutviewer}

JavaScript API-referentie voor Flyout Viewer.

`FlyoutViewer([config])`

Constructor; Hiermee wordt een nieuwe instantie van de Flyout-viewer gemaakt.

## Parameters {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> optioneel JSON-configuratieobject. Hiermee kunnen alle viewerinstellingen worden doorgegeven aan de constructor en wordt het aanroepen van afzonderlijke settermethoden vermeden. Bevat de volgende eigenschappen: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> -id van de DOM-container (normaal gesproken een <span class="codeph"> DIV </span>) waarin de viewer wordt ingevoegd. Het is niet nodig om het containerelement te hebben dat tegen de tijd wordt gecreeerd deze methode wordt geroepen. De container moet echter bestaan wanneer <span class="codeph"> init() </span> wordt uitgevoerd. Vereist. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON-object met viewerconfiguratieparameters waarbij de eigenschapnaam een viewer-specifieke configuratieoptie of een SDK-modifier is en de waarde van die eigenschap een corresponderende instellingswaarde is. Vereist. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> Handlers </span> - <span class="codeph"> {Object} </span> JSON-object met callbacks voor viewergebeurtenissen, waarbij de eigenschapnaam de naam van de ondersteunde viewergebeurtenis is en de eigenschapswaarde een JavaScript-functieverwijzing naar een geschikte callback is. Optioneel. <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> Gebeurteniscallbacks </a> voor meer informatie over viewergebeurtenissen. </p> </li> 
      <li id="li_218F9597A60249AEBA43A9E86EAFF8BA"> <p> <span class="codeph"> gelokaliseerdText </span> - { <span class="codeph"> Object </span>} JSON-object met lokalisatiegegevens. Optioneel. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> Lokalisatie van gebruikersinterface-elementen </a> voor meer informatie. </p> <p>Zie de gebruikershandleiding <i>van de SDK van de</i> viewer en het voorbeeld voor meer informatie over de inhoud van het object. Optioneel. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom" 
}, 
"fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer" 
}, 
defaultLocale:"en" 
} 
});
```

