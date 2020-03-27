---
description: JavaScript API-referentie voor Carousel Viewer.
seo-description: JavaScript API-referentie voor Carousel Viewer.
seo-title: getComponent**
solution: Experience Manager
title: getComponent**
topic: Dynamic media
uuid: b5449564-c01c-4bb3-b265-b8d70e5f1b54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getComponent**{#getcomponent}

JavaScript API-referentie voor Carousel Viewer.

`getComponent(componentId)`

Retourneert een verwijzing naar de Viewer SDK-component die door de viewer wordt gebruikt. De webpagina kan deze methode gebruiken om het gedrag van de viewer buiten de box uit te breiden of aan te passen. Roep deze methode alleen aan nadat de callback van de `initComplete` viewer is uitgevoerd, anders kan de component nog niet door de viewerlogica worden gemaakt.

## Parameters {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

` *`componentID`*` `{String}` - een id van de Viewer SDK-component die door de viewer wordt gebruikt. Deze viewer ondersteunt de volgende component-id&#39;s:

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
   <td colname="col1"> <p> <span class="codeph"> carrouselView </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.CarouselView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imageMapEffect </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.mageMapEffect </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> controlBar </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> setIndicator </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.SetIndicator </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nextButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> prevButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Wanneer u werkt met SDK API&#39;s, is het belangrijk de juiste volledig gekwalificeerde SDK-naamruimte te gebruiken, zoals wordt beschreven in de naamruimte [van de SDK van de](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-namespace.md)Viewer.

Raadpleeg de SDK API-documentatie van de viewer voor meer informatie over een bepaalde component.

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` een verwijzing naar de Viewer SDK-component. De methode wordt geretourneerd `null` als de viewercomponent `componentId` geen ondersteunde viewercomponent is of als de component nog niet door de viewerlogica is gemaakt.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var carouselView = <instance>.getComponent("carouselView"); 
} 
})
```

