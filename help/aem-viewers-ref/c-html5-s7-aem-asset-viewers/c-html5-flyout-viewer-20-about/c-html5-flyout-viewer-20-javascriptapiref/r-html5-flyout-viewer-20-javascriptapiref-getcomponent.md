---
title: getComponent
description: JavaScript API-referentie voor Flyout Viewer
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 618d34af-32d0-45bd-928d-7a4e084edbe6
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# getComponent{#getcomponent}

JavaScript API-referentie voor Flyout Viewer

`getComponent(componentId)`

Retourneert een verwijzing naar de Viewer SDK-component die door de viewer wordt gebruikt. De webpagina kan deze methode gebruiken om het gedrag van de viewer buiten de box uit te breiden of aan te passen. Roep deze methode slechts na `initComplete` callback van de viewer is uitgevoerd; anders, kan de component nog niet door de kijkerslogica worden gecreeerd.

## Parameters {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - `{String}` een id van de Viewer SDK-component die door de viewer wordt gebruikt. Deze viewer ondersteunt de volgende component-id&#39;s:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Component-id </p> </th> 
   <th colname="col2" class="entry"> <p>Naam van de klasse Viewer SDK </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> container </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> flyout </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.FlyoutZoomView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stalen </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.Swatches </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Bij het werken met SDK API&#39;s is het belangrijk een correcte, volledig gekwalificeerde SDK-naamruimte te gebruiken, zoals beschreven in [Viewer SDK](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-namespace.md#concept-453501a601634dd1bca7b96878c22605).

Zie de documentatie van de SDK API van de viewer voor meer informatie over een bepaalde component.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Een verwijzing naar de Viewer SDK-component. De methode retourneert `null` als de `componentId` is geen ondersteunde viewercomponent of als de component nog niet door de viewerlogica is gemaakt.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyoutZoomView = <instance>.getComponent("flyout"); 
} 
})
```
