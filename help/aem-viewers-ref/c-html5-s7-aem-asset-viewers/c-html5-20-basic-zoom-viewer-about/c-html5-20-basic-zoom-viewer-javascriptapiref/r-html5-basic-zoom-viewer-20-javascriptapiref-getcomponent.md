---
description: JavaScript API-referentie voor de Basic Zoom Viewer
seo-description: JavaScript API-referentie voor de Basic Zoom Viewer
seo-title: getComponent
solution: Experience Manager
title: getComponent
topic: Dynamic media
uuid: 3e9f4baf-4914-42a8-a1bf-5756cbbd407b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# getComponent{#getcomponent}

JavaScript API-referentie voor de Basic Zoom Viewer

`getComponent(componentId)`

Retourneert een verwijzing naar de Viewer SDK-component die door de viewer wordt gebruikt. De webpagina kan deze methode gebruiken om het gedrag van de viewer buiten de box uit te breiden of aan te passen. Roep deze methode alleen aan nadat de callback van de `initComplete`-viewer is uitgevoerd. Als dit niet het geval is, wordt de component mogelijk nog niet door de viewerlogica gemaakt.

## Parameters {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

` *`componentID`*` :  `{String}` een id van de Viewer SDK-component die door de viewer wordt gebruikt. Deze viewer ondersteunt de volgende component-id&#39;s:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Component-id </p> </th> 
   <th colname="col2" class="entry"> <p>Naam van de klasse Viewer SDK </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> container  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomView  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.ZoomView  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomInButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomInButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomOutButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomOutButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomResetButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomResetButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> closeButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.CloseButton  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Wanneer u werkt met SDK API&#39;s, is het belangrijk de juiste volledig gekwalificeerde SDK-naamruimte te gebruiken, zoals wordt beschreven in de naamruimte van de SDK van de Viewer

Raadpleeg de SDK API-documentatie van de viewer voor meer informatie over een bepaalde component.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` een verwijzing naar de Viewer SDK-component. De methode retourneert `null` als `componentId` geen ondersteunde viewercomponent is of als de component nog niet door de viewerlogica is gemaakt.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
} 
})
```

