---
title: InteractiveImage
description: JavaScript API-referentie voor Video Image Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 165de14f-0031-4969-9671-5da310d44c28
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# InteractiveImage{#interactiveimage}

JavaScript API-referentie voor Video Image Viewer.

`InteractiveImage([config])`

Constructor, maakt een Video Image Viewer-instantie.

## Parameters {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> Met het optionele JSON-configuratieobject kunnen alle viewerinstellingen aan de constructor worden doorgegeven om te voorkomen dat afzonderlijke settermethoden worden aangeroepen. Bevat de volgende eigenschappen: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID van de DOM-container (gewoonlijk een <span class="codeph"> DIV </span>) waarin de viewer wordt ingevoegd. Tegen de tijd dat deze methode wordt geroepen, is het niet noodzakelijk om het containerelement te hebben gecreeerd. De container moet echter bestaan wanneer <span class="codeph"> init() </span> wordt uitgevoerd. </p> <p>Vereist. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> param </span> - <span class="codeph"> {Object} </span> JSON-object met parameters voor viewerconfiguratie waarbij de naam van de eigenschap viewer-specifieke configuratieoptie of SDK-modifier is en de waarde van die eigenschap een corresponderende instellingswaarde is. </p> <p>Vereist. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> handlers </span> - <span class="codeph"> {Object} </span> JSON-object met callbacks voor viewergebeurtenissen, waarbij de eigenschapsnaam de naam van de ondersteunde viewergebeurtenis is en de eigenschapswaarde een JavaScript-functieverwijzing naar de juiste callback is. </p> <p>Optioneel. </p> <p>Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Gebeurteniscallbacks </a> voor meer informatie over viewergebeurtenissen. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
  "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
} 
});
```
