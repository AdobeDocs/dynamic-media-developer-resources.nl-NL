---
title: setParams
description: JavaScript API-referentie voor Panoramische Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 3c228b84-fbad-434f-96b4-d52485711844
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# setParams{#setparams}

JavaScript API-referentie voor Panoramische Viewer.

` setParams( *`param`*)`

Stelt een of meer parameters in op een bepaalde waarde. De syntaxis van het methodeargument is identiek aan een URL vraagkoord. Namelijk vertegenwoordigt het naam=waarde paren die met worden gescheiden `&`. Net als in een queryreeks zijn de namen en waarden procentueel gecodeerd met UTF8. Voordat u belt `init()`, moet deze parameter worden aangeroepen.

Deze methode is optioneel als de configuratiegegevens van de viewer zijn doorgegeven met `config` JSON-object naar constructor.


## Parameter {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

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
<instance>.setParams("PanoramicView.fmt=png&PanoramicView.iscommand=op_sharpen%3d1")
```
