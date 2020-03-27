---
description: JavaScript API-referentie voor Carousel Viewer
seo-description: JavaScript API-referentie voor Carousel Viewer
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic media
uuid: 5e1e9c8f-866b-4730-9978-b45face85667
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setHandlers{#sethandlers}

JavaScript API-referentie voor Carousel Viewer

`setHandlers(handlers)`

Geeft nul of meer callback-handlers aan. Een vraag aan deze methode beschrijft volledig gebeurtenismanagers die eerder voor die kijkersinstantie werden toegewezen. Moet eerder worden opgeroepen `init()`.

## Parameter {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> handlers </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> JSON-object met callbacks voor viewergebeurtenissen. De eigenschapnaam is de naam van de ondersteunde viewergebeurtenis. De eigenschapswaarde is een JavaScript-functieverwijzing naar een geschikte callback. </p> <p>Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Gebeurteniscallbacks </a> voor meer informatie over viewergebeurtenissen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```

