---
description: JavaScript API-referentie voor Carousel Viewer.
seo-description: JavaScript API-referentie voor Carousel Viewer.
seo-title: CarouselViewer
solution: Experience Manager
title: CarouselViewer
topic: Dynamic media
uuid: 443a5b54-b5f6-4594-810b-ce9b2ba40611
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---


# CarouselViewer{#carouselviewer}

JavaScript API-referentie voor Carousel Viewer.

`CarouselViewer([config])`

Constructor maakt een nieuwe HTML 5 Carousel Viewer-instantie.

## Parameters {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object}  </span> optioneel JSON-configuratieobject. Hiermee kunnen alle viewerinstellingen aan de constructor worden doorgegeven om te voorkomen dat afzonderlijke settermethoden worden aangeroepen. Bevat de volgende eigenschappen: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}- </span> id van de DOM-container (normaal gesproken een  <span class="codeph"> DIV  </span>) waarin de viewer wordt ingevoegd. Tegen de tijd dat deze methode wordt geroepen, is het niet noodzakelijk om het containerelement te hebben gecreeerd. De container moet echter bestaan wanneer <span class="codeph"> init() </span> wordt uitgevoerd. </p> <p>Vereist. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params  </span> -  <span class="codeph"> {Object}  </span> JSON-object met viewerconfiguratieparameters waarbij de naam van de eigenschap viewer-specifieke configuratieoptie of SDK-modifier is en de waarde van die eigenschap een corresponderende instellingswaarde is. </p> <p>Vereist. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> handlers  </span> -  <span class="codeph"> {Object}  </span> JSON-object met callbacks voor viewergebeurtenissen, waarbij de naam van de eigenschap de naam van de ondersteunde viewergebeurtenis is en de waarde van de eigenschap een JavaScript-functieverwijzing naar de juiste callback is. </p> <p>Optioneel. </p> <p>Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Gebeurteniscallbacks </a> voor meer informatie over viewergebeurtenissen. </p> </li> 
      <li id="li_CD88EDB586B241DBB87B13709F24C454"> <p> <span class="codeph"> localizedText  </span> -  <span class="codeph"> {Object}  </span> </p> <p> JSON-object met lokalisatiegegevens. Zie Lokalisatie van gebruikersinterface-elementen en het voorbeeld voor meer informatie over de inhoud van het object. </p> <p>Optioneel </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left" 
}, 
"fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste" 
}, 
defaultLocale:"en" 
} 
});
```

