---
title: PanoramaViewer
description: 'Constructor: maakt een nieuwe HTML5 Carousel Viewer-instantie.'
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# PanoramaViewer{#panoramicviewer}

`PanoramicViewer([config])`
Constructor: maakt een nieuwe HTML5 Panoramische Viewer-instantie.

## Parameter {#section-fa807db629ce43bab286b1e1dc96c492}

Met het optionele JSON-configuratieobject config {Object} kunt u alle viewerinstellingen doorgeven aan de constructor en voorkomen dat afzonderlijke settermethoden worden aangeroepen. Bevat de volgende eigenschappen:
* containerId - {String} ID van de DOM-container (normaal gesproken een DIV) waarin de viewer wordt ingevoegd. Het is niet nodig om het containerelement te hebben dat tegen de tijd wordt gecreeerd deze methode wordt geroepen, nochtans moet de container bestaan wanneer init() wordt uitgevoerd. Vereist
* params - {Object} JSON-object met viewerconfiguratieparameters waarbij de naam van de eigenschap viewer-specifieke configuratieoptie of SDK-modifier is en de waarde van die eigenschap een overeenkomende instellingenwaarde is. Vereist
* handlers - {Object} JSON-object met callbacks voor viewergebeurtenissen, waarbij de eigenschapnaam de naam van de ondersteunde viewergebeurtenis is en de eigenschapswaarde een JavaScript-functieverwijzing naar de juiste callback is. Raadpleeg de sectie Gebeurteniscallbacks voor meer informatie over viewergebeurtenissen. Optioneel


## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
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
