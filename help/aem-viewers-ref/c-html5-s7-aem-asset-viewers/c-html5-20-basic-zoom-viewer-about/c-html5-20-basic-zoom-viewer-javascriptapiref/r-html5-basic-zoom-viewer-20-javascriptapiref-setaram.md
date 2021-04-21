---
description: JavaScript API-referentie voor de Basic Zoom Viewer.
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---


# setParam{#setparam}

JavaScript API-referentie voor de Basic Zoom Viewer.

` setParam( *`name, value`*)`

Stelt de viewerparameter in op een opgegeven waarde. De parameter is of een viewer-specifieke configuratieoptie of een bepaling van de software ontwikkelingskit. Deze parameter wordt vóór `init()` geroepen.

Deze methode is optioneel als de configuratiegegevens van de viewer samen met het JSON-object `config` zijn doorgegeven aan de constructor.

Zie ook [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> naam van parameter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> waarde van parameter. De waarde kan niet met percentages worden gecodeerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```

