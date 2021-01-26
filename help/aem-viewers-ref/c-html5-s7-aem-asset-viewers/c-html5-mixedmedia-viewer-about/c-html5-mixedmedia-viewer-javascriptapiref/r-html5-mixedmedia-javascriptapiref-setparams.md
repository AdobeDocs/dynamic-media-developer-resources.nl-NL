---
description: JavaScript API-referentie voor gemengde media-viewer.
seo-description: JavaScript API-referentie voor gemengde media-viewer.
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic Media
uuid: 46db0ce3-fd70-4577-92ed-e7d2d15e0dab
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# setParams{#setparams}

JavaScript API-referentie voor gemengde media-viewer.

` setParams( *`param`*)`

Stelt een of meer parameters in op een bepaalde waarde. De syntaxis van het methodeargument is identiek aan een URL vraagkoord. Namelijk vertegenwoordigt het naam=waarde paren die met `&` worden gescheiden. Net als in een queryreeks zijn de namen en waarden procentueel gecodeerd met UTF8. Voordat u `init()` aanroept, moet deze parameter worden aangeroepen. Deze methode is optioneel als de configuratiegegevens van de viewer samen met het JSON-object `config` aan de constructor worden doorgegeven.

Zie ook [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> param</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value parameterparen gescheiden met  <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.zoomstep=2,3&ZoomView.iscommand=op_sharpen%3d1")
```

