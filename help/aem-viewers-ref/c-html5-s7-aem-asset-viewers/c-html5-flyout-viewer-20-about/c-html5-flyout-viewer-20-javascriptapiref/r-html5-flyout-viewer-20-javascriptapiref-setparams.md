---
description: JavaScript API-referentie voor Flyout Viewer.
seo-description: JavaScript API-referentie voor Flyout Viewer.
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 12a513d3-32a9-411d-965f-f0eaf553d98d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParams{#setparams}

JavaScript API-referentie voor Flyout Viewer.

` setParams( *`param`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value parameterparen gescheiden met <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Stelt een of meer parameters in op een bepaalde waarde. De syntaxis van het methodeargument is identiek aan een URL vraagkoord. Namelijk vertegenwoordigt het naam=waarde paren die met worden gescheiden `&`. Net als in een queryreeks worden namen en waarden met UTF8-codering voor percentages gebruikt. Voordat u aanroept `init()`, moet deze parameter worden aangeroepen. Deze methode is optioneel als de configuratiegegevens van de viewer samen met het JSON-object worden doorgegeven aan de constructor. `config`

Zie ook [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("FlyoutZoomView.zoomfactor=2,3&Swatches.iscommand=op_sharpen%3d1")
```

