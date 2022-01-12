---
title: setLocalizedText
description: JavaScript API-referentie voor Inline Zoom Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: a0d602f5-e698-4dad-af95-70ef5ef88af6
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# setLocalizedText{#setlocalizedtexts}

JavaScript API-referentie voor Inline Zoom Viewer.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> Object </span>} JSON-object met lokalisatiegegevens. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> Lokalisatie van gebruikersinterface-elementen </a> voor meer informatie . </p> <p>Zie de <i>Gebruikershandleiding van de viewer-SDK</i> en het voorbeeld voor meer informatie over de inhoud van het object. </p> </td> 
  </tr> 
 </tbody> 
</table>

Hiermee stelt u de waarden voor het lokalisatiesymbool in voor een of meer landinstellingen. Deze parameter moet vóór worden aangeroepen `init()`.

Zie ook [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom"},"fr":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer"},defaultLocale:"en"})
```
