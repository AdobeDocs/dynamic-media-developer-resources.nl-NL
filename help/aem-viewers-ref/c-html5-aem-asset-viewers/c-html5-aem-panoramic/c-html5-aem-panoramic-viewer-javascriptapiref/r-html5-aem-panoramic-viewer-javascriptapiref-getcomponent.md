---
title: getComponent
description: JavaScript API-referentie voor Panoramische Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 3c228b84-fbad-434f-96b4-d52485711844
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# getComponent{#getcomponent}

JavaScript API-referentie voor Panoramische Viewer

`getComponent(componentId)`


Retourneert een verwijzing naar de Viewer SDK-component die door de viewer wordt gebruikt. De webpagina kan deze methode gebruiken om het gedrag van de viewer buiten de box uit te breiden of aan te passen. Roep deze methode slechts na `initComplete` callback van de viewer is uitgevoerd, anders wordt de component mogelijk nog niet gemaakt door de viewerlogica.

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
   <td colname="col1"> <p> <span class="codeph"> panoramischWeergave </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.PanoramicView </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Wanneer u werkt met SDK API&#39;s, is het belangrijk de juiste volledig gekwalificeerde SDK-naamruimte te gebruiken, zoals wordt beschreven in [Viewer SDK-naamruimte](../../../c-html5-aem-asset-viewers/c-html5-aem-panoramic/c-html5-aem-panoramic-viewer-sdk-namespace.md#concept-4ee8657c7d67421f8e7880130a246621).

Zie de documentatie van de SDK API van de viewer voor meer informatie over een bepaalde component.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` een verwijzing naar de Viewer SDK-component. De methode retourneert `null` als de `componentId` is geen ondersteunde viewercomponent of als de component nog niet door de viewerlogica is gemaakt.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var panoramicView = <instance>.getComponent("panoramicView"); 
} 
})
```
