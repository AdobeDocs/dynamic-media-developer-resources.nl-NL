---
description: JavaScript API-referentie voor Flyout Viewer.
seo-description: JavaScript API-referentie voor Flyout Viewer.
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic media
uuid: 0c2deb6c-f40f-47e5-a1ef-f5eb5db6ee06
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParam{#setparam}

JavaScript API-referentie voor Flyout Viewer.

` setParam( *`name, value`*)`

Stelt de viewerparameter in op een opgegeven waarde. De parameter is of een viewer-specifieke configuratieoptie of een bepaling van de software ontwikkelingskit. Deze parameter wordt eerder aangeroepen `init()`. Deze methode is optioneel als de configuratiegegevens van de viewer samen met het JSON-object worden doorgegeven aan de constructor. `config`

Zie ook [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> naam </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> naam van parameter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> waarde </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> waarde van parameter. De waarde kan niet met percentages worden gecodeerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```

