---
title: setParam
description: JavaScript API-referentie voor Carousel Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 0829933f-a90b-4066-9904-748f2a727169
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# setParam{#setparam}

JavaScript API-referentie voor Carousel Viewer.

` setParam( *`name, value`*)`

Stelt de viewerparameter in op een opgegeven waarde. De parameter is of een viewer-specifieke configuratieoptie of een bepaling van de software ontwikkelingskit. Deze parameter wordt eerder aangeroepen `init()`.

Deze methode is optioneel als de configuratiegegevens van de viewer zijn doorgegeven met `config` JSON-object naar constructor.

Zie ook [xref](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md).

## Parameters {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

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
<instance>.setParam("style", "etc/dam/presets/css/html5_carouselviewer_dotted_light.css")
```
