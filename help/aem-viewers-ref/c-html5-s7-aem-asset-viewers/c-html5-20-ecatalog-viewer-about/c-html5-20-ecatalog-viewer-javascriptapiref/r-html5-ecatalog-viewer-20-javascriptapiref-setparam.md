---
title: setParam
description: JavaScript API-referentie voor eCatalog Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 781982f6-488d-452c-8168-604c708ae6ce
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# setParam{#setparam}

JavaScript API-referentie voor eCatalog Viewer.

` setParam( *`name, value`*)`

Stelt de viewerparameter in op een opgegeven waarde. De parameter is of een viewer-specifieke configuratieoptie of een bepaling van de software ontwikkelingskit. Deze parameter wordt eerder aangeroepen `init()`.

Deze methode is optioneel als de configuratiegegevens van de viewer worden doorgegeven met `config` JSON-object naar de constructor.

Zie ook [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> naam van parameter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
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
