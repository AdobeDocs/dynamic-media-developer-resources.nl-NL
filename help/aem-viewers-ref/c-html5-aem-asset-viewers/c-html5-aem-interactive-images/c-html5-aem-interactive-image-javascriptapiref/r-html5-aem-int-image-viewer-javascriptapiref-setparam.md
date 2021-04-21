---
description: JavaScript API-referentie voor Video Image Viewer.
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,Business Practitioner
exl-id: ef307acb-2ff0-46df-a06b-8dbac2e412f9
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# setParam{#setparam}

JavaScript API-referentie voor Video Image Viewer.

` setParam( *`name, value`*)`

Stelt de viewerparameter in op een opgegeven waarde. De parameter is of een viewer-specifieke configuratieoptie of een bepaling van de software ontwikkelingskit. Deze parameter wordt vóór `init()` geroepen.

Deze methode is optioneel als de configuratiegegevens van de viewer samen met het JSON-object `config` zijn doorgegeven aan de constructor.

Zie ook [init](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Parameters {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

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
<instance>.setParam("style", "etc/dam/presets/css/html5_interactiveimage.css")
```
