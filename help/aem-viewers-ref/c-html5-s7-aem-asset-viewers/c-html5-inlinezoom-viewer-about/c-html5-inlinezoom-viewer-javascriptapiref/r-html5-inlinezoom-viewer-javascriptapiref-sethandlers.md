---
title: setHandlers
description: JavaScript API-referentie voor Inline Zoom Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 233fadf5-4b09-406d-959b-c2c9c4524021
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# setHandlers{#sethandlers}

JavaScript API-referentie voor Inline Zoom Viewer.

`setHandlers(handlers)`

Geeft nul of meer callback-handlers aan. Een vraag aan deze methode beschrijft volledig gebeurtenismanagers die eerder voor die kijkersinstantie werden toegewezen. Moet eerder worden aangeroepen `init()`.

## Parameter {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> handlers </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> JSON-object met callbacks voor viewergebeurtenissen, waarbij de eigenschapsnaam de naam van de ondersteunde viewergebeurtenis is en de eigenschapswaarde een JavaScript-functieverwijzing naar een geschikte callback is. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> Gebeurteniscallbacks </a> voor meer informatie over viewergebeurtenissen. </p> </td> 
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
