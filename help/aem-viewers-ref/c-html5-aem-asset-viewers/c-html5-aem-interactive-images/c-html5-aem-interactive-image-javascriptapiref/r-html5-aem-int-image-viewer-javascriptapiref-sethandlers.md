---
title: setHandlers
description: JavaScript API-referentie voor Interactive Image Viewer
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: a5e42842-dc88-454b-8229-33a65c01bf88
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---

# setHandlers{#sethandlers}

JavaScript API-referentie voor Interactive Image Viewer

`setHandlers(handlers)`

Geeft nul of meer callback-handlers aan. Een vraag aan deze methode beschrijft volledig gebeurtenismanagers die eerder voor die kijkersinstantie werden toegewezen. Moet eerder worden aangeroepen `init()`.

## Parameter {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> handlers </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> JSON-object met callbacks voor viewergebeurtenissen. De eigenschapnaam is de naam van de ondersteunde viewergebeurtenis. De eigenschapswaarde is een JavaScript-functieverwijzing naar een geschikte callback. </p> <p>Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Gebeurteniscallbacks </a> voor meer informatie over viewergebeurtenissen. </p> </td> 
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
