---
title: PanoramaViewer
description: 'Constructor: maakt een HTML5 Panoramische Viewer-instantie.'
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---

# PanoramaViewer{#panoramicviewer}

`PanoramicViewer([config])`
Constructor: maakt een HTML5 Panoramische Viewer-instantie.

## Parameter {#section-fa807db629ce43bab286b1e1dc96c492}

config
{Object} Met het optionele JSON-configuratieobject kunt u alle viewerinstellingen doorgeven aan de constructor en het aanroepen van afzonderlijke settermethoden voorkomen. Het bevat de volgende eigenschappen:

* containerId - {String} Id van de DOM-container (normaal gesproken een DIV) waarin de viewer wordt ingevoegd. Het is niet nodig om het containerelement te hebben dat tegen de tijd wordt gecreeerd deze methode wordt geroepen, nochtans moet de container bestaan wanneer init() in werking wordt gesteld. Vereist
* param - {Object} JSON-object met parameters voor viewerconfiguratie waarbij de naam van de eigenschap viewer-specifieke configuratieoptie of SDK-modifier is en de waarde van die eigenschap een corresponderende instellingswaarde is. Vereist
* handlers - {Object} JSON-object met callbacks voor viewergebeurtenissen, waarbij de eigenschapsnaam de naam van de ondersteunde viewergebeurtenis is en de eigenschapswaarde een JavaScript-functieverwijzing naar de juiste callback is. Zie de sectie Callbacks van de Gebeurtenis voor meer informatie over kijkersgebeurtenissen. Optioneel.


## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
},
"handlers":{
    "initComplete":function() {
        console.log("init complete");
}
}
});
```
