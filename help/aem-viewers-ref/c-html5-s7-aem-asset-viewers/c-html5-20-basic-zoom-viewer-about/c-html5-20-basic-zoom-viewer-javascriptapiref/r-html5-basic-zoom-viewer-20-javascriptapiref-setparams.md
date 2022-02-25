---
title: setParams
description: JavaScript API-referentie voor de Basic Zoom Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f142dd72-5e45-44f6-a79b-3eaf6a310bde
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# setParams{#setparams}

JavaScript API-referentie voor de Basic Zoom Viewer.

` setParams( *`param`*)`

Stelt een of meer parameters in op een bepaalde waarde. De syntaxis van het methodeargument is identiek aan een URL vraagkoord. Namelijk vertegenwoordigt het naam=waarde paren die met worden gescheiden `&`. Net als in een queryreeks zijn de namen en waarden procentueel gecodeerd met UTF8. Voordat u belt `init()`, moet deze parameter worden aangeroepen.

Deze methode is optioneel als de configuratiegegevens van de viewer zijn doorgegeven met `config` JSON-object naar constructor.

Zie ook [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> param</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value parameterparen gescheiden met <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.zoomfactor=2,3&ZoomView.iscommand=op_sharpen%3d1")
```
