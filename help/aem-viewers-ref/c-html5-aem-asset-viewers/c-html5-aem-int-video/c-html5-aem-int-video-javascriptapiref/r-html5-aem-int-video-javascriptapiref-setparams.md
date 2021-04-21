---
description: JavaScript API-referentie voor Interactive Video Viewer.
solution: Experience Manager
title: setParams
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 32d26999-7815-4c71-ad4c-b7db99ec3d3b
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# setParams{#setparams}

JavaScript API-referentie voor Interactive Video Viewer.

` setParams( *`param`*)`

Stelt een of meer parameters in op een bepaalde waarde. De syntaxis van het methodeargument is identiek aan een URL vraagkoord. Namelijk vertegenwoordigt het naam=waarde paren die met `&` worden gescheiden. Net als in een queryreeks zijn de namen en waarden procentueel gecodeerd met UTF8. Voordat u `init()` aanroept, moet deze parameter worden aangeroepen.

Deze methode is optioneel als de configuratiegegevens van de viewer samen met het JSON-object `config` zijn doorgegeven aan de constructor.

Zie ook [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).


## Parameter {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

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
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```
